﻿# My Twich Command Tool
[Download Latest Release](https://github.com/Revingbell/my-twitch-video-and-sound-commands/releases) (download the archive of your choice and unpack it where you want in your filesystem).

*Read this in another language: [English](README.md), [Français](README.fr.md).*

## How to use:

### Update Config File From v1.1.0
Put your old `config.js` file inside the `js` folder, then open the file `updateConfigFile.html` in the web browser of your choice.  
You will be prompted to download the updated version of the file, save it inside the `js` folder. You can start using v1.2.0.

### Add video and sound files
Put all video files in the `videos` folder, and all sounds in the `sounds` folder.

### Parametrize the program
Open the file `myCommandEditor.html` with your preferred web browser (Tested on Firefox).  

#### Global Parameters
![image](https://user-images.githubusercontent.com/17751686/128336117-d0a7a07d-1f85-469d-af53-374cd0847b49.png)
- `Twitch Channel` : Name of the channel. The program will look for commands starting with a ! in this channel's chat.
Mandatory for this program to work.
- `Chat User` : Name of the user (you or a bot account created specifically) that will write in chat.
Required only for `Bot Commands` to work.
- `Oauth Password String` : Connect to the link: [Get your oauth password key](https://twitchapps.com/tmi/) with the account specified as 'Chat User' to get the authentication key. Never provide this key to anyone. In case of doubt, go back to the link to generate a new one and invalidate the old one. Required only for `Bot Commands` to work.

#### Video Parameters
![image](https://user-images.githubusercontent.com/17751686/128336328-6d53f906-15c6-461f-ae5a-4f9194717ff9.png)
- `Pause Videos Command` : Command string to pause videos. This command will only respond to the channel owner. 
- `Resume Videos Command` : Command string to resume videos. This command will only respond to the channel owner. 
- `Global Video Delay` : Minimum delay between two videos in seconds. If any video has a longer duration than this delay, its duration will be used instead of this value. 
- Videos:
  -  `Command` : Command that triggers the video.
  -  `File Name` : Name of the video file you've put in the `videos` folder.
  -  `Delay` : Minimum delay between two uses of this particular command, in seconds.
  -  `Volume` : Volume of the video, value between 0 and 1. ( decimals with a `.` )

#### Sound Parameters
![image](https://user-images.githubusercontent.com/17751686/128336399-e77b5d6d-79ba-4ccd-bd5f-5910a1410c3b.png)
- `Pause Sounds Command` : Command string to pause sounds. This command will only respond to the channel owner. 
- `Resume Sounds Command` : Command string to resume sounds. This command will only respond to the channel owner. 
- `Global Sound Delay` : Minimum delay between two sounds in seconds. If any video has a longer duration than this delay, its duration will be used instead of this value. 
- Videos:
  -  `Command` : Command that triggers the sound (preceded by a !).
  -  `File Name` : Name of the sound file you've put in the `sounds` folder.
  -  `Delay` : Minimum delay between two uses of this particular command, in seconds.
  -  `Volume` : Volume of the sound, value between 0 and 1. ( decimals with a `.` )


#### Bot Commands
![image](https://user-images.githubusercontent.com/17751686/128336451-b39d61c8-8271-49f7-97ff-da6ecd60abfd.png)
- Bot Commands
  -  `Command` : Command that triggers the bot message.
  -  `Ouput` : Message the bot will send after the command is used. You can use '{username}' as a variable that will be substituted for the name of the user sending the command.

#### Export
Hit this button to download the new version of your `config.js` file, replace it inside your `js` folder.

## Add to OBS

Then as a last step, add the `myCommandTool.html` as an internet source in OBS:

![image](https://user-images.githubusercontent.com/17751686/127782022-b564ccdc-45b1-4810-9643-6fcc72134265.png)
