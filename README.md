# BRX BETA DOCS

## Original BlueRetro docs that apply to the BRX adapter
* [3 - Pairing Bluetooth controller](https://github.com/darthcloud/BlueRetro/wiki#3---pairing-bluetooth-controller)
  * [Controller List & Pairing Guide](Controller-pairing-guide)
* [4 - Web config](https://github.com/darthcloud/BlueRetro/wiki#4---web-config) <-- Note: ignore the BLE OTA FW Update section, follow the FW update over Wi-Fi section below.
  * [BlueRetro BLE Web Config User Manual](BlueRetro-BLE-Web-Config-User-Manual)
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
2. Connect the BRX dongle into one of the controller slot.
3. Hold the BRX dongle button and simultaneously power on the Xbox console.
4. Once power is on release the BRX dongle button.  
5. While the dongle try to connect to Wi-Fi the LED will be solid ON with two quick OFF blink every second until it connect.
6. If Wi-Fi is configured already skip to step X.
7. If Wi-Fi is not yet configure on the BRX dongle the adapter will stay at that state until your configure it.
8. Install the Espressif Soft-AP provisionning App on your phone.\
   Apple: https://apps.apple.com/cn/app/esp-softap-provisioning/id1474040630 \
   Android: https://github.com/espressif/esp-idf-provisioning-android/releases
9. Scan the following QR code within the Espressif App.\
   ![](static/xbox_qr_code.png)
10. Once the app is connected to the dongle select the Wi-Fi Network you want to connect to.
11. Enter the password for the Wi-Fi Network.
12. Once connected the LED pattern will change to two quick ON blink every second.
13. Just wait for the BR dongle to complete it's update.
14. Once done it will reboot and the LED will be pulsing to indicate it's in paring mode.

## Factory reset
1. Turn your Xbox console off.
2. Connect the BRX dongle into one of the controller slot.
3. Hold the BRX dongle button and simultaneously power on the Xbox console.
4. Keep holding the button for around 8 second and then release it.
5. Once done it will reboot and the LED will be pulsing to indicate it's in paring mode.
