This file will explains how to add information to JSON file for Ship.<br/>
Feel free to open an issue if you have any question, if you want to contribute just open a pull request.

## Allowed submissions
The only characters not allowed is the main character of the anime (or the graph would just be a big star)<br/>
Please submit images where there are only the 2 characters on it

## How to submit

A JSON file is made of the following (while reading this, you can have a look at [one of the file](https://github.com/Xwilarg/Ship_data/blob/master/kancolle.json) to understand what I'm saying):
- name: Name of the anime
- color: Color of the node that will display characters from this anime
- ships: All the ships and their relationships

Ships are ranked in alphabetic order, so if you have two characters called Satsuki and Nagatsuki being linked together, you'll do:
```json
"nagatsuki": {
  "satsuki":  [{
  }]
},
```
If you want to add an entry, make sure it's not already here (you can just Ctrl+F to check if your link isn't already here)

The remaining "ship" values are:
- isNsfw: 0: Not NSFW, 1: Slighly NSFW (erotic but not too explicit), 2: NSFW
- linkType: Where you link is from. Please use the website where the art was originally from (so don't post things from Gelbooru, Rule34 etc, check the source of the image instead, it's often written in the post)
- link: Link to the image
- artist: Name of the artist
- imageId: (Only for NHentai) Id of the cover of the doujinshi (please make not that it's not the id of the doujinshi! You can get it by going on the cover and copying the link of the image, it's the number inside it)
