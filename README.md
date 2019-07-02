# Plymouth Themes
The repository contains themes which can be used as boot animations in linux distributions.
The themes have been tested on Ubuntu 16.04 LTE.

![gif](https://github.com/hrishabh23/plymouth-themes/tree/master/mario/gimp/mario.gif)

## Getting Started

### Finding the Plymouth theme directory
Firstly, it is required to know the repository in which the Plymouth themes are located.
In Ubuntu 16.04 LTE, this directory is
```
/usr/share/plymouth/themes/
```
to find the repository, run
```
locate plymouth/themes
```
in bash. Filter out the results, most of them will be files.

### Copying files to Plymouth theme directory
Copy any of the folders in this repository (currently only one, mario) into the themes repository.
Super user privileges will be required.

### Update grub
Run these commands to choose the new theme as deafult
```
sudo update-alternatives --config default.plymouth
```
Then choose the index against the name of the newly copied theme. Then run:
```
sudo update-initramfs -u
```
Done.

### Acknowledgments
* Amazing tutorials by Charlie Brej on Creating Plymouth themes. Can be found [here](https://brej.org/blog/?p=158)
* Sprites by Kevin Huff at stupidsonic@yahoo.com

Mario is a copyright of Nintendo
