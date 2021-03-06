# mashers's Grid Launcher Updater
This program downloads the latest version of [mashers's Homebrew Launcher with grid layout](https://gbatemp.net/threads/release-homebrew-launcher-with-grid-layout.397527/).

This program uses a modified Lua Player Plus by Rinnegatamante, removing non-essential features to greatly reduce filesize. It is based on [this commit](https://github.com/Rinnegatamante/lpp-3ds/tree/18e32b2f1f10a7466b363ebe9e735a9741d43a1c). The source of this is contained at "`extra/lpp-3ds-strip.zip`". Please see [the original repository](https://github.com/Rinnegatamante/lpp-3ds) for technical details.

The "site" part is meant to download and cache the last version number (`version.h`) and `launcher.zip` from https://github.com/mashers/3ds_hb_menu. This is done because ctrulib can't download from HTTPS sites right now (if there is a way, tell me and I'll forward it).

Some of this was quickly put together and not made to be easily changed for use in the future (it's not that hard though). The server-side code could definitely be optimized in some way, but it fits the purpose for the time being.

If you are setting up a custom updater, the `enable` folder in the site should be password protected.

## How to use
This updater can be added to the grid launcher's settings menu by placing `mglupdate.3dsx` and `index.lua` in `/gridlauncher/update`.

Otherwise, extract it any place you like (e.g. `/3ds/mglupdate`)

Run the program and the program will attempt to show you the latest version available. Press A to download and apply the update.

# License
The `index.lua` script is under the MIT license. Lua Player Plus is under the GPLv3 license.
