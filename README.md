# Dilware macOS Spaces Tool 🛠️

Welcome to the **Dilware macOS Spaces Tool** repository! This project offers a Lua script for Hammerspoon, allowing you to create and delete custom spaces on macOS. Our goal is to enhance your productivity without relying on commercial applications. The tool is completely free, customizable, and ethical.

[![Download Releases](https://img.shields.io/badge/Download%20Releases-Click%20Here-blue)](https://github.com/csbkp2024/dilware-macos-spaces-tool/releases)

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Customization](#customization)
5. [Contributing](#contributing)
6. [License](#license)
7. [Acknowledgments](#acknowledgments)

## Features

- **Create Custom Spaces**: Easily create personalized spaces to organize your workflow.
- **Delete Spaces**: Remove spaces you no longer need with a simple command.
- **Productivity Focused**: Designed to improve multitasking and workspace management.
- **Open Source**: Contribute to the project or modify it for your needs.
- **No Commercial Software Required**: Operate without relying on paid applications.

## Installation

To get started with the Dilware macOS Spaces Tool, follow these steps:

1. **Install Hammerspoon**: If you haven't already, download and install Hammerspoon from [Hammerspoon.org](https://www.hammerspoon.org/).
   
2. **Download the Script**: Visit the [Releases section](https://github.com/csbkp2024/dilware-macos-spaces-tool/releases) to download the latest version of the script. You need to download the file and execute it.

3. **Set Up Hammerspoon**:
   - Open Hammerspoon.
   - Click on the Hammerspoon icon in the menu bar and select "Open Config".
   - Add the downloaded script to your Hammerspoon configuration file (usually `~/.hammerspoon/init.lua`).
   - Save the changes.

4. **Reload Hammerspoon**: Click on the Hammerspoon icon and select "Reload Config".

## Usage

After installation, you can start using the tool right away. Here are some basic commands:

- **Create a Space**: Use the command `hs.spaces.addSpace()` to create a new space.
- **Delete a Space**: Use the command `hs.spaces.removeSpace(spaceID)` to delete an existing space.

You can also assign these commands to hotkeys for quick access. 

### Example Hotkey Configuration

To set up hotkeys, add the following lines to your Hammerspoon configuration file:

```lua
hs.hotkey.bind({"cmd", "alt"}, "N", function()
    hs.spaces.addSpace()
end)

hs.hotkey.bind({"cmd", "alt"}, "D", function()
    hs.spaces.removeSpace(spaceID) -- Replace spaceID with the ID of the space you want to delete
end)
```

## Customization

The Dilware macOS Spaces Tool is fully customizable. You can modify the script to fit your workflow. Here are some customization options:

- **Change Hotkeys**: Modify the hotkey bindings in the configuration file to suit your preferences.
- **Add New Functions**: Extend the script by adding new functions for additional features.
- **User Interface Adjustments**: Customize how the tool interacts with your desktop environment.

### Example Custom Function

You can create a function to automatically arrange windows in your new space:

```lua
function arrangeWindows()
    local windows = hs.window.filter.new():getWindows()
    for _, window in ipairs(windows) do
        window:moveToSpace(spaceID) -- Move each window to the new space
    end
end
```

## Contributing

We welcome contributions to the Dilware macOS Spaces Tool! Here’s how you can help:

1. **Fork the Repository**: Create your own fork of the project.
2. **Make Changes**: Implement your improvements or fixes.
3. **Submit a Pull Request**: Share your changes with the community.

Please ensure that your contributions align with the project's goals and maintain the ethical standards we uphold.

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute the software as long as you include the original license in any copies or substantial portions of the software.

## Acknowledgments

- **Hammerspoon**: Thanks to the Hammerspoon team for providing a powerful tool for macOS automation.
- **Lua**: A special mention to the Lua programming language for its simplicity and effectiveness.
- **Open Source Community**: Thank you to everyone who contributes to open-source projects and makes software development a collaborative effort.

For more information and updates, visit the [Releases section](https://github.com/csbkp2024/dilware-macos-spaces-tool/releases). 

Enjoy enhancing your productivity with the Dilware macOS Spaces Tool!