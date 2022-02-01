# librtty

## Information

This is librtty [/ˈlɪbərti/], an open source Arduino library for generating an RTTY bitstream to be fed into an FM transmitter. Uses a potential divider on the Arduino output pin, providing the correct voltages to set the frequency shift.  

## Usage

Call this line before setup():  
`RTTY rtty(radio_txd_pin, baud_rate, stop_bits, CHECKSUM_CRC16)`  

Then call the `transmit()` function with the string you wish to send, forex:  
`rtty.transmit("This is my string\r\n")`  

**Library Functions**:  
Transmit a string:  
`transmit(string);`  

Set the transmission baud rate:  
`setBaud(50);`

Change the transmitting pin:  
`setPin(5);`

Set the stopbits:  
`setStopbits(1.5);`  

Get the current baud rate setting:  
`getBaud();`  

Set the checksum type to be appended to the transmitted string:  
`setChecksum(CHECKSUM_CRC16);`  

Get the current checksum setting:  
`getChecksum();`  

## Credits

Written by Jon Sowman in 2010 and released into the public domain under the
Creative Commons Attribution-NonCommercial-ShareAlike 3.0 License.

Modified in 2022 to work with Arduino 1.0+ and added functions.
