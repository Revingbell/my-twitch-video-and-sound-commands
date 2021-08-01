﻿# my-twitch-video-and-sound-commands

## How to use:
In the file `correspondance.js`, modify this line:
```js
var streamer = 'revingbell';
```
Put in your streamer id inside the quotes.

Put all video files in the `videos` folder, and all sounds in the `sounds` folder.

Then, still in the file `correspondance.js` the json string is described as follows:
```js
var correspondanceJson = JSON.parse(`
{
	"videos": [
		{
			"command": 	"societe", // command as it will be typed in the chat
			"file":		"societe.mp4", // name of the associated video file you've put in the videos folder
			"delay": 	"60", // duration before next use in seconds
			"volume": 	"0.5" // volume value between 0 and 1
		},
		{
			"command": 	"societe2",
			"file":		"societe.mp4",
			"delay": 	"60",
			"volume": 	"1"
		},
    ...
    {
    ...
    } // no "," after the last entry
	],
	"sounds": [
		{
			"command": 	"thereyouare", // command as it will be typed in the chat
			"file": 	"there_you_are.wav", // name of the associated sound file you've put in the sounds folder
			"delay": 	"30", // duration before next use in seconds
			"volume": 	"0.5" // volume value between 0 and 1
		},    
		{
			"command": 	"thereyouare2",
			"file": 	"there_you_are.wav",
			"delay": 	"3000",
			"volume": 	"0.7"
		},
    ...
    {
    ...
    } // no "," after the last entry
	]
}
```
