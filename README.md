# LAMP_LXD_Setup
LAMP Development environment using LXC/LXD.
A simple script that sets up a LAMP development environment under LXC/LXD in Ubuntu.

It sets up a LXC/LXD container environment, creates a LAMP server on a new instance and 
creates a symbolic link from the apache root directory in the container to wherever you want.
This allows you to confortably work on the code from your desktop with your graphic editors 
and visualize the result on real time on the server.

There are only two ways to run the script:
- Without arguments: builds the development environment
- As `LXDLAMP.sh --clean`: deletes the container and the sylink

Everything is default, but you can edit the following variables:
- `CONTAINER_NAME`: name of the container to be created
- `LAMP_DIR`: address to the link that will point to the apache root folder
- `MYSQL_PASSWORD`: the password for the user 'root' in apache

Usage:
```
git clone https://github.com/timothykessler87/LAMP_LXD_Setup
cd LAMP_LXD_Setup && ./LXDLAMP.sh
```
or just
```
wget https://github.com/timothykessler87/LAMP_LXD_Setup/blob/master/LXDLAMP.sh
./LXDLAMP.sh
```

Clean everything:
```
./LXDLAMP.sh --clean
rm -rf LXDLAMP*
sudo aptitude purge lxd
```
