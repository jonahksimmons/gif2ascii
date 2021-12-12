# gif2ascii
Converts gif formated files into a directory of ascii frames that can be animated at a variable frame rate.
This was a copy and slight modification of https://github.com/avanishsubbiah/termimation-save-frames
I just added in error handling, seperated converter and animator, and a few other minor tweeks that were bugging me.

## Instalation
git clone https://github.com/jonahksimmons/gif2ascii
cd gif2ascii
sudo make install

## Usage
### gif2ascii
Usage: gif2ascii [FILE]

Coverts each frame of FILE to an ascii frame in directory ./FILE-ascii/.

### animateDir
Usage: animateDir [DIRECTORY] [FRAME_RATE]

Animates the contents of files in DIRECTORY at FRAME_RATE (default is 24fps).

Examples:

animateDir example

animateDir g 60


## Dependecies
- bash
- coreutils
- ffmpeg (or imagemagick as a fallback)
- jp2a (or libcaca as a fallback)
- bc
- zsh (for some math in the animator, but that can be changed)
