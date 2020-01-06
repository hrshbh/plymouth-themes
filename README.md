# Plymouth Themes
The repository contains themes which can be used as boot animations in linux distributions.
The themes have been tested on Ubuntu 16.04 LTE.

![Mario](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/mario.gif)
![ECorp-Spinner](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/ecorp_spinner.gif)
![ECorp-Glitch](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/ecorp_glitch.gif)
![Mr-Robot](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/mr-robot.gif)

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
Copy the directory corresponding to the desired Plymouth Theme into the themes repository.
Super user privileges will be required.

### Update grub
To install this new theme:
```
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/"path/to-your-plymouth.plymouth" 100
```
Remember to replace "path/to-your-plymouth.plymouth" with the corresponding file with extension `.plymouth`. Change the paths in the above command correspondingly, if the Plymouth Theme directory is not `/usr/share/plymouth/themes/`.

Run these commands to choose among the installed themes:
```
sudo update-alternatives --config default.plymouth
```
Then choose the index against the name of the newly copied theme. Then run:
```
sudo update-initramfs -u
```
Done.

### Acknowledgments
* Amazing blogs by Charlie Brej on Creating Plymouth themes.
   [Part 1](https://brej.org/blog/?p=158),
   [Part 2](https://brej.org/blog/?p=174),
   [Part 3](https://brej.org/blog/?p=197),
   [Part 4](https://brej.org/blog/?p=238)
* Mario sprites by Kevin Huff at stupidsonic@yahoo.com

Copyright Infringement not Intended.

Mario is owned by Nintendo

Mr. Robot is owned by USA Network
