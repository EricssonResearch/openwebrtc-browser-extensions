OpenWebRTC browser extensions communicate with the *daemon* via its local web server. Before any page load, extensions fetch JavaScript from the daemon containing WebRTC functionality and injects it in to the current context. The daemon runs in a separate process in the background.

This repository is a simple browser extension that does that for Safari.

You can find details about installation and running [on the OpenWebRTC wiki](https://github.com/EricssonResearch/openwebrtc/wiki/Running-and-Testing#the-daemon) but you can [download the plugin here](https://github.com/EricssonResearch/openwebrtc-browser-extensions/raw/master/safari/OpenWebRTC.safariextz).

The code that gets injected, for the suspicious of you out there, [is this](https://github.com/EricssonResearch/openwebrtc-browser-extensions/blob/master/safari/OpenWebRTC.safariextension/bootstrap.js).


The result is WebRTC in Safari:

![Safari gUM screenshot](https://github.com/EricssonResearch/openwebrtc-browser-extensions/blob/master/imgs/safari_gum.png)

If you want to modify the extension you need to use the Extension Builder in Safari:

![Safari screenshot](https://github.com/EricssonResearch/openwebrtc-browser-extensions/blob/master/imgs/safari_screenshot.png)
