# CamaControl

This is a REST-ful HTTP server that is intended to be installed on a Raspberry Pi or similar to allow one to control their Mattress Firm 900 series (also used by other vendors) adjustable bed via things like HomeKit, Google Assistant and Amazon Alexa. 

This package doesn't do any of the assistant integration, just provides a web-based API you can tie into other things that integrate with the assistant. 

## Prerequisites

You'll need the [BluePy library](https://github.com/IanHarvey/bluepy) to talk to the bed from Python. This will also require BlueZ, which in turn requires a Linux machine. 

## Files

* camacontrol - the main process. Run as a non-root user after you permit DBUS transactions from non-privileged processes. [See here for details.](https://www.raspberrypi.org/forums/viewtopic.php?t=108581)
* camacontrol.service - a systemd template to daemonize the above.
* camacontrol.pygatt - DEPRICATED. An older version of the code built against the pygatt library vs. BluePy. Left here for posterity/in case anybody wants to update it. 

## Authors

* **Jeff Maki** - *Initial work* - [Jeff Maki](https://github.com/jeffmaki)

## License

This project is licensed under the MIT License 


