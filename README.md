# U.P.S. Manager

U.P.S. Manager is a python script for monitoring an UPS device and communicating to clients to perform a shutdown in the event of power loss.
This is a personal script that I will use to power down VM's and physical hosts in the event of power loss.
Optimally this will extend the runtime available to power-critical items on my server rack by shutting down resources that would consume the available battery power quickly.

## Example
Server Rack consisting of:
* Dell R710 server
* Netapp DS4243 disk shelf
* Internet Provider modem
* Ubiquiti Router
* Network switch w/ POE devices
* Raspberry Pi 4 (DNS, UPS manager host, VPN etc)

At power loss, this manager would shut down the Dell server and Netapp Disk shelf in a safe manner.
This would allow the network to remain online for an extended period of time w/o interruption. 

## Purpose/ Execution
The server has a USB connection to 1 -> n UPS devices.
The server monitors the state of the the UPS device(s) and awaits for the loss of AC Power
Upon loss of power, the server sends a message to all clients to perform a shutdown.

## Supported Devices
* Tripplite Smart1500LCD - Currently in development

## Recommendations
* Run from a low-power consuming node that can stay online

## Installation

Stub for installation instructions

## Configuration
* List of hosts to execute shutdown command against (json format).
* Priority of shutdown  


## Usage

Stub for usage 

## Future Thoughts
* Turn machines back on after some threshold has been met for restored power.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
Stub for License