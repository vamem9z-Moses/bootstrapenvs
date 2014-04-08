To create a new precise image:

Requirements: On Fedora 20+ you will need gnupg and debbootstrap installed.

1. Run sudo debootstrap --arch amd64 --keyring=ubuntu-keyring-2012.05.19/keyrings/ubuntu-archive-keyring.gpg precise precise
2. If you have the ubuntu is downloaded you use it instead of having the debootstrap download it:
	a. sudo mount -t iso9660 -o loop /home/mmiles/Downloads/ubuntu-12.04.4-server-amd64.iso /mnt/iso
	b. sudo debootstrap --arch amd64 --keyring=ubuntu-keyring-2012.05.19/keyrings/ubuntu-archive-keyring.gpg precise precise file:/mnt/iso 


This will create a new precise chroot in the precise directory using the keyring downloaded from: http://archive.ubuntu.com/ubuntu/pool/main/u/ubuntu-keyring/


