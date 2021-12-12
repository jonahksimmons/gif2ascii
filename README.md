# gif2ascii
Converts gif formated files into a directory of ascii frames that can be animated at a variable frame rate.
This was a copy and slight modification of https://github.com/avanishsubbiah/termimation-save-frames
I just added in error handling, seperated converter and animator, and a few other minor tweeks that were bugging me.

## Instalation
sudo make install

## Usage
### gif2ascii
Usage: gif2ascii [FILE]

Coverts each frame of FILE to an ascii frame in directory ./FILE-ascii/.

### animateDir
Usage: animateDir [DIRECTORY] [FRAME_RATE]

Animates the contents of files in DIRECTORY at FRAME_RATE (default is 24fps).

Examples:

animateDir d		Animates the contents of d at 24fps

animateDir g 60		Animates the contents of g at 60fps


## Dependecies
- bash
- coreutils
- ffmpeg (or imagemagick as a fallback)
- jp2a (or libcaca as a fallback)
- bc
- zsh (for some math in the animator, but that can be changed)
