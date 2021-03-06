# Alexa_YouTube Skill
Play Youtube Music via Alexa Echo.
Alexa_YouTube skill makes it easy to play music and playlist from YouTube.

## How to install ##
**IMPORTANT:** Download the latest release version (ZIP file) from [HERE](https://github.com/reger-men/Alexa_YouTube/releases) and upload it in AWS.

[![Alt text](https://img.youtube.com/vi/xr8Mt6yWTBg/0.jpg)](https://www.youtube.com/watch?v=xr8Mt6yWTBg)

Click on the image above to watch the video.

## Features ##
User ...
* ... doesn't need a YouTube account to groove this skill
* ... doesn't have to wait until video is completely downloaded
* ... can easily create and modify playlists
  * Playlists are identified by numbers 
    * ``` Alexa ask youtube for playlist {NUMBER}```
  * Playlists file contains only the ID of the songs and thus remains quite small
  
## Dependencies ##
Youtube API: This skills need Youtube PI service to access on Videos on Youtube for this purpose, the web app https://youtube-alexa.herokuapp.com/ was created. Of course you can also use other services or create new one. 

This WebApp runs on a private server, the corresponding source code can be found [here](https://github.com/reger-men/YoutubeAPI)

## Set your language ## 
Currently this skill supports the 4 languages **en-US, de-DE, fr-FR, it-IT**

Set the language you want to use in ```var lang = "en-US";``` into ``` index.js```

## Expand with your language ## 
The new release make it easy to expand any language you want without changing the source code in ``` index.js```. Following are the steps you should take:
1. Copy one of the existing interaction models file and replace the intent with your language (you need to compile your model)
2. insert your language block into ``` responses.js``` 
3. set your language in ``` index.js``` ``` var lang = "en-US";``` 

## Commands examples ## 
* To play song with title {title}
  * ``` Alexa ask youtube for {title}```
* To insert the current Song in the PlayList number {number}
  * ``` Alexa ask youtube for add to playlist {number}```
* To Remove song from the current PlayList 
  * ``` Alexa ask youtube for remove from playlist```
* To remove PlaList number {number}
  * ``` Alexa ask youtube for remove playlist {number}```
* To play the next song of the current PlayList:
  * ``` Alexa next```
* To get all playlists back
  * ``` Alexa ask youtube for show all playlists```
  
## Development Links ##
[Alexa Developer Console](https://developer.amazon.com/alexa/console/ask)

[AWS Lambda](https://eu-west-1.console.aws.amazon.com/lambda)

## Notes ##
Please note that the aws ```/tmp/``` folder is a non-persistent scratch area. This means that your Playlists are only temporarily stored in it. To solve that, please use an other storage service or your own server storage.
This repository is based off of this original [skill](https://github.com/dmhacker/alexa-youtube-skill)
