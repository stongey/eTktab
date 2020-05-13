# eTktab
Copied from sourceforge repository in order to preserve some changes I made for running from the Terminal on my Mac. All credit to the original authors. Original ReadMe below.

NB - I tried to contact the original author at the email address in the ReadMe, but the email appears to be a dead account.

This repository does not include the binaries that are available for download in the original sourceforge repository. I was unable to get the Mac binary to work.

I have tested and run the UNIX tcl/tk code on my Mac 10.13.6 (High Sierra) with some very minor modifications to the code.

tcl/tk 8.0 or greater must be installed. On a Mac, the easiest way to do this is to use Homebrew: ```brew install tcl-tk```.

Then double-click on the [eTktab](eTktab) file to launch the program.

----

# eTktab
Author: Jason Sonnenschein
http://etktab.sourceforge.net
Email: jes_jm@yahoo.com

Please read the [License](License.md) for this program.


## Thank You's/Credits:
This program is used to write out guitar tablature in the typical style of ascii tab, often found around the internet. The code is based on TkTab by Giovanni Chierico. Many of the ideas for the alerations found here came from emacs tablature mode by Mark R. Rubin. Windows printing handled by Peter Lerup's [prfile32](http://www.lerup.com/printfile). Guitar icon by Sandy at [Around the Pixel](http://www.aroundthepixel.com). Mac OS X icon by Tomoyuki Miyano at [IronDevil](http://www.din.or.jp/~irondv/). Windows and Mac binaries were created with Tcl/Tk wrapper programs--Drag & Drop Tclets and Freewrap.

----
## Special Notes:

Some keybindings changed between version 2.1 and 2.5 to make room for new features. **NOTE: All keybindings specified in this file are true for U.S. keyboard ONLY** and are merely here to illustrate how to use the program. Look at eTktab's help window after loading a keybindings file appropriate to your keyboard.

The program will initially run with English and United States keyboard support.
To change the language support or keybindings, do the following:

1. Download alternate language and/or keyboard definitions from the eTktab website (or create your own, by editing one of the available files)
1. Place the files in a known place on your system (preferably where eTktab resides)
1. Run eTktab
1. Select the menu entry 'Edit->Preferences->Language'
1. Locate the downloaded .etl file on your system
1. Select the menu entry 'Edit->Preferences->Keybindings'
1. Locate the downloaded .etk file on your system

## Files Saved in Version 1:
The file format changed from version 1 to version 2. eTktab version two will no longer read or write version 1 files. You can convert files with the included script (```fileconvert-v1-to-v2```.)

----

## Running eTktab

When eTktab is run without an initial document, it will start with an empty document. The initial document may be for a 4, 5, 6, or 7 stringed instrument, depending on your 'preferences' settings. New windows pulled up via keypress will also conform to this default. The menus allow new documents of any type.

* On *Unix* machines, an initial file may be loaded by putting the filename on the command line.  
* *Macintosh* and *Windows* users can double-click on a document to bring up eTktab with that document.  


## Entering Tablature

There are two cursor modes when entering tablature. These can be toggled via menu or keypress. In 'lead' mode, the cursor is advanced after each note insertion, and tablature to the right of the cursor is pushed along ahead of the newly inserted tab. 'Chord' mode will **not** move the cursor. You will have to advance the cursor manually, after you have entered all the notes in the current chord.

In 6 string mode, there are 30 different keysrokes that will put a note into the tablature. The system they follow is difficult to explain clearly, but easy to use. It mimics the way a guitarist plays. 24 of the 30 keypresses are relative to where a 'vitual hand' is positioned on the fretboard. The program refers to where the hand is as the 'base fret.' The base fret can be changed with the + and - keys, or via menu.

Below are two example charts of the keys on a US keyboard. One is for 6-string mode (guitar,) one for bass. Think
of these charts as a guitar neck, laid over part of your keyboard. The string names are along the top of the chart. The fret numbers are along the left side. Inside the chart are the keys that correspond to various places on the fretboard, according to column (string) and row (fret.)

