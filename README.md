
## UPDATE November 29th, 2016
After a looooonnnggg hiatus, (tbh i forgot about this project) today i already updated to support latest version of NWJS 0.18.8
it also add tray icon.
!!! winstate.js (save window position) is still not working due to NWJS, for the time being i use screen width and height to automatically place the window.
Last but not least, if this widget is dead (no contribution) i will make my own widget based from akiroz idea by using NWJS
## Live2D-Widget
a little cross-platform desktop widget based on the Live2D Sample App in the SDK

[nw.js](https://github.com/nwjs/nw.js) builds are avaliable on [http://nwjs.io/](http://nwjs.io/)

![](https://raw.githubusercontent.com/akiroz/Live2D-Widget/master/screenshot.png)

### Usage:
* adjust window size in package.json
* move: look
* scroll: zoom
* l-click: touch
* r-click: context menu - change models, always on top, and exit

### Install (Windows/Linux):
1. extract the right nw.js package to the root directory
2. optionally edit package.json for window size
3. run `nw(.exe)`

### Install (Mac OS):
1. rename the root directory to `app.nw`
2. put it inside `nwjs.app/Contents/Resources/`
3. optionally edit package.json for window size
4. run `nwjs.app`

### Add/Remove Models:
1. put/delete model folder inside `assets/`
2. (add only) inspect your `*.model.json`, make sure it implements the `idle` motion
3. (add only) optionally implement the `tap_body` motion with proper `hit_areas` defined
4. (add only) if the model doesn't fit properly inside your window, add/edit the `layout` section inside `*.model.json`

   (see `assets/haru/haru.model.json` for reference)

### Troubleshooting
* Gettiing audio to work: 2 possible solutions.
    * follow this [guide](https://github.com/nwjs/nw.js/wiki/Using-MP3-%26-MP4-%28H.264%29-using-the--video--%26--audio--tags.) to get MP3 in nw.js
    * convert all audio to Vorbis (ogg/oga)

### Issues/Todo:
* transparency in linux doesn't work unless GPU is disabled but WebGL requires GPU
* transparency in Mac OS will show a visible title string
