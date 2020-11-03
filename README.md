# Plymouth Themes
The repository contains themes which can be used as boot animations in Linux distributions.
The themes have been tested on Ubuntu 16.04 LTE and Debian 10 Buster.

<!--![Mario](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/mario.gif)
![ECorp-Spinner](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/ecorp_spinner.gif)
![ECorp-Glitch](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/ecorp_glitch.gif)
![Mr-Robot](https://github.com/hrishabh23/plymouth-themes/blob/master/gifs/mr-robot.gif) -->

**NOTE:** The animations are smoother than they appear here in gifs. I was lazy when I was creating gif frames. 

Name | Theme GIF | Name | Theme GIF
---- | --------- | ---- | ---------
Mario | <img src="/gifs/mario.gif" width="640"/> | ECorp-Spinner | <img src="/gifs/ecorp_spinner.gif" width="640"/>
ECorp-Glitch | <img src="/gifs/ecorp_glitch.gif" width="640"/> | Mr-Robot | <img src="/gifs/mr-robot.gif" width="640"/>
Stalker | <img src="/gifs/stalker.gif" width="640"/> | |

## Getting Started

### The Plymouth theme directory
Find out the repository in which the Plymouth themes are located.
In Debian-based distributions this is,
```
/usr/share/plymouth/themes/
```
This command can be used to find out the path to the directory, in which files with the extension `.plymouth` are located:
```
find /usr/ -name '*.plymouth'
```
**NOTE:** If the directory containing the plymouth themes is not `/usr/share/plymouth/themes/`, corresponding changes will be needed in the paths mentioned in `.plymouth` file of the theme that is downloaded from here.

### Copying files to Plymouth theme directory
Copy the directory corresponding to the desired Plymouth Theme into the themes repository.
Super user privileges will be required.

### Update initramfs
**Easy way:**
List all the plymouth themes installed:
```
sudo plymouth-set-default-theme -l
```
This will print a list of themes that are present in the default plymouth theme directory. To choose a one:
```
sudo plymouth-set-default-theme -R THEME
```
Where THEME refers to one of the listed values from the executed command.

**Alternative:**
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

No copyright infringement intended.

Mario is owned by Nintendo.

Mr. Robot is owned by USA Network.
