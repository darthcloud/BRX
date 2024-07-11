# BRX BETA DOCS

![](static/BRX_green_shadow_blk.png)

## Original BlueRetro docs that apply to the BRX adapter
* [3 - Pairing Bluetooth controller](https://github.com/darthcloud/BlueRetro/wiki#3---pairing-bluetooth-controller)
  * [Controller List & Pairing Guide](https://github.com/darthcloud/BlueRetro/wiki/Controller-pairing-guide)
* [4 - Web config](https://github.com/darthcloud/BlueRetro/wiki#4---web-config) <-- Note: ignore the BLE OTA FW Update section, follow the FW update over Wi-Fi section below.
  * [BlueRetro BLE Web Config User Manual](https://github.com/darthcloud/BlueRetro/wiki/BlueRetro-BLE-Web-Config-User-Manual)
* [5 - Physical buttons usage](https://github.com/darthcloud/BlueRetro/wiki#5---physical-buttons-usage)
* [6 - Button combinations functions](https://github.com/darthcloud/BlueRetro/wiki#6---button-combinations-functions)
  * [BlueRetro mapping reference](https://docs.google.com/spreadsheets/d/e/2PACX-1vT9rPK2__komCjELFpf0UYz0cMWwvhAXgAU7C9nnwtgEaivjsh0q0xeCEiZAMA-paMrneePV7IqdX48/pubhtml)

## Known issues
* PS4 & PS5 controller connection at Xbox boot time might lockup the adapter.\
  Workaround: Connect the controller after the boot animation once you reached the Xbox menu.

## Missing feature
* Auto-fire is not yet implemented.

## Firmware Update over Wi-Fi
1. Turn your Xbox console off.
2. Connect the BRX dongle into one of the controller slots.
3. Hold the BRX dongle button and simultaneously power on the Xbox console. Once the power is on, release the BRX dongle button.  
4. The LED on the dongle will be solid ON and do two quick OFF blinks every second, indicating it is attempting to connect to Wi-Fi.
5. If Wi-Fi is configured already, skip to step 10.
6. If Wi-Fi is not yet configured on the BRX dongle, the adapter will stay in the blinking state until you configure it.
7. Install the Espressif "Soft-AP" provisioning App on your phone.\
   Apple: https://apps.apple.com/cn/app/esp-softap-provisioning/id1474040630 \
   Android: https://github.com/espressif/esp-idf-provisioning-android/releases
8. Scan the following QR code within the Espressif App.\
   ![](static/xbox_qr_code.png)
9. Once the app is connected to the dongle, select the Wi-Fi Network you want to connect to and enter the password for the network.
10. Once connected, the LED pattern will change to two quick ON blinks every second.
11. Once completed, it the dongle will reboot and the LED will be pulsing to indicate it's in Bluetooth paring mode.

## Factory reset
1. Turn your Xbox console off.
2. Connect the BRX dongle into one of the controller slots.
3. Hold the BRX dongle button and simultaneously power on the Xbox console. Keep holding the button for around 8 seconds and then release it.
4. Once done, it will reboot and the LED will be pulsing to indicate it's in paring mode.

## Updating the Wi-Fi configuration for FW update
* After 5 failed Wi-Fi connection attempts, the Wi-Fi settings will be reset and will be reconfigurable via the Espressif app.
* Alternatively, you can also factory reset the BRX adapter.

## I don't want to/can't use either of the phone apps.
It's possible to configure the Wi-Fi using a PC with Wi-Fi and a python scripts.

**DOCS TBD**

## I don't want to/can't let the dongle access the Internet
It's possible to configure the Wi-Fi using a PC with Wi-Fi and a python scripts and to set a local web server.

**DOCS TBD**
