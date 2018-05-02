# Description
Docker Image of CSGO Dedicated Server based on ubuntu.<br>Rcon password can be set by editing server.cfg file.<br><br>

Default rcon : toldrcon 

/!\ If the server is not uptodate, just update the variable "ENV REFRESH_DATE 2018-05-02" with the current date and rebuild the image. You can push a pull request, I will accept it and the Docker hook will auto-rebuild the image within an hour...

## Dedicated server is launched with the command
sudo docker run -p  27015:27015 -p 27015:27015/udp -it toldwin/csgo
<br><br>
## You also can launch in command line mode with
sudo docker run -itp 27015:27015/udp toldwin/csgo bash

## To test all incoming connections with tcpdump
sudo apt-get install tcpdump<br>
sudo tcpdump -i eth0 port 27015
