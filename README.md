# rpi_config
collection of config files for automating the setup of a raspberry pi instance

# assumptions
* this script installs the latest version of raspbian-lite
* SD-Card is called mmcblk0
* script is executed as USER ; sudo is installed

## flash_sd-card
* retrieves rpi_latest.img from raspberrypi.org if it doesnt exists already
* flashes the rpi_latest.img to the sd-card
* enables SSH
* enables WIFI

## on_pi
for hardening and improving security the following steps are taken
!!! Please change the hard-coded, insecure password to your needs before executing the script !!!

### user
* change username
* change hostname
* change passwd
* lock root account
### ssh
* enable key-based auth
* only allow unprivileged user to authenticate
### networking
* firewall
* log login attempts with respective IP-address
