# Audacious-WebUI
Web UI for Audacious media player

STATUS: Still experimental, and assumes that Audacious is NOT running under the same user ID as the web server. Requires some knowledge of SSH and key management to enable one user to act as the other.

REQUIREMENTS: Requires CGI enabled on the web server. Tested on Apache2 running on Raspberry Pi 1.

USAGE: User navigates to /cgi-bin/nowplaying in a browser, and javascript-enabled buttons/playlists will make ajax calls to other CGI scripts as requested to play/pause, skip tracks forward/backward, turn shuffle/repeat on/off, change to another playlist.
