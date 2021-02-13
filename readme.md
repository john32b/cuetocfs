## CUE to CFS

This is an accompanying tool to my PS1 Mednafen Launcher [PSXMED](https://github.com/john32b/psxmed) 

It will convert `CUE/BIN` CD games to **Compact File Set** (`.cfs`) archives, while **encoding audio** tracks of the CD to **Vorbis 80kbps**. This is mainly for use in **Mednafen**. An emulator of multiple systems that supports mounting CDs with VORBIS encoded audio tracks. Also `.cfs` archives are great because they offer LZMA compression and can be mounted in Windows with the tool [Pismo File Mount](https://pismotec.com/download/).

:ballot_box_with_check: So the while idea of this, is to minimize the size of CD games, while they are still in a playable format, without the need to be extracted first.

:new: It can now read .cue from within **.ZIP FILES** so you can skip the step of extracting a ZIP to get the contents.

#### Example

For the PlayStation Game **"IN THE HUNT"**

- Original Cue/Bin : **589MB** *(This game has 29 Audio Tracks)*

- Converted to CFS : **39.6MB** (*All audio tracks encoded to Vorbis, and then everything into a single .cfs archive*)

  

## Running

There is no standard install procedure. But there are some **requirements** :

- NodeJS. https://nodejs.org/
- FFMPEG, installed and set on your path. https://ffmpeg.org/ 
  - This is for the Vorbis Encoding to work
- PISMO File Mount https://pismotec.com/download/
  - Get the `Pismo File Mount Audit Package build` and install it
  - It should install the `ptiso.exe`  tool in the program installation. This is the one I need to create cfs archives
- Basic windows terminal and NodeJS knowledge

##### Getting it:

- In this repo, clone or download. The main executable is **cuetocfs.js** 

##### Running it:

On a windows terminal, go to where you put the files and  
 `node cuetocfs`

This will just run the program, but it needs parameters. use `node cuetocfs -help` for help

##### Examples

`node cuetocfs c:\ps1\game.cue`

`node cuetocfs c:\ps1\*.cue`

`node cuetocfs c:\ps1\*.zip`

`node cuetocfs c:\ps1\*.m3u -o c:\converted`

## ABOUT

This is just a one-off thing. No license.

John32B 2020