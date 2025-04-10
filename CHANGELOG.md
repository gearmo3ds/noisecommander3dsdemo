https://keepachangelog.com/en/1.1.0/

## 0.0.13

### Added
- Ability to start/stop playback by pressing the START button (play current row when in clipmatrix view)
- Doubled Master- and bus-effects so each deck has their own - uses more CPU
- Decks can be disabled in DJ-Mixer view to allow reducing CPU usage temporarily
- Decks are initially disabled until the user starts playack
- Rudimentary playlist functionality in twin-file browser
  - Press X and choose "New Playlist" in menu
  - With an *.nsm file highlighted, press X again and choose either "Copy" or "Add to Playlist"
  - Hold A + C-Pad Up/Down to re-order items inside the playlist
  - Press Select to cycle the panel-view-types: FILES -> PLAYLIST -> SAMPLES (not implemented yet)
  - Press A to load a song to the current deck as usual
  - Press B to exit back to files mode and show the "/nc/playlists" directory
  - The current playlist selection is persists, remembered during next app launch
- Browser: Visual scroll-bars appear in long lists to indicate paging is possible (press L/R to page)
- Browser: Pressing Y toggles deck selection
- Browser: new functions: Dulicate, Rename, Create directory, Jump to opposite dir
- Browser: The operations above support multi-selection but currently directories cannot be deleted or copied
- Browser: Multiple rows can be selected by holding X and moving the circle-pad up/down
- Header shows current deck's' loaded file name now

### Changed
- Doubled Master- and bus-effects so each deck has their own - uses more CPU
- Toggling display in clipmatrix has been re-assigned to the L button
- The right-hand status column now shows the currently playing row of track 1 
- Audio init error now shows instructions on dumping DSP firmware to fix it
- Browser: Switching side with circle-pad left/right now
- Browser: Cursor now stays in position when paging with L/R fore more comfort
- Browser: Pressing A when a .lst (playlist) file is selected opens it (switching to PLAYLIST panel type)
- Browser: Copying large files is now slightly faster
- Browser: Shows warning when attempting to load song into deck which it playing and audible (crossfader not off)

### Removed
- Opening a project or creating a project no longer auto-plays the deck (must press Start now)
- Start button no longer cycles pages in instrument view, use B+Circle pad instead.

### Fixed
- DJMixer view: Both "Deck Gain" sliders affect only the selected deck instead of respective side


## 0.0.12

### Added
- HTTP upload feature (button): User can drag a file into a served web-page to transfer it to the 3DS console
  - zip-files are automatically extracted to /nc/samples after uploading
  - Uploading via Firefox seems much slower than via Chrome
- Tracker + pads/piano screen combo, selectable by tapping D-PAD right twice
- Bus FX screen can be access by tapping D-PAD left twice
- New "Instrs" (palette ) mode - allows assigning instrument numbers to pads and record them to the current lane
  - Different numbers can be assigned by holding the pad and pressing left/right on D-PAD
  - Pressing Up on the D-PAD while holding a pad will start a drag session. A copy/swap/clone menu appears when dropping.
  - Pressing D-Down while holding a pad will show a menu for overriding certain values:
    - Pitch, Volume, Slice-number, sample-number and lane number

### Changed
- Ther user can no longer insert notes into phrase number zero
- Allow sliding touch on piano to trigger different notes (needed to re-tap before)

### Fixed
- Muting via B+Pad does not stop sample like PAD + Dpad-UP does

## 0.0.11

### Added
- Current octave is displayed in right-side status column
- B + Y inserts a hard note off value (in contrast A + B changes the note length to current row)
- "Tune to C" button in intstrument view - simple zero-crossing method, sometimes off by one note - not perfect
- Pop-up dialog for downloading demo-samples appears at startup if the samples directory is empty

### Changed
- Changed initial reverb default value from 10 to 0
- Matrix view displays phrase numbers in hex now and coarse edits offsets by 16
- Renamed "Pattern Settings" screen to "Mono to Stereo Settings" and remove redundant controls
- Hid obsolete Grid-Editor view and replaced "Assign" button with "Randomize all samples" button
- Double tapping A shortcut for row-launching in clip-matrix view
- Piano: Triggering notes by sliding is now optional and is initially disabled
  - It can be toggled by pressing DPAD UP while a touching any piano key
  - It's disabled by default because notes tend to double-trigger when playing quickly

