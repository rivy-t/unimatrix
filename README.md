# UniMatrix

Python script to emulate some display from "Ghost in the Shell" (also featured in "The Matrix") in a terminal. Uses Braille unicode characters by default, but can use custom character sets. Accepts keyboard controls while running.

Merges some pull requests ignored by original maintainer will8211 of UniMatrix, itself based on CMatrix by Chris Allegretta and Abishek V. Ashok. The following option should produce virtually the same output as CMatrix:

```
$ unimatrix -n -l o
```

## Why use this

### Pros
- pretty
- easy to modify
- frequency of character sets has been normalized (with the original code, it became very apparent when using all 20k or so Chinese chars and ie. Klingon, that there would be a very unequal distribution ; with this fork, specifying '`-l zBB` will statistially give you twice as many Klingon chars as Chinese ones)

### Cons
- uses quite a bit of resources

## Install

Cloning the repos is good, since it gives you Klingon fonts (they shouldn't really be here, but since they are... must be installed manually to `/usr/sharefonts/klingon/`)

Linux users can also use curl to install:
```
sudo curl -L https://raw.githubusercontent.com/petaflot/unimatrix/master/unimatrix.py -o /usr/local/bin/unimatrix
sudo chmod a+rx /usr/local/bin/unimatrix
```
If you do not have curl, you can alternatively use a recent wget:
```
sudo wget https://raw.githubusercontent.com/petaflot/unimatrix/master/unimatrix.py -O /usr/local/bin/unimatrix
sudo chmod a+rx /usr/local/bin/unimatrix
```
You can also install it with pip:
```
pip install git+https://github.com/petaflot/unimatrix.git
```

Users of Arch-based distros can get it from the AUR as ```unimatrix-git```, although it might not be the most recent version.

## Screenshots

Default settings:

![screenshot1](/screenshot1.png?raw=true "Default")


Blue with custom character set 'Linux' (```$ unimatrix -c blue -u 'Linux'```):

![screenshot2](/screenshot2.png?raw=true "Custom character set")


Yellow with alternate character set: Emoji (```$ unimatrix -c yellow -l 'e'```):

![screenshot3](/screenshot3.png?raw=true "Alternate character set: Emoji")


Emulating CMatrix (```unimatrix -n -s 96 -l 'o'```):

![screenshot4](/screenshot4.png?raw=true "Emulating CMatrix")


## License
Typing `unimatrix --help` will give you access to the full list of options

## License

Unimatrix is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

Unimatrix is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License at <http://www.gnu.org/licenses/> for more details.
