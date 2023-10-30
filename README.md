<br />
<div align="center">
  <a href="https://lucasradouch.com/shortkit">
    <img src="https://lucasradouch.com/assets/images/shortkit/shortkit-logo.png" alt="Shortkit Logo" width="80" height="80">
  </a>
</div>

# Shortkit

Shortkit is a lightweight menu bar tool for macOS that runs custom commands.

![Screenshot](https://lucasradouch.com/assets/images/shortkit/shortkit-screenshot.png)

## System Requirements

* Apple Silicon or Intel® Mac
* Shortkit supports macOS v11.0+
* Sufficient user permissions to run each command

## Installation

You can download the latest dmg from <https://lucasradouch.com/shortkit> or the [Releases page](https://github.com/lucasradouch/Shortkit/releases).

## How to Shortkit

### General

Use the Shortkit icon to access the menu bar drop-down, run commands, and open the App Preferences. 

After installation, Shortkit can run all the time in the background. For ease of use, you can add it to the list of "Open at Login" items using: System Settings → General → Login Items

### Functionality

Shortkit functions by connecting a single-line shell command with a menu bar item that the user can click to run.

### Adding Commands

You can add Shortkit commands by adding rows in the "Commands" tab of the "Preferences" window. Press the plus button on the bottom left to add a new row/command. You can customize the drop-down display name and function by typing a "Name" and "Command" in the respective fields. You can also click and drag each row up and down to re-order them.

Here are a few simple examples of Shortkit commands:

| Name                           | Command                                                        |
|--------------------------------|----------------------------------------------------------------|
| Say Hi                         | say hi                                                         |
| Open Google                    | open "https://google.com"                                      |
| Camera & Lights                | shortcuts run "Lights Camera Action"                           |
| Work Apps                      | open -a "Mail" && open -a "Calendar"                           |
| Run Script 1                   | /Users/lucas/shortkit_scripts/script_1.sh                      |
| Restart Core Audio             | launchctl kickstart -kp system/com.apple.audio.coreaudiod      |

### Command Directory

For detailed examples of commands & more ways to use Shortkit, go to the [Shortkit Command Directory](https://github.com/lucasradouch/Shortkit/blob/main/Command_Directory.md). If you use Shortkit in a different way, feel free to share it to improve the Directory.

### Running Scripts

You can use Shortkit to run files such as shell scripts, just like you can using Terminal. Here is a simple example:

1. Create a directory where your scripts will live. For example: /Users/lucas/shortkit_scripts
2. Save a script to the directory & make it executable. For example: script_1.sh
3. Add a new command in Shortkit:

| Name                           | Command                                                        |
|--------------------------------|----------------------------------------------------------------|
| Run Script 1                   | /Users/lucas/shortkit_scripts/script_1.sh                      |

4. Run the script using Shortkit by clicking "Run Script 1" in the menu bar dropdown.

### Logs

There is a "Log" tab in the main "Preferences" window. This log provides basic information about the time and success/failure of each command attempt. It is cleared when the App restarts and can also be cleared manually.

### Profiles

You can Load & Save your commands as a "Profile" JSON file to use later or share:

1. Create a directory where your Shortkit Profiles will live. For example: /Users/lucas/shortkit_profiles
2. Save a Profile to the directory using the "Save" button in the "Settings" tab of the "Preferences" window. For example: profile_1.json
3. Load a Profile in Shortkit using the "Load" button.

Upon its first launch, Shortkit will load a default/blank Profile. As you make changes, the main user Profile will be automatically updated. Click "Clear All" to reset to the default/blank Profile.

### Feedback

In some cases, you may want basic feedback (outside of the log) if a command runs successfully.

Shortkit provides optional sound feedback that lets you know if a command succeeds or fails. You can toggle this sound feedback on or off and adjust its volume using the slider in the "Settings" tab of the "Preferences" window.

## Limitations

### Shortkit vs Terminal

While Shortkit implements the basic functionality of Terminal, it does not have a dedicated shell window. If you try to run commands like "top" directly - they will fail. 

To work around this, you can create a script file that opens a Terminal window and runs the command there. Then run the script using Shortkit.

### User Privileges

Shortkit can only run commands that the user has privileges to run. To determine which commands you can run with Shortkit, try executing them in Terminal first.

### Password Protected Commands

Traditionally, some commands will prompt the user for a password before they run. Currently, Shortkit is unable to run these commands. I intentionally kept the app simple, leading to this current limitation.

This may change in the future.

## Notes

### Troubleshooting

If Shortkit is not functioning as you would expect, or commands are failing to run, follow these steps:

1. Make sure macOS is up to date, if possible.
2. Restart your machine.
3. Make sure you have sufficient privileges to run each command.
4. If a command fails to run, try running it using Terminal.

If you are still having a problem, please report it.

### Uninstalling

Shortkit can be uninstalled by quitting the app and moving it to the trash. 

## Community

### Contribute

If you are interested in contributing to future Shortkit releases, I'd love to hear from you. If you have an issue or experience a bug, be sure to report it. If you find an interesting use case, or think of a great feature - definitely let me know. Otherwise, feel free to use all aspects of the software and associated files under the official Shortkit [LICENSE](https://github.com/lucasradouch/Shortkit/blob/main/LICENSE).

### Contact

Lucas Radouch

𝕏 - [@lucasradouch](https://x.com/lucasradouch)  // email - [dev@lucasradouch.com](mailto:dev@lucasradouch.com)


