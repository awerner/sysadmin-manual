# Setup of Debian 9 on a Lenovo Thinkpad 470

## Preparation

Grab a copy of the current Netinstall ISO, at the time of writing it can be found at [https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-9.2.1-amd64-netinst.iso](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-9.2.1-amd64-netinst.iso)

Image an empty CD or USB stick with that ISO - how to do that depends on your current operating system and is out of scope for this guide.

Enter the EFI of the the notebook and make sure that `Secure Boot` under the `Security Tab` is set to `Disabled` .

Insert your created boot medium and reboot.

## Booting the Installer

In the `Debian GNU/Linux installer boot menu` select `Install`.

Select your native Language, Country and  Keyboard layout in the next dialogues.

Make sure your network cable is connected to the notebook before confiriming the Keyboard selection, as the Installer will try to auto-detect the network in the next step.

Now enter the hostname for your new laptop, and your domain name in the next dialogue. If you have a local network, set your domain name to `local` or another name that identifies your network.

Now leave the fields for the `root`password blank twice. This tells the Installer to disable the root login, and your User that will be created afterwards will be granted sudo-rights.

Enter your Full Name \(not username\), and on the next page your desired username. Provide a secure password twice.

## Partitioning the disk

Select the 



