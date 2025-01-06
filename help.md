Noise Commander 3DS Help
------------------------

Glossary
--------
Pad        One of the 12 or 16 large "Drum Pads"
           found at the bottom touch-screen.
C-Pad      Circle-pad. The analog stick at the
           top-left above the D-Pad
D-Pad      Directional pad.
L          Left shoulder-button.
R          Right shoulder-button.


About this help screen
----------------------
C-Pad      Scroll up/down
D-Pad      Up/down to navigate sections
D-Pad      Left/right to page
B          Exit


General:
--------
DPAD            Select different screens
Select + DPAD   Select different bottom screen
Circle Pad      Move cursor (Upper screen)
A               Do stuff
B               Cancel stuff / return


Project screen
--------------
Press the DPAD down to show the Project screen 
(at the top).

The project of the currently selected deck (A/B)
can be saved, loaded or a new project can be 
created.


Recording your performance to a wav file
----------------------------------------
The master audio output can be recorded to a wav
file. Select the "Record" menu-item and press A.
To stop recording press A again, it is a toggle.

"REC" will be displayed in the title bar, showing
the current length of the recording.


Loading samples via Twin Browser
--------------------------------
A      Open file-operation Dialog (or load sample)
B      Move to parent directory
Y      Switch to other side
X      Multi selection (not yet supported)
L / R  Navigate page-wise

Press the D-Pad down twice. You should see the
twin-file browser in the top screen.

Here you can simply navigate to a wav file and 
press A to load it.


Loading random samples (Categories View):
-----------------------------------------
A       Load x samples for the selected rows.
B       Select a single row.
X       Select multiple rows
Y       Show popup for browsing / renaming.
Start   Remove unused samples from memory.
C-Pad   Select rows and number of samples to load

A set number of randomly chosen wav-files can be
loaded from user-defined directories.

Samples must be 16-Bit mono wav-files stored on
the SD-Card. The app creates a "/samples" folder
for you during the installation process.

Press up on the DPAD until you are in the
"Sample Categories Vew".

You can choose 12 folders which can be assigned
to the individual instruments.

To assign a new directory, select a slot with the
C-Pad and press Y.
A popup-dialog appears. Choose "Directory".
Use the C-Pad to navigate.
Press right to enter a folder, left to move to 
the parent folder.
Press A to assign the selected folder to the
slot.

Each row in the Categories View displays the
number of samples currently loaded and an amount
to be loaded.

Press left or right on the C-Pad to change the
amount value.

Press B to select a single row or X to select 
multiple rows.

Press A to begin loading for all selected rows.

A progress bar appears in the title of the top
screen. The percentage of memory used is
displayed as "Mem" in the status column to the
right, and the total number of samples is 
displayed under "Smpl".

To assign a category to an instrument (pad), 
go to the Instrument screen and change the
"Category" value.


Setting the Tempo
-----------------
The tempo can be set in the Instrument View.
It is a button in the middle of the upper screen.
Use the C-Pad to select it, then press A.
It will open a popup-dialog.


Instrument / Pad screen
-----------------------
Pad             Play/Select sound
L + Pad         Erases notes while held
R               Select other Deck
Pad + C-Pad     Change value
Pad + Left      Select previous sound
Pad + Right     Select next sound
Pad + Up        Solo pad sound
Pad + Down      Mute pad sound
Select          Cycle slider pages
A               Execute selected button (if any)
A + C-Pad       Change value at cursor
B               Toggle pad mute state
Y               Play sound
X               Reset slider value

Touch pads to play their sound.

Enable REC and play the pads to insert notes into 
the sequencer.

Disable "Play" to select pads without playing 
them (found at bottom right side).

There are three types of selectable items in the 
upper screen:
Sliders, buttons and lanes (pads). 

To change a slider value, first select it and 
then do either:

A) Hold the A button while moving the Circle Pad.
B) Touch a pad on the lower screen while moving 
   the Circle Pad.

To execute a Button, just press A.

The A, X and Y buttons do different things 
depending on the cursor selection.

Pressing such a button while a lane is selected 
by the cursor will trigger an action which 
opererates on the lane (pad).

Pressing such a button while a slider is 
selected: (TODO: explain).

The second of the four bottom row buttons cycles
through several modes:

ROLL - Repeats notes in a short loop while pad
       is pressed.
       
SLICES - Plays the current sound at different 
         starting points.
         Can be recorded.
         
PIANO - Plays sounds in chromatic pitches.
        Can be recorded.

SAMPLES - Plays a different sample sound
          per pad (the first 16 samples).
          Can be recorded.

When the "Assign" mode is on, the selected
action is assigned to the A, X or Y button when
pressed. This is useful to repeat a frequently
used actions.

The assignments are currently not yet saved
and will revert when you re-open the app.

This will change in the future and more
assignable combinations will be available.

The "Ln All",  "Ln Bus" and "Ln Sel" modes at the
right side set the lane-context for certain 
actions.
This is currently only supported by the sample-
selection actions.

The "Intrupt" function will temporarily mute
all other lanes and unmute them again at the 
next bar when you play a sound.


Grid Editor / Pattern screen
----------------------------
UPPER SCREEN

C-Pad            Moves the cursor (upper screen)
B + C-Pad        Moves 8 steps at once.
A                Inserts or removes a note at the
                 cursor (toggle)
