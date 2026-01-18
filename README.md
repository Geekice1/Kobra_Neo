Anycubic Kobra Neo V1.3.3 - Advanced
<p align="center"> <img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" /> <img src="https://img.shields.io/badge/Marlin-2.1.x-blue.svg" /> <img src="https://img.shields.io/badge/Kobra_Neo-Optimized-orange.svg" /> </p>

🌟 Why this fork?
The original firmware and many existing forks have a "broken" preheat system where temperatures are hardcoded. This version fixes the core logic, making the printer's preheat buttons actually listen to your settings.

🛠 What's New & Fixed
🔧 The "Preheat Fix" (Index-Based Logic)
Dynamic Profiles: Unlike other versions, the preheat buttons are now linked to Marlin Material Indexes (I0, I1, I2).

User Control: If you change the PETG, ABS or PLA temperature in the Advanced Settings menu, the shortcut buttons will automatically use your new values. No more hardcoded temperatures!

Simultaneous Heating: Nozzle and Bed start heating at the same time to get you printing faster.

🧪 Improved Material Profiles
PETG Profile Added:A 3rd profile is now available

⚡ Inherited "Pro" Features
Speed & Accel: Max feedrate increased to 50, X/Y acceleration to 1000, and Jerk to 8.

Advanced Menus: Enabled Edit Mesh, Bed Tramming, Controller Fan, and Advanced Settings.

Host Actions: Full Octoprint/Klipper support (Start/Pause/Resume prompts on screen).

Probing: Higher accuracy with multiple probes per point and faster Z-approach.

G-Code Support: Enabled M117 (Screen messages) and M73 (Progress bar).

📥 Download & Installation
Go to the Releases section.

Download firmware.bin.

Copy it to a formatted microSD card.

Insert the card with the printer OFF, then turn it ON.

Wait for the home screen, then delete the file from the card.

⚠️ Mandatory: Before You Print
[!IMPORTANT] Reset EEPROM: After flashing, go to Menu -> Configuration -> Advanced Configuration -> Initialize EEPROM. If you don't, the printer might keep old, buggy values!

🎯 Calibration
PID Autotune: Run it for both E1 and Bed via the menu (Configuration -> Advanced Settings -> Temperature).

E-Steps: This firmware uses my personal values. I highly recommend calibrating your own E-steps for perfect extrusion.

🏗 Building from source
This project is pre-configured for Keil MDK-ARM.

Open Project.uvprojx.

Hit Build.

The .bin file will be generated in the output folder.

🤝 Credits & Acknowledgments
This work is built upon the contributions of the Kobra Neo community:

jokubasver (Base improved firmware)

sjorge & jojos38 (Original Marlin ports)
