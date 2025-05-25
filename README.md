Dynamic P2 LED Matrix Display 🌟"

Transform your P2 LED matrix into a sleek, real-time dashboard—showcasing sensor data, time, and date with effortless elegance. Powered by WLEDMM, this automation ensures your display stays fresh, updating at your chosen interval or whenever your sensors change.

✨ Features
- ✅ Customizable Sensor Display: Show live data from any sensor (temperature, humidity, etc.) in beautifully formatted segments.
- ✅ Time & Date: Always stay on schedule with a crisp, auto-updating clock and calendar.
- ✅ Smart Updates: Refreshes automatically and triggers instantly when sensor values change.
- ✅ Plug & Play: Minimal setup—just configure, deploy, and enjoy!
- ✅ Color-Coded Status Rings: Four directional indicators that glow:
    - 🟢 Green for ON/OPEN states
    - 🔴 Red for OFF/CLOSED states
    - 🔵 Blue for other/unknown states

⚙️ 
Setup Guide

First you need to flash and setup your display with WLEDMM then load the config and preset json. Additional you can add the pixart.htm

If you got the display from us as a gift, wledmm is preloaded otherwise it will be mostly with clockwise

1️⃣ Add to configuration.yaml (Required once)

    ```yaml
    rest_command:
      wledmm_matrix:
        url: '{{ url }}'
        method: POST
        payload: '{{ payload }}'
    ```

2️⃣ Add Blueprint

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fjavastraat%2Fwledmm-matrix%2Fblob%2Fmain%2Fwledmm_matrix.yaml)

3️⃣ Configure Your Automation
  - IP of Matrix: Enter your P2 LED panel's IP (e.g., 192.168.2.231).
  - Main Sensors: Pick any sensor (e.g., sensor.buienradar_temperature for Segment 1).
  - Status Rings: Assign binary sensors to four directional indicators (top/right/bottom/left).
  - Custom Colors: Set colors for ON, OFF, and other states.

4️⃣ Watch It Shine! 🌈
  The display will now show:
  - [Color Rings] Four edge indicators showing device states
  - [Top] Your sensor values (e.g., 23°C | 45% humidity)
  - [Center] Animation or Photo :) 
  - [Bottom] Current time (14:30) and date (28/06)

🔧 Pro Tips:
  - Ensure your P2 panel runs WLEDMM and is reachable at the configured IP.
  - Use darker RGB values (0,145,0) for better LED visibility.
  - Top position is ideal for most important status alerts.
  - Use PixArt to send Images to Segment 4 https://kno.wled.ge/features/pixel-art-converter/
  - After download/copy open the pixart.htm file local or on http://IP/pixart.htm  

🖥️ Visual Layout:
                     [🟢TOP]    
               [23°C]       [45%]
      [🟢LEFT] [Middle animation] [🔴RIGHT]
               [14:30]     [28/06]
                   [🔵BOTTOM]


  - Made by Einstein aka PD2EMC for Playreal
  - Just for fun :)

purchase site：https://www.aliexpress.com/item/1005007201147335.html

github of supplier : https://github.com/sjh007/hub75-64-64

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fjavastraat%2Fwledmm-matrix%2Fblob%2Fmain%2Fwledmm_matrix.yaml)
