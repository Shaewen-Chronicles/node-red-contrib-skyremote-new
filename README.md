# node-red-contrib-skyremote-new
A [Node-RED](http://nodered.org) node to control a Sky satellite box. The node mimics the functionality of a Sky Remote

## Install

#### Easiest
Use the Manage Palette > Install option from the menu inside node-red

#### Harder
Alternatively in your Node-RED user directory, typically ~/.node-red, run
```bash
npm install node-red-contrib-skyremote-new
```

## Usage
A node to control a Sky satellite box. The node mimics the Sky Box functionality of the Sky Remote.  The purpose of writing the node was to allow other nodes such as homekit, alexa and dashboard to control the status of the Sky Box

Works with SkyQ. 

The node can accept the commands listed below: 

```power``` ```sky```
```tvguide``` or ```home``` ```boxoffice``` ```services``` or ```search``` ```interactive``` or ```sidebar```
```up``` ```down``` ```left``` ```right``` ```select```
```channelup``` ```channeldown``` ```i```
```backup``` or ```dismiss``` ```text``` ```help```
```play``` ```pause``` ```rewind``` ```fastforward``` ```stop``` ```record```
```red``` ```green``` ```yellow``` ```blue```
```1``` ```2``` ```3``` ```4``` ```5``` ```6``` ```7``` ```8``` ```9``` ```0```

 A command can be sent as a string in msg.payload (```msg.payload="play"```).  A chain of commands can be sent as an array of strings in msg.payload (```msg.payload = ["1","0","6","select"]``` for example to change to channel 106)

 The node cannot change the TV volume as that is done from the sky remote handest direct to the TV and not via the Sky Box


## Tested devices

Tested with a DE Sky Q box, the underlying npm library supports Sky+HD but I haven't got one to test.

Tried on another device??? Let me know ;)

## History
- 0.1.1 - February 2020 : Changed to SkyQ and reuploaded to NPM becouse Original Version was gone
- 0.0.8 - March 2017 : Adding node-red keyword removing console.log outputs
- 0.0.7 - March 2017 : Getting npm submission correct
- 0.0.4 - March 2017 : Preparing for npm submission
- 0.0.3 - March 2017 : Grammar & typo corrections
- 0.0.1 - March 2017 : Initial Release

## Authors



* Christian Lerch (https://github.com/Shaewen-Chronicles) All Changes past 0.0.8
* Mark Setrem (https://github.com/ukmoose) Original Version


## Credits

This node is a wrapper around the npm  [sky-remote](https://www.npmjs.com/package/sky-remote) library written by [Dal Hundal](https://github.com/dalhundal) 

Node-RED has been made possible by the hard work of Nick O'Leary @knolleary and Dave Conway-Jones @ceejay at IBM Emerging Technology. Much thanks to them and other supporters for advancing this platform.

## License
This project is licensed under the terms of the MIT license.