# simple audio player box controlled by RFID cards

Scanning a rfid card creates a folder with its ID.
To assign an action to the card, put a file into this folder:
* a media file will be played out.
* a .m3ua file can be used to start playing an network audio stream (requires running network).
* a .sh script will trigger any scripted action (for example: stop, shutdown, upgrade)

based on the idea of https://github.com/MiczFlor/RPi-Jukebox-RFID

## Installation

* install ubuntu server image
* sudo timedatectl set-timezone Europe/Berlin
* dpkg-reconfigure keyboard-configuration
* setup wlan, only needed for audio streaming
* apt-get install -y python3-evdev alsa ffmpeg
* rfid-player can be started by systemd service

