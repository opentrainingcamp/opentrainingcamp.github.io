# The working envirement for our training camps

## Optimum

A Linux distrubution (as we are using mainly Ubuntu latest versions) with

### Necessary

1. git
2. > jdk8
3. Maven
4. Netbeans
5. gcc (for C)
6. VS code (an open source visual studio by Windows)

### Options

## On a Windows host

We will use a virtual machine with a Linux (non graphic) distribution (an ubuntu LTS server)

So we will need (for praparing the ubuntu install)

1. VirtualBox
2. VirtualBox gest extention (for mounting a sharing directory between windows and the Linux server)
3. virtualbox extention pack
4. An ubuntu iso

Then install ubuntu (We can give you an prepared image)

2) Install neccessary stuff in your appliance:

apt-get update
apt-get install dkms build-essential linux-headers-$(uname -r)
3) Mount the Guest Addons in VirtualBox. If using the default VBox Extension Pack this is done in the VBox appliance window via Devices >> Install Guest Addons. If you have used another source and downloaded an ISO it can be mounted in the usual VBox way.

Notes: By default VirtualBox no longer includes the VirtualBox Extension Pack but it can be downloaded from here (if you haven't already). Others have reported issues with the default version previously (although this version worked for me). Older (and OS specific) official VBox Guest Addons ISOs can be found here. There is also a user supplied Ubuntu one available via Launchpad - have a look here.

4) Mount the Guest Addons in your appliance. As automounting is disabled in TKL, once you have the ISO mounted (through the VBox interface) you will also need to mount the 'cdrom' within TKL:

mount /dev/cdrom /mnt
5) Install the Guest Addons. Change directory to the mounted ISO and run the VBox addons installer:

cd /mnt
./VBoxLinuxAdditions.run --nox11
Note: You can safely ignore the following error:

Installing the Window System drivers ...fail!
(Could not find the X.Org or XFree86 Window System.)


