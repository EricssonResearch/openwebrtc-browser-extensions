OpenWebRTC browser extensions
=============================

Add WebRTC support to existing browsers using OpenWebRTC

## Step 1 - Running the daemon
OpenWebRTC browser extensions communicates with the *daemon* via its local web server. Before any page load, extensions fetch JavaScript from the daemon containing WebRTC functionality. The daemon runs in a separate process in the backgound. Start the daemon by:
```
./openwebrtc/out/x86_64-apple-darwin/bin/daemon
```
Note that you need to [build](https://github.com/EricssonResearch/openwebrtc#building) OpenWebRTC first. In this example we run it on OS X, but the daemon is also available on Linux.

## Step 2 - Installing extensions

### Safari
Currently we only provide a Safari extension.

### Firefox

[Greasemonkey](https://github.com/greasemonkey/greasemonkey/)
