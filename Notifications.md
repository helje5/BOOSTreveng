subscribed to characteristic 00001624-1212-efde-1623-785feabcd123

received:

* `0f 00 04 01 01 25 00 00 00 00 10 00 00 00 10` - ?
* `0f 00 04 02 01 26 00 00 00 00 10 00 00 00 10` - ?
* `0f 00 04 37 01 27 00 00 00 00 10 00 00 00 10` - ?
* `0f 00 04 38 01 27 00 00 00 00 10 00 00 00 10` - ?
* `09 00 04 39 02 27 00 37 38` - Port Group: 0x39 consists of 0x37 and 0x38
* `0f 00 04 32 01 17 00 00 00 00 10 00 00 00 10` - ?
* `0f 00 04 3a 01 28 00 00 00 00 10 00 00 00 02` - ?
* `0f 00 04 3b 01 15 00 02 00 00 00 02 00 00 00` - ?
* `0f 00 04 3c 01 14 00 02 00 00 00 02 00 00 00` - ?
* `05 00 82 37 01` - Motor A (0x37) starts movement
* `05 00 82 37 0a` - Motor A (0x37) stops movement
* `05 00 82 37 05` - Motor A (0x37) Is reported when a command is received while the motor is still in movement
* `05 00 82 32 0a` - Reports a change of the LED state

* Byte 0 as always: message length

* Byte 1? Protocol version? HiByte of message length? 

* Byte 2 is the message type: 
  * `0x04` port information
  * `0x45` sensor reading
  * `0x82` port changed
  
* Byte 3 is the port number:
  * `0x01` C
  * `0x02` D
  * `0x32` LED
  * `0x37` A
  * `0x38` B
  * `0x39` A and B
  * `0x3a` TILT SENSOR


### Message type 0x04 port information

* Byte 5 is the device type:
  * `0x25` DISTANCE/COLOR SENSOR
  * `0x26` IMOTOR
  * `0x27` MOTOR
  * `0x28` TILT SENSOR
  
### Message type 0x45 sensor reading  



### Message type 0x82 port changed 


* Byte 4:
  * `0x01` action started
  * `0x05` conflict. New action received while other action is still running
  * `0x0a` action finished
  
 
