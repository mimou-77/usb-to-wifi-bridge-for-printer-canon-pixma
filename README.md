
> [!NOTE]
> requires esp-idf >=5.2 + the printer's driver
> this example uses windows
> use the driver of your printer, here we used canon pixma
> hardware : esp32s3

# How this works 

<img src="overview.png" alt="overview" width="600">

- we manually add a new printer defined with its IP (or hostname). <br/>
- we select : 
    - port = 9100 (protocole raw)
    - driver = Canon Pixma (your printer's driver)

Now, when we print a document : 
1. the driver formats the document in the format the printer accepts.
2. the Windows service `spoolsv.exe` (handler of printing FIFO) : opens a TCP connection to the ip of the esp32