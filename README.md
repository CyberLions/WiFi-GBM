# Create a captive portal
1. Download the nodogsplash plugin from the router configuration page
2. SSH into the router using ssh -oHostKeyAlgorithms=+ssh-rsa root@192.168.8.1
3. Create the nodogsplash.conf file in /etc/nodogsplash
4. Edit the splash.html file in /etc/nodogsplash/htdocs with the provided splash.html file
5. Copy Penn State logo using `scp -O -oHostKeyAlgorithms=+ssh-rsa psulogoforincommon-456x150.png root@192.168.8.1:/etc/nodogs`

#Create the evil twin
1. Download airgeddon using `git clone --depth 1 https://github.com/v1s1t0r1sh3r3/airgeddon.git`
2. Download the required dependencies and run using `sudo bash airgeddon.sh -i'
3. Select your Alfa adapter from the menu
4. Place it in monitor mode
5. Select evil twin attacks -> evil twin with captive portal
6. Scan for WiFi networks and select your WiFi network
7. Select Deauth aireplay attack
8. Do not do DOS pursit or Spoof MAC address
9. Select the handshake file you have previously captured
10. Contine with setup, choose english and advanced captive portal
11. Default evil twin captive portal will spin up
12. Change to `/tmp/ag1/www` on your attack machine
13. Change the contents of index.htm to the provided index.htm file
14. Again copy Penn State logo into pwd, `/tmp/ag1/www`
15. View captive portal at the gateway ip address `192.168.8.1`