```
          STRING (guitar)                         STRING (bass)

            E A D G B E                             E A D G
          +-------------+                         +---------+
F  base+0 | 1 2 3 4 5 6 |               F  base+0 | 1 2 3 4 |
R  base+1 | q w e r t y |      OR       R  base+1 | q w e r |
E  base+2 | a s d f g h |               E  base+2 | a s d f |
T  base+3 | z x c v b n |               T  base+3 | z x c v |
```

For example: the 's' key inserts base+2 on the A string.  If 'base fret' is currently set to 5, then pressing the 's' key will put a '7' on the A-string (base+2 is 7 when the base fret is 5.) If you changed the base fret to 12 and pressed the 's' key again, it would now insert a '14' (base+2) on the A-string.

Pressing Shift when using a key in the first row will cause it to 'ignore' the base fret and insert a fret 0 (open) note on that string... So, Shift-3 will add a '0' on the D string, no matter what value the base fret is currently set to. These keystrokes are convenient when tabbing music with notes high on the neck, interspersed with open-string notes.

Note alterations, such as hammer-on and pull-off, may be added and removed from any note. All their keybindings are Alt-<something> (Option on *Macintosh*). Two modifiers are allowed on bar lines... they are left repeat and right repeat. Notes may only have one modifier, but bar lines may have both left and right modifiers simultaneously.

The tuning of the stringed instrument is changed with the tuning dialog. It can be pulled up via the Tuning button, or a keyboard shortcut (typically ';').

## Editing Tablature
Most users will highlight, cut, and paste using the mouse. Bindings for the mouse should perform as you would expect for your system... On all systems, you can use the left button to move the cursor, or highlight regions of tablature. On *Windows* and *Macintosh*, shift-left button extends the highlighted region. On *Windows*, right button will paste. On *Unix*, right button extends the highlighted region and middle button pastes. Note that mouse clicks need to be within a line of tab. Clicks in the blank spaces between lines are ignored.

Region highlighting is also available via keyboard, by setting a 'mark,' then moving the cursor. The same keystroke is used to set and unset the mark.
 
Cut/paste between documents will only work if they are the same type (same number of strings.) Tablature pasted into other programs (word processors, email, etc.) only looks right in **non-proportional** fonts, such as Courier.

An 'undo/redo' feature was added in version 2.0. It remembers 10 steps. Remembering more steps means using more memory. If you have the source... tune as you see fit.

The remaining key bindings are explained in the help screen, which may be called up with the help button at the top of the window, or by hitting '?' or Control-h (Command-h on *Macintosh*).

## Lyrics Entry/Editing
Lyrics may be added and edited by selecting Lyrics in the 'Mode' menu. There are textboxes at the beginning and end of the document and immediately below each score of tablature. The end of each textbox is marked with the section symbol (§). This symbol will **not** show up in cut/paste or printing of lyrics. In lyrics mode, the keybindings for things like saving, printing, etc. still work, but other keys now just insert that character in the window (as in any simple editor.) The user cannot edit any of the tablature while in lyrics mode, and selecting text for cut/paste can not go beyond the boundary of a text box. The PageUp and PageDown keys will move the cursor from one textbox to another. Other cursor movement should work as expected.

## Saving, Exporting, and Printing Files
The 'Save' feature will save files in eTktab's native file format. This is the only format the program can load. Use the 'Export' feature to create a text file of the tablature as it appears on the screen for use in email, newsgroups, etc.  Exported tablature will only look correct in a **non-proportional*** font, such as Courier.

For all platforms, printing is made possible by external helper programs. *Windows* printing is handled by ```prfile```. The file ```prfile.ini```, in the eTktab directory, controls its settings when working with eTktab. *Macintosh* printing is handled by the Unix printing command ```enscript```, and is only available on OS 10.2 and above (as ```enscript``` is not available, or does not work correctly on lower OS revisions.) *Unix* users may choose the command line for their favorite external printing program.

## Bugs
The *Macintosh OS X* version has some known bugs that cannot be fixed at this time. Sometimes a button will not be drawn in dialogs, until the mouse moves over them. Further, keyboard accelerators are not drawn in the file and edit menus. If you are interested in tracking down these bugs, please help out the [Tk toolkit](http://www.sourceforge.net/projects/tktoolkit) project.
