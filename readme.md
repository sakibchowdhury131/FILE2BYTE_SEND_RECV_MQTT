# anyfile can be sent by opening the files in bytes mode

- send: 
	- open the file in bytes mode 
	- publish the contents as bytearray 
 
 
- receive:
	- open an empty file
	- save all the bytes received from MQTT topic
