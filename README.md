## ruri

A **shitty bash script for macOS** that lets you record your desktop via ffmpeg, convert it to .webm and upload it directly to your favourite pomf.se clone

## Usage

place the script on your $PATH and make an alias in your .bashrc file for maximum comfort



```
ruri [filename] [-args]
```

Arguments:
```
-h:     Opens the help menu (this)
-s:     Record sound output
-60:    Switch to 60fps (Default: 30fps) NOTE: not currently compatible with -s
-720p:  Switch to 720p (Default: 1080p)

-c:     Convert + [filename]
```
