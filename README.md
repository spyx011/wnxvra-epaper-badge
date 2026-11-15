# WNXVRA E-Paper Badge
<img width="586" height="322" alt="Screenshot 2026-11-14 224332" src="https://github.com/user-attachments/assets/3c97b21e-7cb9-4345-9590-80e1858332d6" />

A wearable name badge with a 2.9" e-paper display, an ESP32-S3, USB-C charging and a LiPo battery.
The board is shaped like a classic conference badge: chamfered corners, a second panel on the right
joined by two tabs, gold (ENIG) ornaments, and big gold lettering. The battery sits on the back of the right panel.

## Features
- **ESP32-S3-MINI-1**: Wi-Fi, Bluetooth LE, native USB
- **2.9" e-paper** (296 x 128, black/white, GDEY029T94 with SSD1680), 24-pin 0.5 mm FPC
- **USB-C charging** with an MCP73831 (about 196 mA) and a single-cell LiPo (503040, 500 mAh)
- **3.3 V LDO** (AP2112K-3.3); the display supply is switched off by a P-MOSFET during deep sleep
- **5 buttons**: RESET, BOOT, and three user buttons (A, B, C)
- **Gold artwork and lettering** (WNXVRA on the front, @WNXVRA on the back), made of exposed copper
<img width="513" height="353" alt="Screenshot 2026-11-14 224511" src="https://github.com/user-attachments/assets/a454d83f-91c9-4ffe-ac83-09150e7e10d5" />

The e-paper panel needs higher voltages than 3.3 V, so the board has the standard boost circuit
(MOSFET, 47 uH inductor, Schottky diodes and a negative charge pump). Cutting its supply in deep sleep saves battery.
The panel holds its image with no power.

## Bill of materials
48 parts on the board, plus the display and battery. Full list: [`bom/badge_bom.csv`](badge_bom_prices.csv).

##CAD 
3 CAD files one for the base, one for the cover and one for the buttons: [`.STEP`](.STEP).
## Assembly notes
- Check the LiPo plug polarity against J2 before connecting a battery. Cells from different sellers are wired differently.
- Stick the battery to the back of the right panel with double-sided tape, inside the marked outline.
- The two tabs between the panels carry the battery wires. Don't break them off unless you move the battery connector.
- Hold BOOT and tap RESET to enter USB download mode.

