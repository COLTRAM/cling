Read the README from the original project
=========================================

https://github.com/4thline/cling

Mods
---------------------

* Addition of a ApplicationURLHeader

* Modification of RemoteDevice to store the Application URL information

* Modification of RetrieveRemoteDescriptors to get the info from the header and put it in the RemoteDevice

Usage
---------------------

* In a RegistryListener, listen for failed discoveries by implementing remoteDeviceDiscoveryFailed

* In this method, test device.getType().toString().equals("urn:dial-multiscreen-org:device:dial:1")

* If it is the case, then device.getDIALApplicationURL() gives you the application URL provided as a HTTP header during the SSDP dialog

