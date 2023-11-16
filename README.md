# Shredder - OSX Quick-Action for Total Deletion
This Shredder Quick Action for OSX will instantly shred any document or folder, removing it completely from your computer and bypassing the trash using the `rm -rf` command.

## WARNING
This quick action will instantly remove files or folders once you click the confirmation button. **There is no way to recover or reverse this action. Use cautiously, particularly when it comes to program or system files!**

## How it works

This quick action will enable the "SHRED" option in your OSX quick actions menu when you right click on a file or folder. 

It runs the following bash code in the background:

```bash
for f in '$@'
do
rm -rf '$f'
done
```

It also provides the user with a warning and confirmation dialog box, ensuring against accidental shredding of important files and folders.

## Requirements and Compatilibity

Tested with OSX 10.15 (Catalina) to 14.1 (Sonoma). Works on both Silicon (M Series) and Intel macs, all models.

## Installation

Download the workflow zip and unpackage anywhere on your mac. Double click the workflow file and confirm that you want OSX to install this quick action. 

You may also use the included `.wflow` and `.plist` files to build your own Automator workflow that incorporates a shredding action.

