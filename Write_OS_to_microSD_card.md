In order to write the OS to a microSD card, use 
[Raspberry Pi Imager](https://www.raspberrypi.com/documentation/computers/getting-started.html#install-using-imager)
on a Windows, Mac, or Linux PC:
![Raspberry Pi Imager](screenshots/install_os/rpi_main_01.png?raw=true "Main")
1. (Optional) Select "Choose Device" and select "Raspberry Pi 5" (this just filters images to compatible devices)
   ![Select "Raspberry Pi 5 device"](screenshots/install_os/rpi_choose-device.png?raw=true "Raspberry Pi Device")
2. Select "Choose OS", select "Raspberry Pi OS (other)", then select "Raspberry Pi OS Lite (64-bit)"
   ![Select "Raspberry Pi OS (other)"](screenshots/install_os/rpi_choose-os_01.png?raw=true "Operating System")
   ![Select "Raspberry Pi OS (64-bit)"](screenshots/install_os/rpi_choose-os_02.png?raw=true "Operating System")
3. Select "Choose Storage" and select your microSD card
   ![Select microSD card](screenshots/install_os/rpi_choose-storage.png?raw=true "Storage")
4. Select "Next"
   ![Select "Next"](screenshots/install_os/rpi_main_02.png?raw=true "Main")
5. Select "Edit Settings" when asked about applying OS customisation settings
   ![Select "Edit Settings"](screenshots/install_os/rpi_use-os-customization.png?raw=true "Use OS customisation?")
    1. General
       ![Set hostname, username, and password](screenshots/install_os/rpi_os-customization_general.png?raw=true "OS Customisation")
        1. Set hostname to `retropie`
        2. Set username to `pi` and password to `raspberry`
        3. (Optional) Wireless LAN would not be configured in a pre-made RetroPie image, but you can do so here so that
           it will connect to your network on boot
       <!--4. Locale Settings TODO determine default locale settings if at all-->
    2. Services
        1. (Optional) SSH is disabled by default in pre-made RetroPie images, but you can do so here so that you can
           connect to your RetroPie on boot
           ![Optionally configure SSH](screenshots/install_os/rpi_os-customization_services.png?raw=true "OS Customisation")
    3. Options
        1. (Optional) Playing a sound when finished or ejecting the media don't affect the install but may be useful.
       <!--TODO determine whether telemetry is enabled in pre-made images-->
       ![Optionally play a sound or eject media when finished](screenshots/install_os/rpi_os-customization_options.png?raw=true)
6. Select "Yes" to apply OS customisation settings
   ![Select "Yes"](screenshots/install_os/rpi_use-os-customization.png?raw=true "Use OS customisation?")
7. Select "Yes" when warned about all existing data on the microSD card being erased
   ![Select "Yes"](screenshots/install_os/rpi_warning.png?raw=true "Warning")
8. Wait for it to finish writing
   ![Wait](screenshots/install_os/rpi_writing.png?raw=true "Writing")
9. Select "Continue" when it says you can now remove the SD card from the reader
   ![Select "Continue"](screenshots/install_os/rpi_write-successful.png?raw=true "Write Successful")
