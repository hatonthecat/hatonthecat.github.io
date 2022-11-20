One of the goals of this page is to determine how to develop a webpage that can host thousands of concurrent connections on a lightweight System on a chip, such as a raspberry Pi. 

https://en.wikipedia.org/wiki/Yaws_(web_server)

"https://web.archive.org/web/20070118063239/http://www.sics.se/~joe/apachevsyaws.html "Machine 2 requests 20 KByte pages from machine 1. It does this in tight a loop requesting a new page as soon as it has received a page from the server." 

I installed an Apache Server on a Raspberry Pi 3B+ with No-ip.com, MariaDB, php admin webpage less than 500 bytes.![image](https://user-images.githubusercontent.com/76194453/202923239-9fcbf9da-ec33-41fb-83b3-2b0890834f57.png)  Ideally, it would be used to host a BBS=-like system, but with additional features. 


A couple tutorials were used: 

https://peppe8o.com/lamp-server-on-raspberry-pi/

the above tutorial is thorough, although it took 3-4 tries to install MariaDB. In terminal, it could not fetch all the packages, so I retried without issue. Possibly the server or wifi connection was not good. 

Also, permissions to edit and remove /var/www/html and replace it with my own page is listed here:

https://forums.raspberrypi.com/viewtopic.php?t=297575 
"This allows you (pi) to read and write to that directory and apache to
read from that directory. So how do you do that?

sudo chown pi:www-data /var/www/html
sudo chmod 755 /var/www/html"
