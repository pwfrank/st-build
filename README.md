# Simple Terminal
A simple, sensible build of the suckless.org Simple Terminal project.

A PKGBUILD is included for anyone in an Arch-based environment who wants to manage their installation via pacman. Anyone else can build directly from the src directory using make/make clean install

## General controls
Resize font: Control + up/k, Control + down/j  
Copy: ALT + c  
Paste: ALT + v  

## Patches applied
### st-clipboard
Keeps xorg clipboard and primary selections the same, regardless of whether copied by mouse selection or the clipcopy command. Note that this only affects selections made within st, other windows managed by X will still copy to the clipboard and primary selections separately

### st-keyboard_select
Adds a vim-like text selection mode that does not require the use of the mouse.

Enter mode: ALT + ESC

### st-scrollback
Allows scrolling upwards to view previous output

Scroll one line: ALT + up/k, ALT + down/j  
Scroll one page: SHIFT + PageUp, SHIFT + PageDown

### st-scrollback-mouse
Allows scrolling upwards using SHIFT + mousewheel

### st-xresources
Allows colors and terminal attributes to be set dynamically via an .Xresources or .Xdefaults file

## config.h additions
* keyboard_select mode entry keybinding
* ResourcePref array
* Added mkeys array and set mshortcuts array to XK_NO_MOD
* A more sensible default colorscheme
* various remapped controls