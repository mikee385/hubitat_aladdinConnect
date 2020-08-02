# hubitat_aladdinConnect

This provides GarageDoorControl, SignalStrength (BLE door sensor), and SignalStrength (wifi main unit) driver capabilities for Hubitat with Genie Aladdin Connect garage door openers.

Note that all operations have a cloud (internet) interaction.  This implementation is based on the work shared here:  https://documenter.getpostman.com/view/5856894/RzZAjHxV?version=latest

# Installation instructions:

* In the Drivers Code section of Hubitat, add the aladdinConnectSystem and aladdinConnectGarageDoor drivers.
* In the Devices section of Hubitat, add a New Virtual Device of type Aladdin Connect System.
* Open the configuration page for the newly created Device and enter your username and password for Aladdin Connect and click Save Preferences.
* Refresh the configuration page and look for child devices for any garage doors that are configured in your system.  Up to three doors per system are supported.

# Usage instructions:

* Use the Garage Door (control) template in Hubitat Dashboard.
* Create actions in the HSM, Garage Doors, Locks and Valves section to control the door in Rule Machine.  Note that you may need to install HSM if that option does not appear in actions in Rule Machine.

# Disclaimer

I have no affiliation with any of the companies mentioned in this readme or in the code.  I also don't have an Aladdin Connect garage door opener, so my ability to troubleshoot will be limited.
