# ARAudioPlayer

_for emily_

AR-ONLY version of the XRAudioPlayer component (XRMediaPlayer)

**_ARAudioPlayer_** generates an audio player that users can experience in web AR or traditional flat modes. Experiences are built using Three.js/AFrame.

View content using a wide range of devices and formats. Implement the module in both modular server-side and non-modular client-side applications with just a few lines of JavaScript code!

## Usage:

[Server-side](#server-side)

[Client-side](#client-side)

### Server-Side
 1. install using npm
```javascript
npm install araudioplayer
```
 2. import araudioplayer (using require is recommended: not all releases of Node have the newest ES6 features enabled by default)

 (a) using add method
```javascript
var XRMP = require('araudioplayer');
var myPlayer = XRMP.ARAudioPlayer;

myPlayer.add('../media/img/OracularSpectacular.png', '../media/audio/TheYouth.mp3' , { title: 'The Youth', author: 'MGMT', year: 2007});

myPlayer.add('../media/img/ExtraFine.png', '../media/audio/ExtraFine.mp3', { title: 'Extra Fine', author: 'Starmaker', year: 2019});

myPlayer.spawn();
```
 (b) using addFromList method


an object or array of objects in the following format can be processed by the module to generate same outcome as above

```javascript
var XRMP = require('araudioplayer');
var myPlayer = XRMP.ARAudioPlayer;

var collection = {
    'The Youth': {
        coverURL: '../media/audio/TheYouth.png',
        audioURL: '../media/audio/TheYouth.mp3',
        {
            title: 'The Youth',
            author: 'MGMT',
            year: 2007
        }
    },
    'Extra Fine': {
        coverURL: '../media/audio/ExtraFine.png',
        audioURL: '../media/audio/ExtraFine.mp3',
        {
            title: 'Extra Fine',
            author: 'Starmaker',
            year: 2019
        }
    }
};

myPlayer.addFromList(collection);
myPlayer.spawn();
```

### Client-Side

1. download the boilerplate or make your own test directory
2. move to the app.js or index.js level of the directory and create a test.js file
3. implement as follows:

```javascript
var myPlayer = new ARAudioPlayer();
myPlayer.build();

myPlayer.add('../media/img/OracularSpectacular.png', '../media/audio/TheYouth.mp3' , { title: 'The Youth', author: 'MGMT', year: 2007});

coreEventListeners.launch([myPlayer]);
```

### Full API


| property       | type   | description |
| ------------- |:-------------:| -----:|
| type          | string       | short paragraph descriptor of type property |
| socket        | object        |  short paragraph descriptor of socket object |
| hello         | method        | short paragraph descriptor of hello method|
| buildCoreMarkup | method        | short paragraph descriptor of buildCoreMarkup method|
| spawn         | method        | short paragraph descriptor of spawn method|
| assetsContainer | object        | short paragraph descriptor of assetContainer object |
| build         | method        | short paragraph descriptor of build method |
| add           | method        | short paragraph descriptor of add method |
| addFromList   | method        | short paragraph descriptor of addFromList method |
| showTrackList | method        | short paragraph descriptor of showTrackList method |
| playNextTrack | method        | short paragraph descriptor of playNextTrack method |
| playPreviousTrack | method  |  short paragraph descriptor of playPreviousTrack method |
| stream        | method        | short paragraph descriptor of type method |
| application   | object        | short paragraph descriptor of type object |
| view          | string        | short paragraph descriptor of type property |
| XRSetting     | string        | short paragraph descriptor of type property |