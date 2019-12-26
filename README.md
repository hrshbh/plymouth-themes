# Plymouth Themes
The repository contains themes which can be used as boot animations in linux distributions.
The themes have been tested on Ubuntu 16.04 LTE.

![Mario](https://github.com/hrishabh23/plymouth-themes/tree/master/mario/gimp/mario.gif)

## Getting Started

### Finding the Plymouth theme directory
Firstly, it is required to know the repository in which the Plymouth themes are located.
In Ubuntu 16.04 LTE, this directory is
```
/usr/share/plymouth/themes/
```
If themes are placed in other directory, make sure to change the path in the respective `.plymouth` file, downloaded from this repository.
Maybe use:
```
find /usr/ -name '*.plymouth'
```

### Copying files to Plymouth theme directory
Copy any of the folders in this repository into the themes repository.
Super user privileges will be required.

### Update grub
Run these commands to choose the new theme as default
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
* Mario sprites by Kevin Huff at stupidsonic@yahoo.com

Copyright Infringement not Intended.
Mario is owned by Nintendo
Mr. Robot is owned by USA Network
