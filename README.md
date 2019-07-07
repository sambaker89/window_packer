# Description
This project is dedicated for producing **QEMU** windows box.
Replace the ISO URL and ISO checksum for your copy of Windows install.

### Setting up environment variables:
    $ export PACKER_LOG = "1"
    $ export PACKER_LOG_PATH = "logs/packerlog.log"
    $ export TMPDIR = "tmp/"

## Usage:
    $ packer build win10x84-desktop-qemu.json

   ### To start headless:
    $ packer build -var headless=true -var version=0.1.2 win10x84-enterprise-eval.json

## Available builders:
1. win10x64-desktop-qemu.json - winrm, kvm image only
1. win10x64-enterpirse-eval.json - winrm, vagran box ready and no KVM image
1. win2012r2-standard-eval-qemu-ssh.json - KVM image only
1. win2016-standard-eval-qemu-ssh.json - KVM image only

## Host Requiments:
1. internet connection
1. qemu-system-x86
1. local copy of window 10 ISO files

## Notes:
* use the Autounattend.xml to create a ready KVM image
* turn off window auto update and creates a default user.
* This is an evaluation copy, DO NOT include the Product Key.  It will causes "no disk image" error.
