# Description
This project is dedicated for producing **QEMU** windows box.
Replace the ISO URL and ISO checksum for your copy of Windows install.

## Usage:
   $ packer build win10x84-enterprise-eval.json

   ### To start headless:
   $ packer build -var headless=true win10x84-enterprise-eval.json

## Host Requiments:
1. internet connection
1. qemu-system-x86
1. local copy of window 10 ISO files

## Notes:
* use the Autounattend file to create a ready KVM vagrant box.
* turn off window auto update and creates 2 default user.
* This is an evaluation copy, DO NOT include the Product Key.  It will causes "no disk image" error.
* sets up the vagrant
