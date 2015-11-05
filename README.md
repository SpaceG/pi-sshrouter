# raspberry-pi-ssh-router-firewall-vnc-viewer
Run Raspberry Pi over Mac Os X with ssh and vnc connect to Router Firewall


This is Docu about connect the Raspberry Pi to your Router Firewall via ssh. 


first of all you need some extras. 

1. Raspberry Pi 
2. 2 x Switches 
3. A Router
4. Modem
5. Laptop or Machine whatever
6. SD CARD
7. Another Screen (Desktop Monitor)

like in this picture : <a href="https://instagram.com/p/8FvYS6zgnO/">Raspberry Pi - Set Up Introduction</a> 



1.Now, first you have set up your Raspberry Pi via. Screen Display with your Cable connect to the Raspberry Pi. 
Then follow the Installation from the Raspberry Pi. 

2. Connect all your Switches to your Modem and Routers. Then take a Internet Cable, connect your Pi to the Switches. 

3. Now we go Connect the Raspberry Pi to your Mac Os
All of first do you have to Download the VNC Viewer here Download the newest Version of VNC Viewer for Mac OS X DMG Universal 5.2.3 The Install it on your Machine (Mac Os).

4.First Open your Terminal in Mac Osx. Then Type <code> ping raspberrypi.local </code> 
My Terminal : 

<pre>
Space-O-Mac-Pro:~ cybo$ ping raspberrypi.local
PING raspberrypi.local (10.0.0.3): 56 data bytes
64 bytes from 10.0.0.3: icmp_seq=0 ttl=64 time=1.202 ms
64 bytes from 10.0.0.3: icmp_seq=1 ttl=64 time=0.554 ms
64 bytes from 10.0.0.3: icmp_seq=2 ttl=64 time=0.597 ms
64 bytes from 10.0.0.3: icmp_seq=3 ttl=64 time=0.544 ms
64 bytes from 10.0.0.3: icmp_seq=4 ttl=64 time=0.597 ms
64 bytes from 10.0.0.3: icmp_seq=5 ttl=64 time=0.553 ms
64 bytes from 10.0.0.3: icmp_seq=6 ttl=64 time=0.645 ms
64 bytes from 10.0.0.3: icmp_seq=7 ttl=64 time=0.674 ms
64 bytes from 10.0.0.3: icmp_seq=8 ttl=64 time=0.578 ms
64 bytes from 10.0.0.3: icmp_seq=9 ttl=64 time=0.581 ms
64 bytes from 10.0.0.3: icmp_seq=10 ttl=64 time=0.566 ms
64 bytes from 10.0.0.3: icmp_seq=11 ttl=64 time=0.614 ms
64 bytes from 10.0.0.3: icmp_seq=12 ttl=64 time=0.581 ms
64 bytes from 10.0.0.3: icmp_seq=13 ttl=64 time=0.577 ms
64 bytes from 10.0.0.3: icmp_seq=14 ttl=64 time=0.554 ms
64 bytes from 10.0.0.3: icmp_seq=15 ttl=64 time=0.590 ms
64 bytes from 10.0.0.3: icmp_seq=16 ttl=64 time=0.646 ms
64 bytes from 10.0.0.3: icmp_seq=17 ttl=64 time=0.641 ms
64 bytes from 10.0.0.3: icmp_seq=18 ttl=64 time=0.575 ms
64 bytes from 10.0.0.3: icmp_seq=19 ttl=64 time=0.602 ms
64 bytes from 10.0.0.3: icmp_seq=20 ttl=64 time=0.645 ms
^C
--- raspberrypi.local ping statistics ---
21 packets transmitted, 21 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 0.544/0.625/1.202/0.134 ms
</pre>



 (5.) After Ping your Network, do you will get your current IP from the Mac. Not the IP from your Provider. Then go forward in the same Terminal Window, type your <code> ssh pi@raspberrypi.local </code> the Prompt with your Enter Taste.
 
 <code> ssh pi@raspberrypi.local </code> 
 
 
 (6.) Now do you will get to the ssh RSA Key, if you have one.


<pre>
Space-O-Mac-Pro:~ cybo$ ssh pi@raspberrypi.local
The authenticity of host 'raspberrypi.local (10.0.0.3)' can't be established.
RSA key fingerprint is 7d:b7:30:bb:bc:78:97:da:3e:d8:e7:e7:7f:e4:a6:04.
Are you sure you want to continue connecting (yes/no)?
 </pre>


Then Say Yes/No i typed Yes then i will be forward to the Passwort of my Raspberry. (The Pasword you can set up, by installing your Raspberry PI First Time.



<pre>
Linux raspberrypi 3.18.11+ #781 PREEMPT Tue Apr 21 18:02:18 BST 2015 armv6l

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Mon Sep 28 00:04:24 2015
pi@raspberrypi ~ $
</pre>


(7.) Now :) , you entery and connect your Raspberry PI via Terminal on your Machine. Right After you entry your RaspberryPi via Terminal, you have now to type the Commanline ls to see what is on your Raspberry Pi. As, we can see everything is fit to start the VNC Viewer (Server) prompt this Commandline.

<code> sudo apt-get install tightvncserver </code> 


Don’t be worry this need a while, after that process type Commandline

<code> tightvncserver </code> 


you will get this Information out : Type your Password from your PI. After he ask you about a view-only password. Press (also for me ) No you will get forward to the desktop of your RaspberryPi. This Number after pi:1 is very important for our Viewer :1 This we need it for our VNC Viewer.


<pre> 

You will require a password to access your desktops.

Password: 
Verify:   
Would you like to enter a view-only password (y/n)? no

New 'X' desktop is raspberrypi:1

Creating default startup script /home/pi/.vnc/xstartup
Starting applications specified in /home/pi/.vnc/xstartup
Log file is /home/pi/.vnc/raspberrypi:1.log

</pre>

At last we have to set up the VNC Viewer. Start it by Dopple Click then a Window will show up: In this Window type the scanned and pinged IP Adress also mine is here 10.0.0.3:

Type in that Window The Number 10.0.0.3:1 Then Press Connect in the Interface. Pingo Here is it, you run now Linux RaspberryPi over Mac Os X Machine.
<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="5" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:50.0% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAAGFBMVEUiIiI9PT0eHh4gIB4hIBkcHBwcHBwcHBydr+JQAAAACHRSTlMABA4YHyQsM5jtaMwAAADfSURBVDjL7ZVBEgMhCAQBAf//42xcNbpAqakcM0ftUmFAAIBE81IqBJdS3lS6zs3bIpB9WED3YYXFPmHRfT8sgyrCP1x8uEUxLMzNWElFOYCV6mHWWwMzdPEKHlhLw7NWJqkHc4uIZphavDzA2JPzUDsBZziNae2S6owH8xPmX8G7zzgKEOPUoYHvGz1TBCxMkd3kwNVbU0gKHkx+iZILf77IofhrY1nYFnB/lQPb79drWOyJVa/DAvg9B/rLB4cC+Nqgdz/TvBbBnr6GBReqn/nRmDgaQEej7WhonozjF+Y2I/fZou/qAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://instagram.com/p/8PHK_lTgjl/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">Connect RaspberryPi to your Router via ssh and VNC Viewer! 🎓👾🍇💥 #raspberrypi #router #comnandline #terminal #ssh #vnc #linux #macosx #firewall check out my new post here www.lucasgatsas.ch ;)</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">Ein von Lucas Gatsas (@lucasgatsas) gepostetes Video am <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2015-09-30T01:21:57+00:00">29. Sep 2015 um 18:21 Uhr</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>
