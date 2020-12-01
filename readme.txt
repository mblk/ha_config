#
# docker
#

docker stop ha

docker rm ha

docker pull homeassistant/raspberrypi3-homeassistant:stable



docker run --init -it --name="ha" -v /etc/localtime:/etc/localtime:ro -v /home/pi/ha_config:/config --net=host --restart=always --device /dev/ttyACM0 --device /dev/serial/by-id/usb-dresden_elektronik_ingenieurtechnik_GmbH_ConBee_II_DE2231123-if00 --device /dev/vchiq homeassistant/raspberrypi3-homeassistant:stable

docker run --init -d --name="ha" -v /etc/localtime:/etc/localtime:ro -v /home/pi/ha_config:/config --net=host --restart=always --device /dev/ttyACM0 --device /dev/serial/by-id/usb-dresden_elektronik_ingenieurtechnik_GmbH_ConBee_II_DE2231123-if00 --device /dev/vchiq homeassistant/raspberrypi3-homeassistant:stable


#
# ...
#