### Fixed
- Shifting single note row with A+DPAD UP/DOWN does not work without selection sometimes
- Row lengths don't update when inserting or removing row in matrix view
- Bus-numbers display range started at zero, now starts a one
- Notes are still played when erasing notes with L + Pad
- Clearing a pattern un-assignes samples from instruments
- Avoid handing reserved sample, pattern or instrument with zero index to the user (adjusted related functions in code)
- Wrong tempo value shown in tempo-dialog

## 0.0.10

### Added
- Per-bus probability setting ("BChance" in Bus-FX view)
- Per-lane probability setting ("LnChance" in tracker bottome companion view)
- Per-note probability setting in tracker companion screen (Percentage column)
  - If the first hex digit is zero then the second number represents a percentage (1=10%, 5=50% etc.)
  - 0F ("First") is a one-off trigger, only fired when the phrase plays for the first time
  - If the first hex digit is non-zero then the trigger occurs every nth out of x times (x being the second digit)
    - e.g. "14" plays every first out of four times and so forth (the maximum is 8/8)
- Splash screen
    
### Changed
- Removed automatic insertion of note length in tracker editor
- Files are now sorted alphabetically in browsers
- The phrase length now updates to the total length of the four euclideans whenever a value is changed
- Added dynamic length toggle ("Len") button to second page in euclidean view (off by default)
  - When enabled, the clip length is set to the total euclidean length whenever a value is changed
- The "All", "Bus" and "Selected" lane mode buttons now behave as mutually exclusive radio buttons
- The Y-button now resets the selected parameter in instrument view
- A unique instrument is assigned to each lane's first clip when creating a new project
- Default template is created by code when no template.nsm file is found
- Follow- and narrow modes are now initially active by default in tracker view

### Fixed
- Deleting notes by holding L+Pad was broken
- Reverb-tail never ends due to fixed-point math (replaced with float for fix)
- Instruments not duplicated by "Duplicate Uniquely" if instrument column is empty in matrix view
- Note with no volume value should play at full level but was quieter (64 instead of 0x64)

## 0.0.9

### Added
- Support for loading 8-Bit wav files. Now we can load up to 128 bars worth of 24khz 8-Bit audio at 88 BPM (my default tempo)
  This equates to roughly 348 seconds per deck. There is 8 MB available for each deck. So ~700 seconds in total.
- "Insert linear slices" in tracker-menu. Places notes evenly in current lane
- "Randomize slices" in tracker-menu. Changes ALL slice values in current lane (selection). Should be useful for drum-loops
- "Clear phrase" option in tracker menu
- Replaced "Insert Row" with "Insert Row Above" and "Insert Row Below" options in matrix menu
- "Dup Ins" button clones current instrument into a new slot
- Ducking
    - Lanes can be defined as triggers by enabling the "TrgDuck" toggle in the instrument view.
    - The ducking effect can be enabled per bus in the bus-effects view.
    - The mix, rate and pause parameters are accessible in bottom-tracker widget
    - The ducking can be globally disabled in the bottom tracker-companion view
- Playhead in euclidean view
- Option to create a new instrument when loading a sample from the twin panel browser
- Experimental option to send a metronome click-sample to the right headphone channel. 
  - This is to sync with external devices but it requires something that can detect and convert
    onsets in the incoming audio to midi clock or a "real" audio pulse signal on the receiving side.
  - This means it won't work when plugged directly into a korg volca or similar.
  - I use a custom Axoloti setup for this but it could also be programmed as a raspberry pi or PC app.
- Can now load songs from the twin-panel file browser by pressing A

### Changed
- NumBeats now equates 4 beats to a bar for matching loops to the song tempo
- Selecting a row in matrix view also selects and displays the phrase in the tracker view
- Other pads are colored red when exclusive solo is active
- Notes with no value in volume column play at full volume
- The default pitch value in euclidean mode is now zero
- Instrument view: No more modes. Button B is now for muting instead of escaping
- Instrument view: Removed lane selection display from bottom to make room
- B + CPadLeft/CPadRight now cycles between the instrument view pages
- After loading a song, the first row is now triggered for playback to avoid silence

