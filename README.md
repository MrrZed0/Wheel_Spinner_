Preview: https://mrzed0.com/wp-content/uploads/Wheel_Spinner/overlay.html

========================================
3D PERSISTENT STREAM WHEEL
Setup & User Guide
========================================

OVERVIEW
--------
This system is a custom 3D Stream Wheel that runs using:
- A Python backend server
- OBS browser overlay
- Streamer.bot automation
- Optional Stream Deck controls

The wheel automatically:
- Loads entries from names.txt
- Removes used results permanently (blacklist.conf)
- Saves results between sessions


========================================
1. FILE STRUCTURE
========================================

All files MUST stay in the same folder:

- overlay.html              (Wheel overlay)
- admin.html                (Color settings panel)
- server.py                 (Python backend server)
- run.bat                   (Start server script)
- python-3.14.4-amd64.exe   (Python installer)
- names.txt                 (List of entries, one per line)
- colors.conf               (Saved wheel colors)
- blacklist.conf            (Removed/winning entries)
- wheel_of_fortune_tick.mp3 (Spin sound effect)


========================================
2. INSTALLATION
========================================

STEP 1 — Install Python
------------------------
1. Run: python-3.14.4-amd64.exe
2. IMPORTANT: Enable “Add Python to PATH”
3. Finish installation


STEP 2 — Start Server
---------------------
1. Run: run.bat
2. Keep the black command window open
3. Confirm message:
   "Wheel Server running at http://localhost:8000"


STEP 3 — Configure Colors
-------------------------
1. Open:
   http://localhost:8000/admin.html
2. Choose your wheel colors:
   - Segments
   - Border
   - Text
   - Center
3. Click: SAVE COLORS.CONF
4. Replace the file in your folder


STEP 4 — Launch Wheel
---------------------
1. Open:
   http://localhost:8000/overlay.html
2. Wheel loads automatically:
   - Reads names.txt
   - Removes blacklist entries
   - Spins after 2-second delay
3. Result is saved to blacklist.conf


========================================
3. OBS STUDIO SETUP
========================================

1. Open OBS Studio
2. Add Source → Browser
3. Name: Wheel Spinner
4. URL:
   http://localhost:8000/overlay.html
5. Set resolution:
   800 x 800 (recommended)

Optional:
- Enable "Shutdown source when not visible"
  (wheel resets when shown again)


========================================
4. MANAGING THE WHEEL
========================================

RESET WHEEL:
- Open blacklist.conf
- Delete all contents

ADD NEW ENTRIES:
- Edit names.txt
- One entry per line

AUTO BEHAVIOR:
- Removed entries are never reused
- Wheel updates dynamically
- Colors remain consistent even after removals


========================================
5. STREAMER.BOT SETUP
========================================

IMPORT:
Use the provided Streamer.bot import code to load all actions automatically.


Import_Code:
------------
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




ACTIONS INCLUDED
-----------------

1. Add_Item_To_Wheel
   - Adds entry from chat/reward input
   - Appends to names.txt

2. Start_Wheel_Spinner_Server
   - Starts Python backend server

3. End_Wheel_Spinner_Server
   - Stops Python server

4. Show_Overlay_And_Spin
   - Shows OBS overlay
   - Spins wheel

5. Hide_Overlay
   - Hides OBS overlay

6. Reset_Wheel
   - Clears:
     names.txt
     blacklist.conf


========================================
6. OBS INTEGRATION
========================================

Browser Source Setup:
- Path:
  C:\Program Files\obs-studio\Wheel_Spinner\overlay.html
- Recommended size:
  1920 x 1080
- Enable:
  "Refresh when scene becomes active"


========================================
7. STREAM DECK SETUP
========================================

INSTALL PLUGIN:
1. Open Stream Deck software
2. Go to Plugin Store
3. Install "Streamer.bot"
4. Set WebSocket:
   ws://127.0.0.1:8080


ENABLE IN STREAMER.BOT:
Settings → WebSocket Server → Enable


BUTTONS
-------

SPIN BUTTON
- Action: Show_Overlay_And_Spin

HIDE BUTTON
- Action: Hide_Overlay

OPTIONAL:
- Add Item → Add_Item_To_Wheel
- Reset → Reset_Wheel


========================================
8. HOW IT WORKS
========================================

1. Viewer adds item (command/reward)
2. Item saved to names.txt
3. Python server manages data
4. OBS displays wheel
5. Streamer.bot triggers spin
6. Winner is saved permanently in blacklist


========================================
9. TROUBLESHOOTING
========================================

- Server not starting:
  → Ensure Python is installed + PATH enabled

- Wheel not updating:
  → Refresh OBS browser source

- Stream Deck not working:
  → Check WebSocket connection (8080)

- Permissions issues:
  → Run Streamer.bot as Administrator


========================================
END OF GUIDE
========================================
