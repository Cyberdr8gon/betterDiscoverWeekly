# betterDiscoverWeekly

## Build Instructions:

Currently, it doesn't do much, and I plan on writing python/shell/whatever tools to do builds for us.
For the most part compiling works like this:

(most of this is done so we have a future build order)

FIRST.
1. be sure you have nvm installed for your system. Use it to download node 7.0.0 (current version we are using), then tell nvm to use 7.0.0.
2. If you don't have node-gyp installed, evoke `npm install -g node-gyp` (if you are on linux/Mac OS you *might* have to use sudo commands if node doesn't use user directories)

NEXT. 
1. cd into addons, run `node-gyp configure` This creates makefiles/visual studio project for the addon to compile. 
2. cd into build, then run make if you are on a *nix system or open the project config and compile with visual studio.

This will generate a _whateverAddon_.node that we can use as a nodeJS addon directly in our JS by requiring. Currently, we don't have a tool to automatically move the node addon into the coreApp because it has no function. Eventually this will all be automated with a tool.

FINALLY.
1. cd down to the root of the project, cd into coreApp
2. run `npm install`
3. run 'npm start'

You will see what we have so far. More soon....