### Fixed
- Pop at the end of a sample playback due to mis-interpreted sample-length
- Send-effects still audible when bus-volume is zero (pre-fader)
  Changed to post-fader behavior as it seems what you normally expect
  A pre/post fader option should be added in the future in case it is desired
- Resampling only recorded half the amount of bars set
- Don't trip if resampled data contains no wav file header
- Cursor selection is lost when cycling instrument page by pressing Start
- File -> Reload was not working
- File -> Reload Seq was not working (Reloads only sequence data, no samples)

## 0.0.8

### Added

- Previously missing credits for BSD licensed Axoloti DSP code
- Ability to audition and load wav-files from the twin-browser into the current instrument
- Option to create a new category from the loaded sample, based on the directory name
- Octave +/- buttons in piano view

### Changed

- New Instrument creation dialog remembers last setting
- Clear samples from selected categories rather than all in categories view
- Added new "Touch-Grid" menu to bottom of drum pads screen for quicker mode selection.
  - The modes can be selected from a grid. Pressing the origin selects the previous mode again.
- Pressing DLEFT and DRIGHT now only changes the octave when the screen is currently touched.

### Fixed

- Triggering interrupt only works on current deck
- Triggering a muted pad during interrupt does not unmute it
- Every lane is unmuted every bar after using the interrupt function
- Interrupt function does not restore previous mute states
- Instrument loop-settings not always updated resulting in stuck loop mess
- Copy/paste/duplicate clips ignores lengths
- Interpolate function ignores selection
- Inserting a note off (pressing A+B) freezes the app when the track is empty
- Matrix rows above 12 are not displayed green as they should

## 0.0.7

### Added

- Added "New Ins" button to instrument widget.
  When pressed, the user must choose a sound category, then a blank instrument is selected.

### Fixed

- Making instruments unique replaced all instruments with zeroes in patterns
- Instrument loop settings not saved to file
- Clip Matrix: Select button toggles row continue mode (forgot to document previously)
- Function above now displays status message
- Prevent freeze when phrase is longer than 128 steps by limiting it to that length
- Added 5 seconds timout for date/time web call in installer
- Cannot select instruments with index larger than 127
- Triggering wrong row when matrix view is scrolled
- Made row-continue mode was not per deck
- Background of sample-file-name in instrument view not cleared causing glitchy display
- Changing instrument volume only applied when triggering pad but not from slider
- Instrument not assigned to phrase when made unique
- Live notes inserted to wrong location when phrase is longer than one bar
- Out-of-bound read when triggering sample on deck 2
- Pressing R did not switch deck in clipmatrix- and tracker views

## 0.0.6

### Changed

- Maximum amount of phrases per lane from 16 to 128
- Maximum amount of instruments from 192 to 256
- Instrument numbers now refer to a global list instead of per-lane to allow re-usage for chords.
- Install-directory name changed from "/noisecmdr" to "/nc" with the "samples" and "tracks" directories inside it to de-clutter the root directory.

### Added

#### Instrument view

- "HalveCurrentPattern" button (makes current phrases 50% shorter)
- "Connect" button: Allows streaming display to PC companion-app via local wifi 

#### Clip Launching Matrix view

Press up on the DPAD to see.

Active cells are displayed in green.

A cell that is about to launch pulsates in green.

When multiple cells refer to a shared phrase number, their color becomes red.

A single cell can be copied by pressing B while selected. 
Pressing B after selecting another cell will paste the value again.

|Press | Description|
|---|---|
|CPAD | Move cursor
| A | launch cell (phrase)
| B | Insert last value to cell
| B + CPAD | Change cell values (phrase)
| B +A | Launch row
| X         | Cycle selection modes (cursor / all tracks)
| Y | Open menu
| Start | Toggle between editing phrase numbers or clip lengths

|Menu Item | Description|
|---|---|
|Insert Row|Inserts a row ABOVE the currently selected row|
|Delete Row|
|Copy| Copies the recangular selection
|Paste| Pastes the rectangular selection at the cursor
|Rotate| Not yet fully implemented
|Duplicate| Same as copy & paste to next row
|Toggle continue| Cells normmaly cycle downwards but repeat the current when this is disabled.
|Capture as new|Enters currently playing phrase numbers to the current row (override)
|Insert next free|Finds and insert the next unused / empty phrase number to the current cell
|Make unique|Copies every selected phrase into a unique slot to allow editing non-destructively afterwards (de-dupe)
|Make instr unique|Clones the instruments used in the selected phrases to allow editing non-destructively afterwards
|Remove duplicates|Opposite of make unique, replaces all phrases which have identical content
|Duplicate uniquely|Duplicates the current row and makes both, phrases and instruments unique


