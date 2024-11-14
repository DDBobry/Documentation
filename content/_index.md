+++
title = "Home Page"
type = "home"
+++

Welcome to the official documentation for **ZTD**! This documentation is designed to help both developers and modders understand the inner workings of the game, from entity definitions to modding capabilities. Here, you’ll find comprehensive information about the **XML data structure** used to define in-game elements like buildings, enemies, attacks, and upgrades, along with a guide to using the **Mod API** for customizing game mechanics and creating new content.

---

## Overview

**ZTD** is a strategic game where players must build defenses to fend off waves of zombies. The game's core mechanics and content are designed to be data-driven, allowing for easy customization and extension through XML files. This approach enables modders and developers to adjust gameplay elements, create new entities, and configure complex behaviors without diving into the core codebase.

### Key Topics in This Documentation:

- **XML Data Structure**: A breakdown of each XML element used in ZTD. Each element plays a unique role in defining game logic, behaviors, and visual properties.
  
- **Mod API**: A guide to the Mod API, designed to allow users to introduce new gameplay mechanics, modify existing entities, and create custom scripts that interact with the game.

---

### Special Note for Modders

The path prefix `__base__` is used to refer to assets that are part of the **ZTD** core game files. When modders create their own content, this path is replaced by `__mod_name__`. This is the folder name of the mod inside the `mods` directory, which holds the custom content specific to that mod.

For example:
- In the **ZTD** game itself, the path `__base__/assets/textures/zombie.png` refers to an image asset in the core game.
- For a mod called `myMod`, the path would look like `__my_mod__/assets/textures/zombie.png`. Here, `my_mod` is the name of the mod, and the asset path points to that mod's specific textures located in the `mods/my_mod/assets/textures/` directory.

This structure allows modders to use custom textures, sprites, and other assets, while maintaining compatibility with the core game content.


---

This documentation is continuously updated to reflect the latest changes and improvements. Dive into the sections to learn more about how to configure and extend ZTD!
