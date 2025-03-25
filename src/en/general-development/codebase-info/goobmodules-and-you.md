﻿# Goobmodule and You

## What?

Goobstation provides a way to isolate your code into separate, custom modules. These custom modules retain full functionality like the core modules, while solving the problem of having to recompile the entire game when making changes specific to your downstream.

## Why?

As stated above, there are two primary reasons:

1. **Streamlined Testing and Deployment**: By separating downstream-specific code from the rest of the game, you can compile and test your custom features independently.

2. **Enhanced Modularity**: Instead of managing files and folders within the already bloated Content.Client/Shared/Server projects, you can organize your work into four distinct, fork-specific projects.

This approach is specifically designed to accommodate [Robust Modularity](https://github.com/space-wizards/docs/pull/152) should it be implemented in the future.

## Terminology

- **Core Module**: Modules belonging to the base space-station-14 repository. These include `Content.Client`, `Content.Server`, `Content.Shared`, and their dependencies like `Content.Shared.Database`.

- **Custom Module**: Modules that are part of the Client or Server process but don't belong to Core Modules. In Goobstation's case, these are prefixed with `Content.Goobstation.`.

- **Engine Module**: Modules that are part of RobustToolbox (the game engine). These are prefixed with `Robust.`.

- **.Common**: A module type intended to be shared between Custom and Core modules. These hold interfaces, components, and other types that both module types need to share.

- **ModLoader**: The Module Loader system responsible for loading both core and custom modules.

- **Infix**: The module identifier, which is the middle part of a module name. For example, "Goobstation" in `Content.Goobstation.Common`.

## How

The client loader, unless configured otherwise, loads every Assembly from the `Assemblies` folder with a specific prefix. 
This prefix can be defined in the `manifest.yml` file and defaults to `Content.`.

By creating new projects with the `Content.` prefix, you can have the game automatically load them at startup alongside the core modules.

The dependency structure works as follows:

```
Goobmodules → Core Modules
    ↑
    |
Core Modules → .Common Module → Goobmodules
```

This means:
- Goobmodules (custom modules) can directly reference core modules.
- Core modules cannot directly reference Goobmodules, as this would create a circular dependency.
- Instead, core modules must communicate with Goobmodules through an intermediary `.Common` module.
- The Common module must not depend on either core or custom modules and should be able to build standalone.
- Any part of this system can depend on Engine Modules.

## Implementation

### 1. Check Configuration
Review your `manifest.yml` file to check if any prefixes have been set there.

### 2. Create Your Projects
Create four projects with appropriate naming:
- Prepend them with the correct prefix (default is `Content.`)
- Give them a meaningful name
- Suffix them with the module type (Client, Shared, Server, Common)

For example: `Content.Goobstation.Client`, `Content.Goobstation.Server`, etc.

### 3. Set Up Dependencies
Follow the dependency chain described above. You can use Core Modules as dependencies for your new modules, but not vice versa.

### 4. Create Entry Points
Each module must have an EntryPoint class which inherits from the appropriate type:
- `GameClient` for Client modules
- `GameShared` for Shared or Common modules
- `GameServer` for Server modules

Each of these base classes provides override methods for each RunLevel (PreInit, Init, PostInit). Refer to the engine documentation for more information about these.

### 5. Configure IoC
You'll need to set up Inversion of Control. Refer to the Space Wizards [IoC documentation](https://docs.spacestation14.com/en/robust-toolbox/ioc.html) for detailed information.

### 6. Configure Build Paths
When building your project:
- Ensure your `Client` custom module is built in the same folder as the Core client module
- Similarly, ensure your `Server` custom module is built in the same folder as the Core server module
- `Shared` and `Common` modules should be built as dependencies of the above, so you don't need to set specific build paths for them

## Verification

If you've done everything correctly, Content.Client or Content.Server should load your custom module on startup, with everything registering and initializing properly.
