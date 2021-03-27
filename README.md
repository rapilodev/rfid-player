# a simple audio player controlled by RFID cards

After reading an rfid card, an associated audio file is played.
If no file has been assigned yet, an empty folder is created in which audio files can be stored. Multiple audio files in an album folder are played in sequence.

If a network is available, audio streams can be played as .m3ua files. Arbitrary actions can be triggered by shell scripts with the file extension .sh in the folders (e.g.: stop, shutdown, upgrade).
If several audio files of an album are in one folder, they can be navigated by RFID cards.
To register these navigation cards, only one file named NEXT or PREV must be placed in the folder belonging to the card.

This player is based on the idea of https://github.com/MiczFlor/RPi-Jukebox-RFID

## Installation

* install ubuntu server image
* sudo timedatectl set-timezone Europe/Berlin
* dpkg-reconfigure keyboard-configuration
* setup wlan, only needed for audio streaming
* apt-get install -y python3-evdev alsa ffmpeg
* rfid-player can be started by systemd service

