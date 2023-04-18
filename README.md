# WezTerm Finder Integration

This repository provides macOS Finder integration for WezTerm, a GPU-accelerated cross-platform terminal emulator and multiplexer. The integration consists of two parts:

 - A Finder service to open a folder in a new WezTerm window.
 - An Automator application to open files with a custom command in a new WezTerm window and helix-editor.

## Open Folder in WezTerm Service

This service allows you to right-click a folder in Finder and open a new WezTerm window with the folder as the current working directory.

### Installation

1. Download the `New WezTerm window from here.workflow` file from this repository.
2. Move the downloaded file to ~/Library/Services/.
3. The service should now be available. You can right-click a folder in Finder, navigate to "Quick Actions" (or "Services" in older macOS versions), and select "Open in WezTerm" to open the folder in a new WezTerm window.

## Open TOML Files in WezTerm Application

This Automator application allows you to open files in a new WezTerm window, executing the hx command with the path to the file. The example is for .toml files

### Installation

1. Download the OpenTOMLinWezTerm.app file from this repository.
2. Move the downloaded file to your Applications folder or another location of your choice.
3. To set the downloaded application as the default for opening .toml files, right-click a .toml file in Finder, select Get Info (or press Cmd + I), and find the "Open with" section. Click the dropdown menu and select "Other...". Navigate to the location where you saved the OpenTOMLinWezTerm.app, select it, and click Open. Finally, click the Change All... button to apply this change to all .toml files.

Now, when you double-click a .toml file in Finder, it will open a new WezTerm window and execute the hx command with the path to the file.