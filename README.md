
# ruri.sh

A **fairly quick bash script for macOS** that lets you record your desktop via ffmpeg, convert it to .webm and upload it directly to your favourite pomf.se clone.

I'm using **growlnotify** for the custom notifications. You can find my **Growl skin** [here](https://grassii.github.io/)

## Demonstration

![](images/demo.gif)

[Fullscreen Demo](https://a.pomfe.co/yiyuvla.webm)

## Dependencies

You'll need:

[Growl + growlnotify](http://growl.info/)

[ffmpeg](https://www.ffmpeg.org)
```
brew install ffmpeg --with-libvpx
```

However, you can replace the growl notifications with something like [terminal-notifier](https://github.com/julienXX/terminal-notifier) (which just isn't as aesthetically pleasing as growl since you can't really customize it.

## Setup

Place the script on your **$PATH** and make an alias in your .bashrc or .bash_profile for maximum comfort

```
alias ruri="bash ruri.sh"
```
To find out which audio and video devices you want to record, type
```
ruri -av
```
**[0] Capture screen 0** will be your main display

**[1-999] {Audio device name}** here you can find out which audio device you'd like for ruri to record.

Change the value of the **video** and **audio** variables in ruri.sh (line 4/5) accordingly.
```
#AUDIO/VIDEO

video=0
audio=2
```
You can also change the filehoster in ruri.sh by editing the **host**, **up_url** and **down_url** variables.
```
#FILE HOST
host="pomfe.co"
up_url="https://pomfe.co/upload.php"
down_url="https://a.pomfe.co"
```
[Here's](https://github.com/tsudoko/long-live-pomf/blob/master/long-live-pomf.md) a list of popular pomf.se clones, finding out where the upload.php is located shouldn't be difficult as they're almost all based on the original pomf system.

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
