# Server vs Client

## CLI
Generic command line usage
* python3 upsmanager.py <nodeType> <serverip>

## Server
Server will have a single thread:
* Loop checking for changes in state of AC power to the UPS


### Startup
* main loop
    * Check state of UPS devices
    * If no AC power is detected -> Increment counter
    * If counter >= threshold, send shutdown command to all enrolled nodes


### Startup
* Consume hosts configuration file 
* Verify all hosts can be reached via ssh w/ keys
* Begin main loop