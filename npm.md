

New installation
Download from: https://nodejs.org/en/download/ 
This installs both node.js and npm

To update existing npm
```npm install npm -g```
or
```npm install npm@latest -g```
Check https://stackoverflow.com/questions/34408154/what-exactly-does-npm-install-g-do
for ```-g``` switch.

To check version: ```npm -v```

To check latest version of npm:
https://www.npmjs.com/package/npm

## Nodejs Update

To check latest version of node.js
https://nodejs.org/en/

### nvm for windows

https://github.com/coreybutler/nvm-windows/releases
```nvm -v```

run this with admin right
```setx /m NVM_HOME D:\0dev\tools\nvm```

Not working, need to manually do it ( Seems permission problem, need to run installer wth admin right)
```
mklink /D D:\0dev\tools\nodejs D:\0dev\tools\nvm\v19.5.0
rmdir D:\0dev\tools\nodejs
```

create a settings.txt in the executable folder with the following content
```
root: D:\0dev\tools\nvm
path: D:\0dev\tools\nodejs
arch: 64
proxy: none
```
Then run the following (assume 19.6.0 is the new version installed).

```
nvm on
nvm install latest
nvm list
nvm use 19.6.0
```

Now node has the new version.

To fix permission, we need security policy change:
https://www.itechtics.com/enable-gpedit-windows-10-home/
https://www.itechtics.com/easily-enable-group-policy-editor-gpedit-msc-in-windows-10-home-edition/
https://www.tenforums.com/general-support/111678-local-security-policy-editor-not-found.html

Or follow these, to install with admin right
- https://www.c-sharpcorner.com/article/installing-node-version-manager/
- https://www.freecodecamp.org/news/set-up-windows-for-nodejs-development-with-nvm/


### Mac and Linux
This is a better option of nvm since npm can handle it without extra package nvm.

This does not work in Windows

```
node -v
npm cache clean -f
npm install -g n
or
n stable
or
n latest
or
n [version.number]
```