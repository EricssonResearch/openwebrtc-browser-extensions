OpenWebRTC browser extensions
=============================

Add WebRTC support to existing browsers using OpenWebRTC

## Step 1 - Running the daemon
OpenWebRTC browser extensions communicates with the *daemon* via its local web server. Before any page load, extensions fetch JavaScript from the daemon containing WebRTC functionality and injects it in to the current context. The daemon runs in a separate process in the backgound. 

Start the daemon by running:
```
./openwebrtc/out/x86_64-apple-darwin/bin/daemon
```
Note that you need to [build](https://github.com/EricssonResearch/openwebrtc#building) OpenWebRTC first. In this example we run it on OS X, but the daemon is also available on Linux.

## Step 2 - Installing extensions

### Safari
Currently we only provide a Safari extension, just  [download](https://github.com/EricssonResearch/openwebrtc-browser-extensions/blob/master/safari/OpenWebRTC.safariextz) and doubleclick.

If you want to modify the extension you need to use the Extension Builder in Safari:

![Safari screenshot](https://github.com/EricssonResearch/openwebrtc-browser-extensions/blob/master/imgs/safari_screenshot.png)

### Firefox
Even though Firefox already has WebRTC support you may want to use OpenWebRTC as a backend. You should be able to use a [Greasemonkey](https://github.com/greasemonkey/greasemonkey/) script and quite easily inject code like this:

```
var script = document.createElement("script");
script.src = "http://localhost:10717/owr.js";
document.head.appendChild(script);
```
