# MortalMS Development: Planned extra fixes & features for enhancing the base game

## Key

Issue types:

| **Abbreviation** | **Meaning**                                  |
|------------------|----------------------------------------------|
| A                | Audio                                        |
| C                | Combat                                       |
| Ctl              | Player controls                              |
| F                | Fatal, i.e. causes a crash or forces restart |
| G                | Graphical                                    |
| GM               | Game-Mechanical                              |
| I                | User interface                               |
| M                | Meta                                         |
| N                | Networking                                   |
| O                | Outside of the main game                     |

## Issues

| **Priority** | **Difficulty** | **Type(s)** | **Issue**                                               | **Description**                                                                                                                                                                  |
|--------------|----------------|-------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 140          | ?              | A           | Sound plays even when window is not focused             | Players should be able to opt out of this behavior with a setting, allowing music, sounds, both, or neither to be played when not focused.                                       |
| 190          | ?              | M           | Documentation                                           | Ongoing push to document all parts of the client codebase. Mostly this can take the form of Doxygen comments on all member and free functions, but can take other forms as well. |
| 200          | ?              | M           | Need a Lua scripting interface                          | Should use [Sol 2](https://github.com/ThePhD/sol2).                                                                                                                              |
| 203          | Hard           | GM, I       | Cash shop is not implemented                            |                                                                                                                                                                                  |
| 215          | ?              | M           | `noexcept` consistency                                  | Functions that cannot throw (or "can" throw but not in practice, i.e. it is acceptable to `std::terminate`) should be `noexcept`, all others should be `noexcept(false)`.        |
| 220          | ?              | M           | Performance profiling & optimization                    | Profile to look for what can be optimized/what is a performance bottleneck. Ongoing process.                                                                                     |
| 230          | ?              | M           | Use a more efficient hashtable                          | `std::unordered_map` and `std::unordered_set` are plagued by the (useless) interface bits that they have to expose. Use `SwissTable` when Google releases it.                    |
