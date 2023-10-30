# Shortkit Command Directory

This is a directory of some useful commands Shortkit can run. 

**_WARNING: Running commands can affect system operations and data. In general, macOS protects the user with security features, but please use caution: especially with system commands._**

## Siri & Shortcuts

Running Shortcuts is a great way to use Shortkit to control your Mac quickly - without needing any advanced coding experience. Just build using Shortcuts, and launch with Shortkit.

| Name                           |Command                                                              |
|--------------------------------|---------------------------------------------------------------------|
| Siri Voice                     | say Hi my name is Siri                                              |
| Run Shortcut                   | shortcuts run “Shortcut Name”                                       |

## Running Script Files

More advanced users can use Shortkit to run script files to keep things organized, clean, and accessible from the menu bar.

1. Create a directory where your scripts will live. For example: /Users/lucas/shortkit_scripts
2. Save a script to the directory & make it executable. For example: script_1.sh
3. Add a new command in Shortkit: Name: "Run Script 1" Command: "/Users/lucas/shortkit_scripts/script_1.sh"
4. Run the script using Shortkit by clicking "Run Script 1" in the menu bar dropdown.

| Name                           |Command                                                              |
|--------------------------------|---------------------------------------------------------------------|
| Run Script 1                   | /Users/lucas/shortkit_scripts/script_1.sh                           |


## System Services

Restarting system services is another useful way to use Shortkit. Here are some examples:

| Name                           |Command                                                              |
|--------------------------------|---------------------------------------------------------------------|
| Wi-Fi                          | launchctl kickstart -kp system/com.apple.airportd                   |
| Bluetooth                      | launchctl kickstart -kp system/com.apple.blued                      |
| Networking                     | launchctl kickstart -kp system/com.apple.configd                    |
| Core Audio                     | launchctl kickstart -kp system/com.apple.audio.coreaudiod           |
| Dock                           | launchctl kickstart -kp system/com.apple.Dock.agent                 |
| Spotlight                      | launchctl kickstart -kp system/com.apple.metadata.mds               |
| Notification Center            | launchctl kickstart -kp system/com.apple.UserNotificationCenter     |
| Disk Management                | launchctl kickstart -kp system/com.apple.diskarbitrationd           |
| Time Machine                   | launchctl kickstart -kp system/com.apple.backupd-auto               |
| System UI Server               | launchctl kickstart -kp system/com.apple.SystemUIServer             |
| Window Server                  | launchctl kickstart -kp system/com.apple.WindowServer               |

**_Restarting system services may interrupt certain functionalities temporarily. For example, restarting the Window Server will disrupt your GUI session. Always save your work before restarting any service, and only restart services if you have a specific need or understanding of why you're doing it._**

## Open

The open command is a quick way to open apps, websites, and more. This is particularly useful if your dock is cluttered or if you're looking to streamline your workflow.

| Name                           |Command                                                              |
|--------------------------------|---------------------------------------------------------------------|
| Website                        | open "https://google.com"                                           |
| Single App                     | open -a "Safari"                                                    |
| Multiple Apps                  | open -a "Safari" && open -a "Mail" && open -a "Calendar"            |

## Osascript

Execute AppleScripts and other OSA language scripts. Osascript executes the given script file, or standard input if none is given. Scripts can be plain text or compiled scripts. Will work with any Open Scripting Architecture (OSA) language.

Syntax: osascript [-l language] [-e command] [-s flags] [programfile]

Here are a few examples of how to use osascript. Replace "Application Name" with the name of the application you want to target, like "Safari":

| Name                           |Command                                                              |
|--------------------------------|---------------------------------------------------------------------|
| Quit App                       | osascript -e ‘tell application "Application Name" to quit’          |
| Focus App                      | osascript -e 'tell app "Application Name" to activate'              |
| Empty Trash                    | osascript -e 'tell application "Finder" to empty trash'             |
| Restart w/o Confirmation       | osascript -e 'tell app "System Events" to restart'                  |
| Shut Down w/o Confirmation     | osascript -e 'tell app "System Events" to shut down'                |
