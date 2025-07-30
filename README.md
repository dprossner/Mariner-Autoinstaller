### Fixed a bug preventing input for smb share name from being asked for, added virtual drive size customization, and modified to install the mariner fork by @beaudeanadams with support for firmware 4.4.3

## See https://github.com/luizribeiro/mariner/ for info on hardware requirements and the origin of the main compenent that this script installs.

# Mariner Autoinstaller

This script is intended for a fresh Rasbian Lite installation on a Raspberry Pi Zero, but should work on all Pi models that support USB OTG.

It will expand the filesystem to the full size of your SD card, install Mariner, set up a folder on the Pi as a USB drive, create a sambashare, and a couple other things.
### Skip Configuration
If you've already expanded your filesystem (seems to be done automatically on boot in modern versions of PiOS), and changed your hostname and password, you can skip those steps in the script by running
`sudo touch ./resume-mariner`, which creates a file that tells the script these tasks have been completed. Just make sure all background tasks from initial boot are done.


### Download
Either from this Github or using
`wget https://github.com/dprossner/Mariner-Autoinstaller/blob/Testing/mariner.sh`

### Prepare for execution
`sudo chmod +x ./mariner.sh`

### Execute
`sudo bash ./mariner.sh`

Follow the prompts in the script, reboot, and run once more.
You should see a different set of prompts on the second run.