#### Tracker view

Press right on the DPAD to see.

The top row displays the lane number and the column abbreviations. The full column name is displayed in the status-bar at the bottom of the top screen when a column is selected.

Columns are only selectable when the "Column select mode" is enabled.

A single cell can be copied by pressing B while selected. 
Pressing B after selecting another cell will paste the value again.

**Tip**: Press Select + DPAD right to show the Pads view on the bottom screen with the tracker view at the top screen.

Now you can use the pads or the piano to insert notes to specific locations. Make sure that the pattern follow mode is off (A) and REC is enabled.


|Press | Description|
|---|---|
| A         | Toggle playhead follow mode
| B         | Insert last value or escape selection
| B + C-Pad | Change cell value
| B + A     | Clear cell value
| B + X     | While held, C-Pad changes note length
| X         | Cycle selection modes (cursor / all tracks)
| Y         | Open menu
| 
| L         | Toggle compact mode (only notes)
| A + B     | Set note length to cursor
| A + C-Pad | Up/Down shift cell(s)
| A + D-Pad | Left/Right moves the lane (reorder)

|Menu Item | Description|
|---|---|
|Copy|Copy selection
|Paste|Paste selection
|Cut|Copy and clear selection
|Duplicate|Copy and paste selection to next row
|Interpolate|Fills gaps between every value in the selected columns with interpolated values

 - Selected cells can be shifted by holding A and pressing up or down on the d-pad
 
 - Without a selection, the current row is shifted, useful for nudging/fixing timing mistakes
 - Duplicating a selection will move the cursor and selection to allow repeating from there

 - Allow moving lanes with A + dpad left/right in trackerwidget

 - longer notes are succeeded by empty characters instead of "---"
 - Pressing A+B inserts a "note off" (changes the length of the previous note)
 - Holding B+X allows changing the note length with the C-Pad
 
 - Added Events::insertLengthToNextNote() and
   Events::findPreviousNoteRowIndex() methods.
 - Fixed broken test code
 - Now using the parameters default value when inserting to empty cell
 
#### Tracker companion view (bottom screen of tracker view)

This view is a very crude placeholder and needs to be fleshed out or replaced in the future

- Sliders allow setting the current clip- and phrase length. 
- The phrase loops for the duration of the clip length

|Button|Meaning|
|---|---|
| Follow| Same as pressing A, toggles cursor following phrase playback
| Cmpct| Same as pressing L, toggles compact mode
| SlCol | Toggles ability to selected individual columns, else only lanes are selectable
| Loop | Does nothing, not implemented, apologies
| Mouse | Allows moving the cursor like a mouse or trackpad. Use the CPAD at the same time to nagivate even faster
| Pinst| When on, selects any instrument the cursor comes across during playback
| Ginst| When on, selects any instrument the cursor comes across while navigating

#### Companion PC app (Qt5 based) 
PC companion app source code and linux x64 binary available on [GitHub](]https://github.com/gearmo3ds/noisecommander3dscompanion)

The 3DS screens can be displayed on a PC via local wifi.

#### Navigation Map

The current screen location is displayed by a small map on the upper left screen.

#### Rotaty Slider widget

This rotary slider is currently only used in the FX view and the bottom tracker-view.

Touching a slider will display a "Pac-Man" or pie-chart like graphic in the top screen.
Slide clockwise around the screen center to increase the value and anti-clockwise to decrese it.

- Pressing the D-Pad up or down while dragging a rotary slider allows changing the sensitivity.
- DPAD + left resets sensitivity to 1.0 and right toggles between two slots to allow setting a coarse and a fine value.

## 0.0.5

### Added

