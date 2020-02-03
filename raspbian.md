# Raspbian

## Headless configuration

In my setup, not only I don't have any keyboard/monitor available but anyway: it would quickly become cumbersome to configure multiple raspberry-pi manually.

Therefore, we'll configure both `ssh` and `Wifi` connection at the provisioning time so we can manage the raspberries remotely.

* [Download latest `Raspbian ... Lite` image][4]
* Unzip and mount the `.img` image (1)
* Create the files `ssh` & `wpa_supplicant.conf` at the root directory of the image
* Edit [`wpa_supplicant.conf`][2] according to your setup

> (1) MacOS natively support the `.img` format: if you double click on the image, it should mount the image in `/Volumes`

## Sources

* [`config.txt` reference][1] - equivalent of BIOS config
* [headless configuration][2]
* [`vcgencmd` documentation][3] - command line utility for the Raspberry Pi

[1]: https://www.raspberrypi.org/documentation/configuration/config-txt/README.md
[2]: https://www.raspberrypi.org/documentation/configuration/wireless/headless.md
[3]: https://www.raspberrypi.org/documentation/raspbian/applications/vcgencmd.md
[4]: https://www.raspberrypi.org/downloads/raspbian/
