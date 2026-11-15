
> [!NOTE]
> requires esp-idf >=5.2 + the printer's driver

# How this works 

1. The Canon Pixma printer driver formats the document in the  format that the printer accepts
2. the PC establishes a TCP connection, sends the RAW bytes by wifi to the esp32s3, the esp32s3 sends them to the usb port.
(also data from the printer are received from the usb port).


# Steps (without using the script)
1. connect : USB port ===> to the printer ; UART port ===> to the PC
2. in "main.c" : use your SSID/PASSWORD ; network must be on 2.4GHz <br/> build and flash the firmware.
3. in the serial monitor : search for 'IP: 192.168.x.x' and 'printer ready !' then in the interface of the AP : reserve that ip for the esp32s3.
4. create the RAW TCP/IP port : <br/>
in settings > printers > right click on the printer > properties > ports > add port > std TCP/IP port, new port > put ip of the esp32s3, peripheral type = custom, protocole=RAW, port number = 9100, SNMP disabled > tick this new port > disable "bidirectionnal mode"   

# Steps (using the script)

