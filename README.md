# spotify-qt packages

Debian bookworm packages for spotify-qt  
  
++spotify-qt:  
An unofficial Spotify client using Qt as a simpler, lighter alternative to the official client. Please note that you need an actual Spotify client running, for example librespot, which can be configured from within the app.
Note: Controlling playback requires Spotify Premium.  
Goals:  
Fast, light on resources, and small file size.  
Portable, and supporting as many platforms and architectures as possible.  
Customizable.  
https://github.com/kraxarn/spotify-qt  
+-------------------------------------------------  
  
I builded these packages because they are not in debian 12 repository; and I don't want to use the infamous snap version. Besides, there is only a 64bits Appimage (which I prefer over snap) version of spotifyqt.  

x64,i386 & armhf packages provided.  
  
# installation:  
  
download appropriate package, and do (for example for 32bits package):  
  
```
sudo apt install ./spotify-qt-v3.11_i386.deb
```
(or install with graphical .deb installer if you have one, for example QSI installer for q4os: left click the .deb, then 'open with' and choose QSI installer)  
  

# spotify-qt configuration:  
At first start it will ask you for your "Client ID" and "Client Secret"; to obtain these keys do this:  
open https://developer.spotify.com/dashboard/  
create a new application  
goto edit settings in the app overview  
add http://localhost:8888 in Redirect URIs section  
  
Then grab your client ID and client Secret and you will be able to loggin :)  
  
Then go to settings:  
settings >> interface >> titlebar : uncheck 'Application titlebar'  
(it'a a matter of taste, but I prefer if the app use the default windows decorations of my os)  
settings >> interface >> general >> toolbar position : bottom  
(a matter of taste once again)    
  
There are great chances you intend to play music locally, to do so you need to install spotifyd (packages for debian 12 here: https://github.com/seb3773/spotifyd-packages ) or librespot.  
Once done, go to settings:  
(config example for spotifyd)  
settings >> spotify >> general : librespot or spotifyd path : /bin/spotifyd  
settings >> spotify >> general : check 'start with app' & 'always start'  
settings >> spotify >> configuration : additional arguments: -b pulseaudio  
(I recommend pulseaudio, but you can use alsa too)  
Of course, you'll have to put your username in settings >> spotify >> configuration, or alternatively, you can use a config file for spotifyd. (more infos here: https://github.com/seb3773/spotifyd-packages )
  
  
+-----+






