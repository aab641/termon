# termon
Raspberry Pi Hardware Monitor Application. See CPU &amp; GPU Performance of your Desktop/Laptop from a raspberry pi.

Termon is a client application, Open Hardware Monitor is the server application from https://openhardwaremonitor.org/downloads/

The server application makes your hardware vitals accessible; serving a json webpage with all the information needed.

This client application is designed to neatly print that JSON data using Java in Terminal or Command Prompt.

I would recommend editing /etc/rc.local on the raspberry pi and replacing the last line with the statement below.

`Java -jar termon.jar [Refresh in Miliseconds] [Insert Desktop IP:PORT Here] & exit 0`

If you would like to run the script manually; here is an example: `Java -jar termon.jar 1000 192.168.1.245:8080`

Right now, the client application is setup to look for GPUs with the keyword "NVIDIA" in the JSON served by the OpenHardwareMonitor.
I do not have AMD products so I have not made it look for AMD products.
You may download the source and re-appropiate it for your needs. It should be extremely simple to change termon to look for AMD
or any other products.

I used a raspberry pi 4 with this Screen: https://www.amazon.com/gp/product/B08343QX67/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1

Video demo below:

[![Demo Here](http://i3.ytimg.com/vi/gQHTQh_N-Go/hqdefault.jpg)](https://youtu.be/gQHTQh_N-Go)

Color Scheme:

![Termon Screenshot](https://i.imgur.com/67ov0qH.png) 

Screenshots below:

![Termon Screenshot](https://i.imgur.com/2jbiCNp.png) 

![Termon Screenshot](https://i.imgur.com/nxNTHO9.png) 
