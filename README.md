# hubitat_aladdinConnect

This package provides driver capabilities for Hubitat with Genie Aladdin Connect systems: GarageDoorControl; SignalStrength (as rssi for the BLE door sensor); and Battery (as % for the BLE door sensor) .

Note that all operations have a cloud (Internet) interaction. This implementation is based on reverse engineering of the new API, which began rolling out in late 2021 and broke compatibility with 1.x versions of this driver.  This implementation was used as a reference for basic API operations: https://github.com/shoejosh/aladdin-connect

This new implementation also utilizes a websocket interface for faster status updates without polling, with great thanks to @mike-s123 for doing the research and documenting that interface.  Polled refreshes are now only necessary for SignalStrength and Battery level.

# Installation instructions:

* In the *Drivers Code* section of Hubitat, add the aladdinConnectSystem and aladdinConnectGarageDoor drivers.
* In the *Devices* section of Hubitat, add a *New Virtual Device* of type Aladdin Connect System.
* Open the configuration page for the newly created *Device* and enter your username and password for Aladdin Connect and click *Save Preferences*.
* Refresh the configuration page and look for child devices for any garage doors that are configured in your system.  Up to three doors per system are supported.

# Usage instructions:

* Use the *Garage Door (control)* template in Hubitat Dashboard.
* Create actions in the *HSM, Garage Doors, Locks and Valves* section to control the door in Rule Machine.  Note that you may need to install Hubitat Safety Monitor (HSM ) if that option does not appear in actions in Rule Machine.

# Disclaimer

I have no affiliation with any of the companies mentioned in this readme or in the code.  I also don't have an Aladdin Connect garage door opener, so my ability to troubleshoot will be limited.
