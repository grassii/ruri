# ruri

A **shitty bash script for macOS** that lets you record your desktop via ffmpeg, convert it to .webm and upload it directly to your favourite pomf.se clone

## Setup

place the script on your **$PATH** and make an alias in your .bashrc or .bash_profile for maximum comfort

```
alias ruri="bash ruri.sh"
```
To find out which audio and video devices you want to record, type



## Usage

```
ruri [filename] [-args]
```

Arguments:
```
-h:     Opens the help menu (this)
-av:    Lists audio/video devices
-s:     Records audio output (Default: no audio)
-60:    Switches to 60fps (Default: 30fps) NOTE: not currently compatible with -s
-720p:  Switches to 720p (Default: 1080p)

-c:     Convert + [filename]
```
