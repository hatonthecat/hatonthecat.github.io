One of the goals of this page is to determine how to develop a webpage that can host thousands of concurrent connections on a lightweight System on a chip, such as a raspberry Pi. 

https://en.wikipedia.org/wiki/Yaws_(web_server)

"https://web.archive.org/web/20070118063239/http://www.sics.se/~joe/apachevsyaws.html "Machine 2 requests 20 KByte pages from machine 1. It does this in tight a loop requesting a new page as soon as it has received a page from the server." 

I installed an Apache Server on a Raspberry Pi 3B+ with Noip.com, MariaDB, php admin webpage less than 500 bytes.![image](https://user-images.githubusercontent.com/76194453/202923239-9fcbf9da-ec33-41fb-83b3-2b0890834f57.png)  Ideally, it would be used to host a BBS-like system, but with additional features. 

The website is hosted at: http://buoy.hopto.org/
A couple tutorials were used: 

https://peppe8o.com/lamp-server-on-raspberry-pi/

the above tutorial is thorough, although it took 3-4 tries to install MariaDB. In terminal, it could not fetch all the packages, so I retried without issue. Possibly the server or wifi connection was not good. 

Edit: I removed MyAdminPHP and MariaDB since i was only serving static pages.

Also, permissions to edit and remove /var/www/html and replace it with my own page is listed here:

https://forums.raspberrypi.com/viewtopic.php?t=297575 

"This allows you (pi) to read and write to that directory and apache to
read from that directory. So how do you do that?

sudo chown pi:www-data /var/www/html

sudo chmod 755 /var/www/html "


Another goal of this project is to explore hosting simple servers on a microcontroller, with an OS such as FreeRTOS or Zephyr: https://www.freertos.org/FreeRTOS-Plus/FreeRTOS_Plus_TCP/TCP_Networking_Tutorial.html

https://elinux.org/images/1/18/Rissanen.pdf The Apache Server on my Raspbian OS, using a Raspberry Pi 3+ uses just under 200MB of RAM to host a couple 512byte pages. More than likely, that much RAM is not needed, and could likely be done on just 2MB of RAM or less. Hosting a Gopher or Gemini server may be a simpler protocol, although all internet protocols will be explored. I haven't hosted an HTTP site in over 15 years, so give me a break :) I actually wrote a lot more on that page. It was called Witsy.com, and it was hosted on https://www.knightsbridge.net/index.html for a year or two. I used CuteFTP or Filezilla to upload static pages, similar to the pages I have now, except that I host the server now. I would have kept it but I graduated college and I had other careers to pursue.
