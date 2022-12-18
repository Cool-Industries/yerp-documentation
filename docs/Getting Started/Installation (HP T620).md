**Install Home Assistant:**

1.  Install SSD and RAM into your T620
2.  Install HA Supervised by flashing it to a SSD with an adapter (skip to step 7 if you have this, otherwise continue to do it via live boot)
3.  Put a Linux distro of your choice onto a USB (I like to use Ventoy for plenty of options)
4.  Boot into that distro, install BalenaEtcher, grab the current URL for the Home Assistant .img.gz for x86 from the Home Assistant github
5.  Open BalenaEtcher and copy the .img.gz to the internal disk
6.  Restart the T620, remove the USB
7.  Once the command line interface comes up, you need to get the thing online. Ethernet is the best option here, but if you need wifi that needs to be configured via prompt. It'll be something like:
    `network update wl1ps0 --wifi-ssid "NETWORK_NAME" --wifi-mode wpa-psa --wifi-key password --wifi-dhcp auto`
    ..and then it should update and connect. If it says successful you can type `network info`, look for something in there with the wifi SSID. Also if you use the `exit` command, HA will show you the welcome message again, that has the IP the machine was assigned.
8.  Do a reset on the thing: `host reboot`
9.  Once the welcome screen comes up again, your instance should come up in a web browser. If you had a  keyboard and monitor or KVM, etc. plugged in, you can disconnect them now, everything else will be done via browser (or shell, optionally).
10. Pull up that URL and take a break, HA needs a few minutes to get ready. *(If this takes over 20 minutes, there's likely something wrong with your install. The easiest fix is starting over, cloning a new image onto your SSD.)*

**Configure Home Assistant**

1.  Once you've got an account set up for yourself, go to your settings page (it's your name, lower left corner) and turn on advanced mode. You may also want to set dark mode for yourself, that's here too.
2.  Head to Settings %3E Add-On's; we've got quite a few to install. Some of these need others for their own installation processes, so an order like this should help:
    Studio Code Server (or File Editor), SSH & Web Terminal (or the other SSH one, if you don't mind doing some commands via shell outside of the browser), Mosquitto Broker, MariaDB, InfluxDB, Nginx Proxy Manager, VLC.
    And then these ones as well, which require you to add their repos first: Zigbee2MQTT, PicoTTS, Cloudflared
3.  OK, time to configure all of these. I'll link some youtube walkthroughs here.
4.  Head to Settings > Integrations to Set up Mosquitto and core-vlc.
5.  [Install HACS](https://hacs.xyz/docs/setup/download/). You can wait on resetting since you'll have to in a second for the next step:
6.  [Set up PicoTTS](https://www.home-assistant.io/integrations/picotts/), via editor. Reset.

*incomplete, but posted for viewing / feedback / contributions>)