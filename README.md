# Gam101_UE_eg_mods-6789

Examples of Array, Map, Enum, Struct for week 9. Some examples of previously covered topics incl. UI updates, inheritance, use of Delta Time. Also event binding, function binding, even a Macro.
Coming soon; Lerp, Sin and other game math. 

* Wander around with WASD, mouselook and space for jump. 
* Collect collectable (skulls, fish pinatas, etc) and see the count go up in the ui.
  - Demonstrates use of: enums, event dispatchers and handlers (custom events), maps and polymorphism.
* Note two columns spinning at different rates, based on the "Rotations Per Second" variable in their details panel when selected.
  - Demonstrates use of: Event Tick, delta time (time since previous frame started), maths and applying rotation.


## Some of the Blueprint Classes

### Structs Widget
  Location: Content/ThirdPerson/Blueprints/WBP_StructsWidget
  Type: Widget Blueprint
  Name Meaning: It was created initially for struct/container examples

### E_CollectableType
  Location: Content/ThirdPerson/Blueprints/

An enum (enumeration type) that contains names of the different types of collectables (and assigns integers to each as an id), and we use that in any Blueprints that need to do anything differently based on collectable type, like updating the UI. Also, with an enum like this you don't always have to remember the exact names of different collectable types, you just pick them from a drop-down list, or they appear in a switch statement automatically.

### BP_ThirdPerson Character
  Location: Content/ThirdPerson/Blueprints/

Features:
  - Notes overlaps, checks if they're collectables
  - Keeps a map collection with the count of each collected collectable, and the keys for them use an Enum (E_CollectableType) so you get a drop down instead of having to check the key names or risk mispelling them (more info below)
  - Dispatches event collectables are collected, with type {enum) and count
  - also when speaking
  - Epic's Third person template additions
  