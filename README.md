# raspberrypi5-retropie-setup
## Purpose of this guide
RetroPie currently does not provide a pre-made image for the Raspberry Pi 5. Also, the 
[latest image](https://retropie.org.uk/download/) at the time of writing this guide is v4.8 based on Raspbian with 
Debian 10 from March 14, 2022. 

The [GitHub for RetroPie](https://github.com/RetroPie/RetroPie-Setup) has active development and at least somewhat 
supports the Raspberry Pi 5 and the latest Raspberry Pi OS with Debian 12. So a manual installation is possible, but 
the [official documentation](https://retropie.org.uk/docs/Manual-Installation/) is outdated and covers a wider range of 
hardware, which can make it hard to follow.

This guide will cover performing a manual installation specific to Raspberry Pi 5 hardware and will attempt to install 
RetroPie the same way it would be installed from a pre-made image. 

## Install OS
Raspberry Pi 4 used to be able to install the OS onto an micro SD card directly from the internet using 
[Network Install](https://www.raspberrypi.com/documentation/computers/getting-started.html#install-over-the-network), 
without the need for another computer. However this is not yet available for Raspberry Pi 5. So we will need another PC 
and a way to read/write to a micro SD card.

In order to install the OS, use [Raspberry Pi Imager](https://www.raspberrypi.com/documentation/computers/getting-started.html#install-using-imager)
on a Windows, Mac, or Linux PC:
![Raspberry Pi Imager](./screenshots/rpi_main_01.png?raw=true "Main")
1. (Optional) Select "Choose Device" and select "Raspberry Pi 5" (this just filters images to compatible devices)
   ![Select "Raspberry Pi 5 device"](./screenshots/rpi_choose-device.png?raw=true "Raspberry Pi Device")
2. Select "Choose OS", select "Raspberry Pi OS (other)", then select "Raspberry Pi OS Lite (64-bit)"
   ![Select "Raspberry Pi OS (other)"](./screenshots/rpi_choose-os_01.png?raw=true "Operating System")
   ![Select "Raspberry Pi OS (64-bit)"](./screenshots/rpi_choose-os_02.png?raw=true "Operating System")
3. Select "Choose Storage" and select your micro SD card
   ![Select micro SD card](./screenshots/rpi_choose-storage.png?raw=true "Storage")
4. Select "Next"
   ![Select "Next"](./screenshots/rpi_main_02.png?raw=true "Main")
5. Select "Edit Settings" when asked about applying OS customisation settings
   ![Select "Edit Settings"](./screenshots/rpi_use-os-customization.png?raw=true "Use OS customisation?")
   1. General
      ![Set hostname, username, and password](./screenshots/rpi_os-customization_general.png?raw=true "OS Customisation")
      1. Set hostname to `retropie`
      2. Set username to `pi` and password to `raspberry`
      3. (Optional) Wireless LAN would not be configured in a pre-made RetroPie image, but you can do so here so that
         it will connect to your network on boot
      4. Locale Settings {::comment}TODO determine default locale settings if at all{:/comment}
   2. Services
      1. (Optional) SSH is disabled by default in pre-made RetroPie images, but you can do so here so that you can 
      connect to your RetroPie on boot
      ![Optionally configure SSH](./screenshots/rpi_os-customization_services.png?raw=true "OS Customisation")
   3. Options
      1. (Optional) Playing a sound when finished or ejecting the media don't affect the install but may be useful. 
      {::comment}TODO determine whether telemetry is enabled in pre-made images{:/comment}
      ![Optionally play a sound or eject media when finished](./screenshots/rpi_os-customization_options.png?raw=true)
6. Select "Yes" to apply OS customisation settings
   ![Select "Yes"](./screenshots/rpi_use-os-customization.png?raw=true "Use OS customisation?")
7. Select "Yes" when warned about all existing data on the micro SD card being erased
   ![Select "Yes"](./screenshots/rpi_warning.png?raw=true "Warning")
8. Wait for it to finish writing
   ![Wait](./screenshots/rpi_writing.png?raw=true "Writing")
9. Select "Continue" when it says you can now remove the SD card from the reader
   ![Select "Continue"](./screenshots/rpi_write-successful.png?raw=true "Write Successful")
