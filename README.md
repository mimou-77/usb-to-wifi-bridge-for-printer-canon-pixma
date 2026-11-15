
> [!NOTE]
> requires esp-idf >=5.2 + the printer's driver

# How this works 

<img src="overview.png" alt="overview" width="600">

1. The Canon Pixma printer driver formats the document in the  format that the printer accepts
2. the PC establishes a TCP connection, sends the RAW bytes by wifi to the esp32s3, the esp32s3 sends them to the usb port.
(also data from the printer are received from the usb port).



# Steps (without using the script)
1. connect : USB OTG port ===> to the printer ; UART port ===> to the PC
2. 

# Steps (using the script)

