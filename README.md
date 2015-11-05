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


5. After Ping your Network, do you will get your current IP from the Mac. Not the IP from your Provider. Then go forward in the same Terminal Window, type your <code> ssh pi@raspberrypi.local </code> the Prompt with your Enter Taste.
