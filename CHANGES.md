# eTktab revision history


## 1.0 (initial revision--changes from tktab->eTktab listed)
* changed file dialogs
* added cut/paste
* added embellishment code
* added emacs tablature mode key bindings
* added code to change guitar's tuning
* added new ways to move around in tab
* added dialog when quit without saving changes
* made dialog windows transients
* made window contents follow when screen moves


## 1.1
* added -b flag for bass mode ( 4 strings, not 6 )
* added 's' embellishment for slap/pop of a note
* cleaned up codebase and added comments


## 2.0
### CLEANUP:
* misc. cleanup:  changed variable, window, and proc names, rewrote some cruft
* cleaned up a handfull of bugs
* added key bindings for buttons in alert windows
* alert windows placed at center of parent window
* added code to limit resizing of certain windows
* changed behavior of many procs if some tab is currently highlighted
* made adjustments to code surrounding current directory for file I/O
* *****CHANGED FILE FORMAT** (see [README](ReadeMe.md)</A>)
* 'lead mode' now inserts in front of pre-entered tab
* mod's to behavior of space and insert keys
* many changes to button bar
* some speed ups of various proc's

### NEW FEATURES:
* 'open' now automatically adjusts to bass or 6-string mode of loaded file
* can now move, copy, paste via mouse
* can now have multiple tab windows up at once
* can now paste into other running eTktab windows
* can now paste into other applications
* added undo/redo feature
* added 'repeat' marks on bar lines
* now windows/mac compatible; makes some adjustments to each platform


## 2.1
* changed 'alt' key to 'option' key in macintosh version
* Shift-[1-6] inserts at fret 0, ignoring the current 'base fret'
* changed tablature font size in MS Windows


## 2.5
### CLEANUP:
* Changes to tab drawing proc's
* Created some 'mega-widget' procs
* more use of standard tk dialogs
* menu changes (multiple columns, separators, keyboard accelerators)
* 'ghosting' menu options via 'disable', instead of changing colors
* cleaned up help window formatting
* more generalized creation of 4/5/6 string modes (easier to add more modes)
* clearer use of arguments to various proc's
* allow cut/paste between eTktab windows in different eTktab processes in Unix
* other miscellaneous stuff
 
### NEW FEATURES:
* added alternate keybinding support
* added alternate language support
* added 5 string mode
* added user-preference code (fonts, colors, formatting, tunings, initial document type, initial window size)
* added up/down,pgup/pgdn,home/end keybindings to help window
* added bend,release,tapping,muted note modifiers (program now includes all note modifiers referenced in alt.guitar.tab FAQ)
* added 'new line of tablature' function, bound to Return key
* added formatting info. to documents, yet still backwards compat.
* added keybinding for select-all
* **removed 'Meta' keybinding** for Unix (now only Alt)
* **changed keybindings for repeat symbols** to be CMD-; for both right and left
* **changed keybinding for 'change chord/lead mode'** to tab key
* changed behavior of 'new_tab' keybinding to work off preferences, instead of current doctype
* removed unix '-b' flag, in favor of user's preferences
 

## 3.0
### CLEANUP:
* Code additions and alterations for Mac OS X (Aqua) native version
* Found bug that made paste button unavailable inappropriately
* Much cleanup of quirks in highlighting of selected tablature
* More efficient (faster) coding of drawing window contents
* added up/down arrow buttons to alter some values in pulldown menus
* fixed a bug in altered tunings in saved files
* Changed appearance of mouse pointer in certain situations
* Rewrote much of README file

### NEW FEATURES:
* Lyrics editing mode
* Added document printing
* Added menu of open windows
 
## 3.1
### CLEANUP:
* Fixed bug with reading files from older versions
* Fixed bug when using pgdn key at end of document
* Fixed bug causing eTktab to ignore formatting info. in files
* Fixed bug causing wrong keybindings after opening a file, in some situations
* Fixed bug regarding backspace key in lyrics mode
* Mouse clicks now place cursor more accurately in lyrics mode
* Fixed bug regarding bad behavior when trying to run a second eTktab process in MS Windows
* Added extend/paste mouse bindings in lyrics mode
* Added a verification dialog when reverting preferences to defaults
* New MS Windows installer
* Fixed Mac OS Classic not being default app for 5-string tab files
* **Thanks for the bug reports!!!!**
 
### NEW FEATURES:
* Added 7 string tablature mode
* Added named presets to tuning window, editable in user preferences


## 3.2
### CLEANUP:
* Lyrics/tab mode now switches automatically, in response to mouse clicks in tab scores or 'textboxes'
* Can now click on end of textbox symbol to go into that textbox
* In lyrics mode, "current position" color now only added to the textbox that contains the cursor
* Focus now follows cursor for left/right cursor key
* Menubuttons now keep consistent size, where possible
* Fixed bug in internationalization code, regarding 'Save' in File menu
* Return key uses new feature, listed below to insert whitespace, rather than blank tab positions to end of line
* Macintosh Classic and OS X now have File, Edit, and Help menus exclusively in the Mac Menubar (rather than the window statusbar)
* Many OS X bugfixes, due to upstream cleanup in tcl/tk 8.4.5
 
### NEW FEATURES:
* Blank spaces may now be added to tablature (using whitespace in tab makes files unreadable by versions older than 3.2)


## 3.21/3.22
* Releases for ***Mac OS X* ONLY**
* 3.21: workaround for OS X dialog button bug, and changes to printing interface
* 3.22: workaround for OS X menu accelerator bug
 
### KNOWN BUGS: (see readme)
* OS X: some buttons not drawn
