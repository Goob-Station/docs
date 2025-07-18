# Identity3

| Designers                                            | Implemented | GitHub Links |
|------------------------------------------------------|-------------|--------------|
| Misandry | :x: Lmao       | 2030         |

# Existing issue

Identity system is old - it has been virtually untouched since [2022](https://github.com/space-wizards/space-station-14/pull/9612) when Kara/mirrorcult and Moony had implemented it.
The only update since then has been hiding your character’s name if you have no ID and no visible face.

However, this never solved the core problem of "everyone knows everyone": for example, hearing "Commander Zeta" over the radio or recognizing "Agent Kilo" by face.
Not only is this illogical, but it also contradicts a fundamental design principle of roleplay, since everyone knowing everyone else encourages metagaming.

This proposed rework aims to fix these issues by simulating how an average person naturally identifies others.

# Terminology

ID Card - your standard issue ID card with a name on it.
Descriptor - a description of the character, e.g. old man, young moth woman, etc.
Voice - heard **clear** speech coming from a mob

# Core Tenet

**No-one knows anyone anymore**, within reason.

Identification revolves around ID cards — what’s on the card is recognized as belonging to the person wearing it.
If you hear someone with a visible ID reading "Rango Chains," you **might** recognize their voice later.
If you see someone with a clear face and the same ID, you **might** visually recognize them afterward.

You don’t always notice every small detail in the moment, so you aren’t guaranteed to remember someone’s information perfectly.

# Basic Setup

**Examining people defaults to a descriptor**

Player characters start with knowledge of their department’s coworkers and any relevant members, for example:
* Engineers know other engineers and the Chief Engineer. Security officers know other security officers.
* The Chief Engineer knows both other engineers **and** Command staff.
* Scientists **do not** know anyone from Cargo or Medical, as they belong to different departments.

There are some special cases:

* The Captain knows other Command staff, but not members of other departments.
* The Head of Personnel knows **everyone’s** identity at the start of the round.
* Atmospheric technicians know every engineer, but engineers don’t know atmospheric technicians — to reinforce the atmos elitism.
* Passengers don’t know **anyone**, and no one knows passengers.
* Security Cadets don’t recognize Command characters; Security Officers do.
* ~~Virologists don’t know anyone~~
* Latejoins, while announced, are not immediately recognized by anyone.

# The Woven Web of Relations

**The ID card is now an item slot on the jumpsuit.**

As established earlier, to remember someone’s identity you need a reference (face and/or voice) plus identifying information — their name.  
Every overheard or observed interaction involving a visible ID card with information gives a chance to remember that person.  
Being physically closer increases that chance, and it’s higher if you see their face rather than just hearing their voice.

If someone is not recognized, their name is read from their ID card. If you hear their voice, the name from the ID card is used if it has been seen or remembered; otherwise, a descriptor (e.g. young woman, old moth) is used.  
If someone has no ID card and neither their face nor voice is recognized, only a descriptor is given.
Someone without identification cannot be remembered by any means, so they are never associated or recognized mechanically.  

An ID card **cannot be read** if it's in the PDA slot.

# Implications, Complications

**Identity blocking masks will NOT always be a requirement to have your identity obscured.**

The metagame shifts from "pressing your examine keybind and screaming their name on comms" to remembering how the adversary looked 80% of the time. If you didn't know their name as they were beating you - you at least should remember how they looked.
Syndicate communication and other clandestine channels can be used more freely with lesser risk of being recognized by any eavesdroppers.
**Voice mask is largely nerfed**, you should be able to mimic voice only of people *you* know. To conceal yourself a voice modulator mask from /tg/ can be of better use, which will force a descriptor no matter what.

Kill and protect objectives immediately provide all required information about their target.

Should there be a conflict between what you see and what you know - its stated as such, for example:
* A character you recognize as "Major Duhk", but carrying an ID of "Urist McHands" - Major Duhk (as Urist McHands)
* A character you don't recognize, see carrying an ID of "Urist McScales", but don't recognize them as "Urist McScales" - Unknown (as Urist McScales)
* A character you don't recognize by voice, but recognize by face as "Jack Pierson" - Jack Pierson.
* * Also, higher chance to recognize their identity by their face in addition to voice.
* * Works the other way too.

# Social memory

**One person can only remember so many faces in a short timespan**

Did you ever remember everyone in a group from just one 5-minute session of who's who?
Neither did anyone, really.

Depending on their job or role, characters have a limited number of additional identities they can remember.
An engineer may have the capacity to remember, for example, 10 other characters outside his default known co-workers.
This works in a stack-type system - "Social memory", where any new or **refreshed** identity is put at the top of the stack, the last item of the stack is removed if the amount of relationships exceeds the limit.
This allows for people being interacted the most to be continuously remembered, while those remembered in a one-off interaction are quickly forgotten. 

An identity is refreshed and moved to the top of the stack whenever you interact with a recognized individual.

An identity can be "permanently" remembered if an excessive amount of interactions is done - in which case it's added to the "default" list and stops participating in the social memory stack.