- Very basic pattern chaining in pattern select view, chain mode toggle and clear buttons
- Bar-buttons in lower grid-editor view which select bar to display or loop
- Loop-Bar button in bottom grid-editor view
- Experimantal effects-view (Press Select + DPAD down to show)
- Global tempo-synced delay effect 
- Per-bus fold distortion effect
- Per-bus delay- and reverb send parameters
- Per-bus low pass filter with cutoff- and resonance parameters
- Crossfading the individual buses is now possible
- Per deck gain parameter
- Record-source option in resample dialog allows choosing master (0) or a bus number (1-4)
- Notifications are now indicating when resampling starts and ends
- "Open Template" menu-entry in Project view loads "/tracks/template.nsm" if it exists
- "Open Recent" menu-entry in Project view showing the last 10 opened files
- "Restart" button in instrument view to allow manually re-syncing downbeat to other music by restarting the pattern
- Display of current/total pattern bars in right-side status column

### Changed

- Pattern now blinks when queued
- Cycle-selecting a new sample now plays the sample if in "Play" mode.
- Made lanes in upper instrument view non-selectable to avoid accidental changing.
- Pads with sample number zero are assigned a new random sample after loading new samples
- Optimized SSAT function for overall better dsp performance.
- Bus assignments and global swing amount now saved in file
- Hard-coded temporary attenuation of folding distortion
- The default category path is now an empty string insted of "/samples"

### Fixed

- Roll-length was offset in relation to the button labels (-1)
- Cannot switch deck with R when in Categories / DJMixer view
- Occasional crash due to stack overflow. Allocated more stack memory as a fix
- Resampling was allocating twice as many samples as needed, wasting memory

### Removed
- Omitted unused "All" mode in right side status column display

## 0.0.4

### Added

- Ability to record audio from microphone (16khz, 5 second max)
- "Interrupt" function: mutes all other lanes when user triggers a sound and unmutes them again at the next bar
- "Save Increment" option in Project View moves current file to backup directory with appended number before saving a new file

### Changed

- Soloing a lane now stops the samples on the other tracks
- Unique instrument numbers are now assigned to the empty patterns when initialized to avoid unknowingly changing shared instruments
- Current filename is displayed in save as dialog
- Adjusted "leap-size" for certain parameters, e.g. pitch is incremented by steps of 12
- Pressing X resets a selected slider to it's 'default value

### Fixed

- Cycling samples changed pitch even when numBeats is zero


## 0.0.3

### Added

- Added "NumBeats" setting in instrument widget
  - When greater than 0, the sample pitch is adjusted to match the tempo.
  - The pitches are updated when the user changes the tempo.
  - The "NumBeats" pitches are also updated when the user selects a different sample.
- Added tempo-dialog to instrument view
  - An additional fractional BPM value is now available
- Ability to control the amount of even sample slices for an instrument.
  - The value-range is 2-16.
  - When the slice amount is smaller than 16, the unused slices are shown in black and produce no sound.
- Added simple wav file loading support to the twin-browser

### Changed

- Server-side script (not the app) now queries patreon user-data every hour automatically to provide access to new users unattended.
- Instrument View: When the category/folder type is changed, a sample is immediately selected to reflect the change.
- Instrument View: Displays the current sample filename (only the first 16 characters).
- Tweaks to file-browser in "Categories View":
  - The current directory is now displayed at the top.
  - When moving to the the parent directory (left c/d-pad) it is now selected instead of the first.
  - The D-Pad can now be used to navigate page-wise.
  - Pressing B exits the browser.
- Help screen: The user can now jump between sections with D-Pad up/down.
  - Added information about sample loading and recording session as wav file.
- When the "Samples" pad mode is active and the right toggle is set to "Select", 
  then pressing a pad assigns that sample number to the current instrument.

### Fixed

- Selecting a "Category"-directory in the  "Category View" file browser had no effect.
- Now saving tempo in file and setting it correctly when loading a file.
- Tempo-fitting ("SyncLen") was misbehaving when it needed to slow the rate down (negative offset).
- Pressing Start and Select no longer quits the app in Release builds.
- The bottom row's buttons no longer react to touch-sliding over, this was prone to accidents and annoying.
- Issue where the mute mode got stuck after displaying a dialog 
- No color highlighting in samples/slices pad mode.

### Removed

- Removed redundant entries in Project View menu
- Removed stop-gap widget "Track Select"
- Removed a few unused sliders from second page of instrument view


## 0.0.2

