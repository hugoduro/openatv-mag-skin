# MAG-TV v2 – Enigma2 Skin (OpenATV 6.x), 1280x720
====================================================

Same look and feel as e2player / TVH Player:

- Channel list with video preview, picon, current programme, progress bar, "Next" programme and description of the selected channel.
- Information bar showing channel number, picon, name, now / next, progress bar, remaining minutes and clock (30% transparent background).
- Second information bar (press INFO twice) displaying the full programme description.
- All other windows (menus, settings, EPG, etc.) use the same colour palette.

## CONTENTS

`usr/share/enigma2/MAG-TV/`  
Skin, fonts (DejaVu) and frames.

`usr/lib/enigma2/python/Components/Converter/MagInfo.py`  
Skin converter (channel number, time, remaining minutes and next programme).

## INSTALLATION (via SSH/Telnet, e.g. PuTTY)

1. Copy the `mag-tv-skin.tar.gz` file to `/tmp` on your receiver (via FTP, using the root user).
2. On the receiver, run:

   ```bash
   tar -xzf /tmp/mag-tv-skin.tar.gz -C /
   ```

3. Go to **Menu > Setup > System > Skin (User Interface)**, select **"MAG-TV"** and confirm the GUI restart.

**Without SSH:** Copy the `usr/share/enigma2/MAG-TV` folder and the `MagInfo.py` file via FTP to the corresponding paths on your receiver, then select the skin from the menu.

## IF THE INTERFACE FAILS TO START (RECOVERY VIA SSH/TELNET)

Run the following commands
