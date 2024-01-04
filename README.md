# Audacious-WebUI
Web UI for Audacious media player

## STATUS
Still experimental, and assumes that Audacious is NOT running under the same user ID as the web server. Requires some knowledge of SSH and key management to enable one user to act as the other.

## REQUIREMENTS
Requires CGI enabled on the web server. Tested on Apache2 running on Raspberry Pi 1.

## SETUP
- Copy the files in 'cgi-bin' to your cgi-bin directory. Copy the files in 'images' to '/images/buttons'
- Edit the audtool and playlist-select scripts, replacing $AUDUSER and $AUDUSER_HOME with the username and home directory of the user running the media player. 
- Generate an rsa key pair, with the private key in the SSH directory of the user running the web server, and the public key in the SSH authorized_keys file of the user running the media player (yes, it probably would have been better to just run the media player as the same user for the web server).

## USAGE
User navigates to /cgi-bin/nowplaying in a browser, and javascript-enabled buttons/playlists will make ajax calls to other CGI scripts as requested to play/pause, skip tracks forward/backward, turn shuffle/repeat on/off, change to another playlist.