### Added
- Help/Manual (text-only) appears when holding L+R.
- Added silent-select mode toggle to pads screen
  - Pressing pads does not trigger a an audible note in silent-select mode.
  - The second button from the left now cycles through alternate screen modes: Roll, Slices and Piano.
- Added function to unmute all tracks (found in upper screen)
- Added simple "Next bar" pattern change function
  - Touching a pattern in the pattern-select view will chain it so that the change happens at the occurence of the next bar.
  - Holding Select while touching switches immediately.
- Credits screen (Press Down in D-Pad twice to see)
- Added cutoff and fold-distortion parameters to DJMixerWidget
- Added very simple AutomationWidget
- GridEditor: Pressing start toggles between patterns and automation in lower screen.
- Vertical touch changes value of column which is selected in GridEditor
- Start no longer adds random euclidean sequence
- Added All- and Bus mode buttons. 
  - The Bus-mode applies an action to all lanes that have the same bus assigned as the current lane.
  - The All-mode applies an action to all lanes at once.
  - After enabling either mode, it is disabled by pressing B (think of it as an escape key).
  - Sample cycling and randomization support these modes now.
- Exposed Samplerate reduction effect in dj-mixer widget
- Progress-bar appears in title row when samples are loaded
- Global swing setting (could later be per track if needed)
- New Euclidean widget with visualization and touch (open through action in instrument view).
- Gated mode which uses Note-off to play as long pad is held. Find it in the instrument view.
- New resampling dialog in instrument view.
- Added very crude Twin-File browser for copying or deleting files.
- Added sample-trigger mode to perform widget. 
  - It allows triggering different samples than the assigned one, by playing 16 pads.
  - Supports recording and deletion of unused samples.

### Changed
- Categories View: All are selected by default
- Brought bus volume sliders back
- Made categories screen the first when pressing up
- Allow changing values with C-Stick while touch is held
- Allow erasing notes by holding L + pad in pad mode
- Empty patterns now appear as darker color in the pattern select view
- Pads: Sliding to a different tile now re-triggers it
- Sliding a pad to a different tile mutes it if the A button is held
- Holding a pad and pressing the dpad up solo solos it, down mutes it, left/right selects sample.
- The left/right DPad buttons in piano mode now select the octave
- Increased pitch-rise range by factor 5

### Fixed
- Drum pads flashed when either deck triggered a sound. Now only the selected one flashes
- Sluggish crossfade-slider in GridEditorCompanion due to double event firing
- GridEditorCompanion-Pushbuttons had stopped working
- Copying a pattern switches deck selection
- Selecting a random sample did revert selected bus-assignments to the settings stored in the category.
- Euclidean mode ignores intstrument pitch
- Euclidean mode fills only the first 32 steps
- Don't allow loading samples again while already in progress

## 0.0.1

## Added

An echo-widget at the bottom of the top screen prints actions when triggered by the user.

The active deck is now displayed at the side in the echo widget.

Added a toggle button for sequencer recording mode to the button of the pads screen.

## Changed

Screens are now selected with the D-Pad:

 - Press once to select screen
 - Press multiple times to cycle additional screens
 - Press Select + D-Pad to select alternate lower screens
 - Press Select + Up to return to the companion screen of the upper one

The Instrument / Perform view is selected by default when the app is launched.

The C-Stick moves the upper-screen cursor.

Representations of the 12 lanes, the master lane and four bus lanes can be selected at the bottom of the top screen. The master / buses currently have no functionality.

Pressing a pad at the bottom screen selects it's lane and the top screen updates accordingly.

Initially the current lane is selected.

Pressing B (Escape) returns to the last lane selection.

Sliders can be changed by holding A and moving the C-Stick.

Actions can be triggered by selecting them and pressing A.

When Assign is enabled, selecting actions assigns them to the button X,Y or A button when pressed.

The project / file menu can be accessed by pressign down on the D-Pad, here a project can be loaded or saved and the user may exit the application.

Some features are temporarily inaccessible due to GUI refactoring:

- Slicing

The distortion- and filter effects currently onlu affect bus 1. This will change in the future.

When SD-Card recording is activated, the file-path is displayed at the bottom and the recording time is displayed at the top left in the title bar.

Added a "Follow" option to the Grid-Editor (bottom screen). When enabled, the current bar is displayed during playback.

## Fixed

Some bugs but probably introduces some too.

## 0.0.0

Initial release

