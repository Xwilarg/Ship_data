This file will explains how to add information to JSON file for Ship.<br/>
Feel free to open an issue if you have any question, if you want to contribute just open a pull request.

## Allowed submissions
- Don't add the main character in the list (like the Teitoku for KanColle or the Doctor for Arknights), this it to avoid the graph to just be a big star
- Try to find the original source of the image. If you take if from Gelbooru, the original source is often written in the post page
- Try not to include fetichisms that are too weird, I won't make a full list so please try to use your common sence for this one
- Try to keep nodes linked together, this is to avoid having lot of nodes flying everywhere
- Try to have have the 2 characters on the image

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
- linkType: Where you link is from. Please use the website where the art was originally from
- link: Link to the image
- artist: Name of the artist
- imageId: (Only for NHentai, Twitter and Gelbooru) Id of the cover of the doujinshi (please make not that it's not the id of the doujinshi! You can get it by going on the cover and copying the link of the image, it's the number inside it)
- comment (Only for Gelbooru) explanation why Gelbooru is used
