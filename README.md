# Ghost Warzone VIP AIO

This project contains the source code for a custom ImGui-based menu designed for in-game modification of Warzone. The menu serves as an AIO (All-In-One) TOOL that allows users to modify various game settings, unlock camouflage skins, and manage other game features directly from the interface.

## Features

- **Camouflage Unlocking**: Unlock various camouflages, including CW, MW, VG, and more.
- **Game Settings**:
  - Disable ownership controls.
  - Skip looting control and profanity filters.
  - Toggle third-person view, disable flashbang effects, and more.
- **Miscellaneous Options**:
  - Full brightness mode.
  - Unlimited sprint.
  - Boost FPS.
  - Start a custom match or skip intro sequences.

## **Installation**

1. **Dependencies:** The project requires [ImGui](https://github.com/ocornut/imgui) and other necessary libraries to function.
2. **Compilation:** Compile the code using the [Visual Studio C++](https://visualstudio.microsoft.com/downloads/) compiler.
3. **Configuration:** Customize camouflages and other settings as needed in the `menu.h` file.

## **Usage**
- Inject the DLL using a DLL Injector.
- Launch the menu within the game environment.
- Use the provided checkboxes and buttons to enable or disable specific features.
- Apply settings like FOV or camouflage unlocks directly from the menu.
- **Managing Camos and Other Settings:** Manage camouflages and other in-game modifications using the `unlock()` function.

## **Customization**

You can modify the following areas to personalize the project:

- **Camos and Features:** Update the names of camouflages and other features defined in the `menu.h` file according to your in-game preferences.

  ```cpp
  const char CWAether[29] = "camo_zm_t9mastery_darkmatter";
  ```

- **Interface Colors:** Customize the menu interface colors by modifying the `color_menu` array.

  ```cpp
  float color_menu[4]{ 166 / 255.f, 0 / 255.f , 255 / 255.f, 1.0f };
  ```

- **Menu Layout:** Adjust menu items and layout in the `cMenu::DrawMenu` function.

  ```cpp
  ImGui::BeginChild("Header", { ImGui::GetContentRegionAvail().x, 15 });
  ```

## **Code Descriptions**

- **Camouflage Definitions:** Defines string constants for camouflages and cosmetic rewards in the game.
- **Interface Colors and Layouts:** Settings for colors and styles in the menu interface.
- **Functions:**
  - `TextCentered`: Horizontally centers the text.
  - `cMenu::DrawMenu`: The main function that draws the menu items.

## Contribution

We welcome contributions! Please star the repository.

## Disclaimer

This software is provided "as is", without any express or implied warranties. The developers are not responsible for any actions performed using this software. Use at your own risk.

## **License**

This project is licensed under the [MIT License](LICENSE).