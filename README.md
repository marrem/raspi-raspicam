# RaspiMJPEG as a service

## Install raspimjpeg

* Most recent fork as of writing: https://github.com/nickolas360/raspimjpeg
* clone repo
* build: `make` `sudo make install`
* raspimjpeg binary should now be in /usr/local/bin

* copy raspimjpeg.config to /etc
* copy prepareRaspimjpeg to /usr/local/bin
* copy camraspimjpeg.service to /etc/systemd/system

* sudo systemctl daemon-reload
* sudo systemctl enable camraspimjpeg.service
* sudo systemctl start camraspimjpeg.service

* with values from config as in this repo, images should now be written in /dev/shm (ramdisk)


## Using images

You can install mjpeg-streamer to use the written images and publish them as a mjpeg stream, so 
you can use the raspberry-pi as a regular webcam



