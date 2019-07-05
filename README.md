# Description
This project is dedicated for producing **QEMU** windows box.

## Usage
   $ packer build win10x84-enterprise-eval.json
   
   to start headless:
   $ packer build -var headless=true win10x84-enterprise-eval.json

## Host Requiments:
1. internet connection
1. qemu-system-x86

## note
This setup use the Autounattend file to create a ready KVM vagrant box. It automatically update window image and creates 2 default user.
