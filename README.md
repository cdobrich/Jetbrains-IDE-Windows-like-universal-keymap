# Windows-like IntelliJ keymap for macOS

## TL;DR

Take the file <https://github.com/cdobrich/windows-like-intellij-keymap-for-macos/blob/master/Windows-like%20for%20macOS.xml> and place it inside "~/Library/Application Support/JetBrains/\<IDE-NAME>/keymaps".

## Overview

A node script to generate a Windows-like keymap for all of your JetBrains IDEs on macOS, based on the Windows default keymap for IntelliJ IDEA Community Edition combined with a little sensibility from Windows VSCode whenever unsure. This is for when you have already memorized many of the shortcuts on Windows and you have recently migrated to macOS, to do iOS development for example.

The IntelliJ default keymap can be found here: <https://github.com/JetBrains/intellij-community/blob/master/platform/platform-resources/src/keymaps/%24default.xml>.

Please note that this project assumes your keyboard is of the Windows layout, where the bottom row starts with "Ctrl -> Win -> Alt". Alternatively with a Mac keyboard layout, take a keyboard where the bottom row starts with "Ctrl -> Option -> Cmd" and swap the Win and Alt inputs using the OS or Karabiner-Elements.

The script performs three main tasks:

-   Updates every shortcut using the Alt modifier to use Command instead. Where there are conflicts, the shortcut is either removed, unchanged, or ported from the [Mac OS X 10.5+ IntelliJ keymap](https://github.com/JetBrains/intellij-community/blob/master/platform/platform-resources/src/keymaps/Mac%20OS%20X%2010.5%2B.xml).
-   Replaces the Insert key with the Help key. Insert on a full-sized keyboard is interpreted as Help on macOS.
-   Adds additional shortcuts which are common on macOS, such as Cmd+X/C/V to Cut/Copy/Paste, Cmd(+Shift)+Z to Undo/Redo, Alt/Ctrl+arrow keys to navigate to the start/end of words or lines, and more.

Because all JetBrains IDEs are based on IntelliJ, the keymap should be compatible with all of them, including WebStorm and Android Studio. However, you may want to make small adjustments to the keymap afterwards for some shortcuts unique to specific IDEs.

## Run it yourself

Method 2: Clone, build, run

```
git clone https://github.com/cdobrich/Windows-like-IntelliJ-keymap-for-macOS
yarn        # install dependencies (also runs `yarn build` to build the project)
node .      # run the main script
```

# Keyboard Shortcuts / Keys / Hotkeys

You have made your own custom Jetbrains IDE keymap file. Grab it from your own repository:

	https://github.com/cdobrich/Windows-like-IntelliJ-keymap-for-macOS

(On Mac) Menu: Pycharm -> Preferences -> Keymap

# Installation

Install Locations:

	MacOS:

		Syntax: ~/Library/Application Support/JetBrains/<product><version>/keymaps
		Example: ~/Library/Application\ Support/JetBrains/WebStorm2021.3/keymaps

	Linux:

		Syntax: ~/.config/JetBrains/<product><version>/keymaps
		Example: ~/.config/JetBrains/IntelliJIdea2021.3/keymaps


To install:

	1. Close the Jetbrains application.
	2. Copy the file .XML file to the appropriate target location.
	3. Start the Jetbrain application.
	4. Select the Keymap.


# Keyboard Shortcut List Modifications from Mainline

@tags: keyboard, keystrokes, hotkeys, shortcuts

NOTE: The 'Meta' is 'Cmd' key on MacOS and is the same as the 'Win' key on Windows-Keyboards.

Add All Imports: Alt + Shift + Enter
Auto-Indent Lines: 
	Meta + Alt + 0
	Ctrl + Alt + I
	Meta + Alt + I
Code Completion: Ctrl+Space
		To complete methods, keywords etc.
		This will also assist with autocompleting Interfaces.
	** Complete Current Statement: Ctrl + Shift + Space
	** Second Basic Completion: Meta + Ctrl + Space
	** Type-Matching: Ctrl + Shift + Space
Code Indent -> Convert to Spaces: Ctrl + Alt + S
Comment Line Toggle: Ctrl + /
Complete Code (Snippet Insert): Ctrl + J
Delete Line (Cut to Paste Buffer): Shift + Delete
Duplicate Line: Ctrl + D
End (required for MacOS): Ctrl + Shift + End
Extend Selection: Ctrl + Shift + E
Focus Commits Sidebar: Meta + 0
	** Conflicted, does not currently work.
Focus Editor: Meta + E
	** Conflicted on KDE.
Focus Projects Sidebar: Meta + 1
	** Conflicted, does not currently work.
Git Branch Menu: Ctrl + Shift + `
Go Back in History: 
	Alt + [
	Meta + Ctrl + Left
Go Forward in History: 
	Alt + ]
	Meta + Ctrl + Right
Go to Line (number): Ctrl + G
Hide All Tool Windows: Ctrl + H
Highlight All Matches: Ctrl + Shift + L
Home (required for MacOS): Ctrl + Shift + Home
Imports Add All: Alt + Shift + Enter
Jump to Matching Bracket: See Matching Brackets
Matching Bracket: 
	Cmd + M (also known as Meta + M)
	Ctrl + [ (for previous)
	Ctrl + Shift + [ (for previous)
	Ctrl + ] (for next)
	Ctrl + Shift + ] (for next)
Maximize (Hide All Tool Windows): Ctrl + H
Move Caret to File End (required for MacOS): Ctrl + Shift + End
Home Caret to File Top (required for MacOS): Ctrl + Shift + Home
Maximize Window: 
	** See also Zen-Mode
Move Line Down:
	Alt + Down
	Ctrl + Shift + Down
Move Line Up:
	Alt + Up
	Ctrl + Shift + Up
Open Last Closed Tab: Ctrl + Shift + T
Optimize Imports: Meta + Ctrl + O
Paste Plain Text: Ctrl + Shift + V
Quick Switch: Meta + `
	** Conflicted on KDE, may not work.
Recently Edited Files: Ctrl + E
Reformat Code: Meta + Ctrl + Shift + L
Rename: Shift + F6
Run Any Command: Ctrl + Ctrl
	** Conflicted, does not currently work.
Search all filename and function names: Shift Shift 
Settings:
	Ctrl + Alt + S
	Ctrl + P
	Meta + ,
Show/Hide Sidebar: Ctrl + H
Show Context Actions: 
	Alt + Enter
		** May not work on MacOS.
	Meta + Enter
		** Conflicted on Linux. Probably works on MacOS.
Show Matching Bracket: See the 'Matching Bracket' command on this list.
Show Commits Sidebar: Meta + 0
Show Projects Sidebar: Meta + 1
Show / Hide Terminal: Ctrl + `
Split Editor Create Tab Window (Right): Ctrl + \
Split Editor Create Tab Window (Down): Mouse Menu
	** Close Split Editor Tab Window: Ctrl + W						# Like standard normal
Split Editor Tab Close (show Single): Ctrl + Shift + /	# NOTE: Custom set
Split Editor Jump or Switch Window Panel: Ctrl + 1      # Or Ctrl + 2, Ctrl + 3, etc...
Terminal Toggle Show/Hide: Ctrl + `
Toggle Open/Hide Terminal Console: Ctrl + `
Undo Closed Tab:
	Ctrl + Shift + T
	Meta + Shift + T
Zen-Mode (Hide All Tool Windows): Ctrl + H