B                Plays current sound
Y                Mutes current lane (toggle)
X                Solo current lane (toggle)
L                Clear all notes in current lane
R                Select other deck (A/B).
L + C-Pad up/dn  Select lanes and clear them 
L + C-Pad side   Rotate notes
R + C-Pad side   Select bar focus 
                 (if auto-follow is disabled)

LOWER SCREEN

Crossfade        Sets the volume ratio between
                 Deck A (left) and Deck B (right)
                 
Rand             Selects a random sample
Follow           If enabled, the upper screen
                 shows the currently playing bar.
                 Only the a single bar is viewed
                 when this option is disabled.
Rand All         Selects random samples for all 
                 lanes.
                 
Pattern Matrix   Selects a pattern when the next
                 bar pays.
Select + Pat     Selects a pattern immediately
R + Pat          Copies the current pattern to
                 a new slot and selects it.
                 

Parameter Automation
--------------------

Press Start in the Grid Editor screen to see
the automation editor.

This is currently extremely crude and only allows
setting a value for the currently selected column
by sliding up or down with touch.

The animatable parameters are:
Volume, Note length, Slice Index, Sample Index


Recording audio from microphone
-------------------------------

1. Find and select the "FromMic" button in the 
Instrument view.

2. Press A and hold it to record.

3. Release A to stop recording.

The new sample is immediately assigned to the 
current instrument lane to play with.

Clip Matrix View
----------------

Press up on the DPAD to see.

Active cells are displayed in green.

A cell that is about to launch pulsates in green.

When multiple cells refer to a shared phrase 
number, their color becomes red.

A single cell can be copied by pressing B while 
selected. Pressing B after selecting another cell will 
paste the value again.

 CPAD       Move cursor
 A          launch cell (phrase)
 B          Insert last value to cell
 B + CPAD   Change cell values (phrase)
 B +A       Launch row
 X          Cycle selection modes (cursor / all tracks)
 Y          Open menu
 Start      Toggle between editing phrase numbers 
            or clip length
 Select     Toggle row continue
            Off: Repeat the current row clip
            On: Play next row of island

Menu:

 Insert Row         Inserts a row ABOVE the 
                    currently selected row|
 Delete Row         Deletes the current row
 Copy               Copies the rectangular 
                    selection
 Paste              Pastes the rectangular 
                    selection at the cursor
 Rotate             Not yet fully implemented
 Duplicate          Same as copy & paste to next 
                    row
 Toggle continue    Cells normmaly cycle 
                    downwards but repeat the 
                    current when this is disabled
 Capture as new     Enters currently playing 
                    phrase numbers to the current
                    row (override)
 Insert next free   Finds and insert the next 
                    unused / empty phrase number 
                    to the current cell
 Make unique        Copies every selected phrase 
                    into a unique slot to allow 
                    editing non-destructively 
                    afterwards (de-dupe)
 Make instr unique  Clones the instruments used 
                    in the selected phrases to 
                    allow editing 
                    non-destructively afterwards
 Remove duplicates  Opposite of make unique, 
                    replaces all phrases which 
                    have identical content
 Duplicate uniquely Duplicates the current row 
                    and makes both, phrases 
                    and instruments unique

Tracker View
------------

Press right on the DPAD to see.

The top row displays the lane number and the 
column abbreviations. The full column name is 
displayed in the status-bar at the bottom of the 
top screen when a column is selected.

Columns are only selectable when the "Column 
select mode" is enabled.

A single cell can be copied by pressing B while 
selected. 
Pressing B after selecting another cell will 
paste the value again.

**Tip**: Press Select + DPAD right to show the 
Pads view on the bottom screen with the tracker 
view at the top screen.

Now you can use the pads or the piano to insert 
notes to specific locations. Make sure that the 
pattern follow mode is off (A) and REC is 
enabled.

 A          Toggle playhead follow mode
 B          Insert last value or escape selection
 B + C-Pad  Change cell value
 B + A      Clear cell value
 B + X      While held, C-Pad changes note length
 X          Cycle selection modes
 Y          Open menu
 
 L          Toggle compact mode (only notes)
 A + B      Set note length to cursor
 A + C-Pad  Up/Down shift cell(s)
 A + D-Pad  Left/Right moves the lane (reorder)

Menu:

 Copy         Copy selection
 Paste        Paste selection
 Cut          Copy and clear selection
 Duplicate    Copy and paste selection to next row
 Interpolate  Fills gaps between every value in 
              the selected columns with 
              interpolated values
 Insert linear slices   Adds slice notes to
                        current lane
 Randomize slices   Changes ALL slice values
                    in the current lane

Tracker companion view
----------------------

This view is a very crude placeholder and needs 
to be fleshed out or replaced in the future

Allows setting the current clip- and phrase 
length.The phrase loops for the duration of the 
clip length.

Buttons:

 Follow   Same as pressing A, toggles cursor 
          following phrase playback
 Cmpct    Same as pressing L toggles compact mode
 SlCol    Toggles ability to selected individual 
          columns, else only lanes are selectable
 Loop     Does nothing, not implemented, apologies
 Mouse    Allows moving the cursor like a mouse or 
          trackpad. Use the CPAD at the same time 
          to nagivate even faster
 Pinst    Selects any instrument the cursor comes 
          across during playback
 Ginst    Selects any instrument the cursor comes 
          across while navigating
