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
Start           Starts or stops playback (toggle)


Rotary sliders
--------------
Rotary sliders are manipulated by moving the
finger/stylus around the center of the bottom
screen.

Clock-wise to increase the value and anti-
clock-wise to decrease the value.

While touching, pressing LEFT on the D-Pad
toggles a coarse-snapping mode that can help
setting sane values for the track's length
(multiples of four) quickly.


Project screen
--------------
Press the DPAD down twice to show the Project 
screen (at the top).

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


Twin Browser
--------------------------------
A      Load/Execute file (song, wav etc.)
B      Move to parent directory
Y      Switch to other side
X      Show file operation menu (copy etc.)
L / R  Navigate page-wise
Select Cycles through panel-types

Press the D-Pad down once. You should see the
twin-file browser in the top screen.

Here you can simply navigate to a wav file and 
press A to load it.

Songs can be loaded the same way.

CIA files can be installed this way too.


Playlists
------------------------------
Playlists can be created via the browser
file operation menu.
The copy operation can be used to add entries.

Holding A allows to move the selected entry
up or down.

Pressing A loads the selected song entry.


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
B + C-Pad       Cycle slider pages
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

INSTRUMENTS - Assign different instruments to
              pads with different values for
              pitch, volume, Slice, Sample
              and Lane.
              See "Instrument Palette" section
              for more information.

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

Rand All         Selects random samples for all
                 lanes.

Instrument Palette
------------------

This screen let's you assign different
instruments to each of the 12 pads and / or
assign variations to these values:
- Instrument number
- Note (semitones)
- Volume
- Slice number
- Sample number
- Lane (track) to play on

You can find the instrument palette inside the
lower pad-screen and open it from the menu which
appears when pressing the second button from the
bottom left.

Shortcuts while holding a pad:

Pad + D-Left: Decrement instrument number
Pad + D-Right: Increment instrument number

Pad + D-Up: Start dragging a pad
   When touch is released before D-Up then
   a pop-up menu offers three operations:

   COPY - Copies the dragged pad
   SWAP - Exchanges the dragged and and dropped
   CLONE - Clones the instrument to a free slot

   When D-Up is released first then the last
   operation is repeated without showing the
   pop-up menu.

Pad + D-Down: Shows the edit-menu
   Here you can edit the Note, Volume etc.
   A sound-preview is played Every time you change
   a value.
   Press B or D-Down again to close the menu.

Cloning instruments allows you to make further
variations like different loop-points or
envelope settings etc. and record a performance.

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
 AA         Launch entire current row
 B + A      Launch entire current row
 B          Insert last value to cell
 B + CPAD   Change cell values (phrase)
 X          Cycle selection modes (cursor / all tracks)
 Y          Open menu
 L          Toggle between editing phrase numbers 
            or clip length
 Select     Toggle row continue
            Off: Repeat the current row clip
            On: Play next row of island
 Start      Toggle playback     
 

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

Values are inserted and changed by holding B
and moving the Circle-Pad.

Columns are only selectable when the "Column 
select mode" is enabled.

A single cell can be copied by pressing B while 
selected. 
Pressing B after selecting another cell will 
paste the value again.

You can use the pads or the piano to insert 
notes to specific locations. Make sure that the 
pattern follow mode is off (A) and REC is 
enabled.

There are 12 regular lanes, 4 Bus-lanes and one
master lane.

 A          Toggle playhead follow mode
 B          Insert last value or escape selection
 B + C-Pad  Change cell value
 B + A      Clear cell value (twice for row)
 B + X      While held, C-Pad changes note length
 B + Y      Insert note off
 X          Cycle selection modes
 Y          Open menu
 
 L          Toggle compact mode (only notes)
 R          Switch deck selection
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
 Clear Phrase Deletes all notes & events
              of the lane to start fresh
 Insert Note Stops can help to prevent notes
              from previous pattern to play
 Double content length increases the phrase
              length and copies the first 
              halve into the second
 Halve content length does the Opposite
 

Probability trigs (chance):

 Note can be suppressed by a random chance by
 entering numbers in the % column:

 When the first digit is zero then the second
 digit represents a percentage, i.e.
 05 means 50% and so on.

 When the first digit is non-zero then the
 note is played x out of y times.
 14 means play only the first time out of
 every four cycles.

Fades:

Certain columns of the lanes allow for
long fades with this set of commands which
can be inserted by holding B and pressing
UP/DOWN on the D-Pad:

(I) - Fade In
(O) - Fade Out
(U) - Fade Up
(D) - Fade Down
(T) - Set Limiting Target
(S) - Stop fading

Columns which support fade commands:
- (CV) : Channel Volume
- (B1) : Bus Volume
- (FC) : Bus Filter Cutoff

The values are in step (32th) units.
Larger values result in longer fades.


Selection:

Tap Y once to select a range within the current
lane. 

Tay Y again (e.g. twice) to select a range
for all lanes.

Holding B and moving the circle pad changes
the values of all selected cells.

Holding A + circle pad UP/DOWN shifts the 
selected cells.

Holding Y and pressing UP/DOWN on the D-Pad
selects everything above or below.


Pitch Slides (Portamento):

When a row has a note-value without an
instrument-value (IN), then the pitch will
slide gradually to the new value.

The speed-rate is determined by the "PSlide"
value of the instrument or the "GL" column-
value in the same row.


Lane Columns:

Parameters can be automated by by inserting 
values into their respective columns.

Columns can be shown or hidden by pressing
B + D-LEFT and toggling items in a menu.


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


Uploading samples/files through a web-browser
---------------------------------------------
Find and press the "Upload" button in the
instrument view.

Enter the shown ip-address into your browser on
a PC or mobile phone.

Here you can either drag and drop a single file
or click "Choose File" and then click "Upload".

The upload-directory depends on the file-type.
wav and zip files go to "/nc/samples"
cia files go to "/nc/cia"
any other file goes to "/nc/upload"

Zip-files are automatically extracted into the
"/nc/samples" directory

In my tests chrome was a lot faster than firefox.
Uploading and extracting files can be fairly slow
but may be quicker or more comfortable than
physically moving the SD-Card to a computer.

The 3DS file system implementation is slow
when dealing with many files, such as a
sample-library.

A modern USB-3 SD-Card reader may be the best
choice if you have a lot of files after all.

This feature is intended to be used in your
local Wifi network and has no security in mind
whatsoever, you may not want to use it in a
public network.


Waveform view
---------------------------------------------
Press right a few times to see the waveform-
view. It displays the currently active sample.

Touch     - Moves the cursor
A         - Plays sample from cursor position
C-Up/Down - Zooms in/Out
C-Left/Right - Pans the view when zommed
X         - Trims cursor-left audio
Y         - Trims cursor-right audio
