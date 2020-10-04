The documentation apply to files that are inside the "custom" folder

This file will explains how to add information to JSON file for Ship.<br/>
Feel free to open an issue if you have any question, if you want to contribute just open a pull request.

## Allowed submissions
- Don't add the main character in the list (like the Teitoku for KanColle or the Doctor for Arknights), this it to avoid the graph to just be a big star
- Try to find the original source of the image. If you take if from Gelbooru, the original source is often written in the post page
- Try not to include fetichisms that are too weird, I won't make a full list so please try to use your common sence for this one
- Try to keep nodes linked together, this is to avoid having lot of nodes flying everywhere
- Try to have have more than 2 characters on the image
- Don't post official arts, the goal is to display ships made by the community

## How to submit

There are 3 kinds of files:
 - names.json: Contains all the animes we have information about
 - crosseover.json: Contains crossover ships
 - All the others: All the ships between one anime

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
(In crossover.json, names are in the format animeName_characterName)<br/>
If you want to add an entry, make sure it's not already here (you can just Ctrl+F to check if your link isn't already here)

The remaining "ship" values are:
- isNsfw: 0: Not NSFW, 1: Slighly NSFW (erotic but not too explicit), 2: NSFW
- linkType: Where you link is from. Please use the website where the art was originally from
- link: Link to the image
- artist: Name of the artist
- imageId: (optional) Id of the cover of the doujinshi (please make not that it's not the id of the doujinshi! You can get it by going on the cover and copying the link of the image, it's the number inside it)
- comment (optional) explanation why Gelbooru is used
- fallback (optional) Gelbooru link to the image (in case the original image is deleted)

## How to get these values
### Gelbooru
Example: Asashimo x Kiyoshimo<br/>
Origin post: https://gelbooru.com/index.php?page=post&s=view&id=4795435

 - nsfw: 0 (the image is not NSFW)
 - linkType: "gelbooru"
 - link: "https://gelbooru.com/index.php?page=post&s=view&id=4795435" (the link to the post, remove everything after "id=XXXXXXX")
 - imageId: "https://img2.gelbooru.com/images/34/05/3405a69234e639ef18679a6168ab5641.jpg" (Scroll down and click on Original Image to get this link)
 - comment: "Image no longer available on Pixiv" (Why you weren't able to get the image from its original source)

### Pixiv
Example: Hatsushimo x Kiso<br/>
Original post: https://www.pixiv.net/en/artworks/53568062

 - nsfw: 0 (the image is not NSFW)
 - linkType: "pixiv"
 - link: "https://www.pixiv.net/en/artworks/53568062" (the link to the post)
 - artist: "ＺＡＫＩ" (the artist that made the image, you can find it on the top right of the image)
 - fallback: "https://gelbooru.com/index.php?page=post&s=view&id=2935258" (the link of the image on Gelbooru)
 
### Twitter
Example: Akebono x Shoukaku<br/>
Original post: https://twitter.com/atusi_2225/status/663005670233370624

 - nsfw: 0 (the image is not NSFW)
 - linkType: "twitter",
 - link: "https://twitter.com/atusi_2225/status/663005670233370624" (the link to the post)
 - imageId: "CTN4JJgUYAE7DY3" (click on the image then right click on the displayed image and copy the link. Your new link will looks like https://pbs.twimg.com/media/XXXXXXXXXX?format=XXX&name=XXXXXX , we want the part between "media/" and "?format="
 - artist: "atusi_2225" (you can easily get it from the post link, between "twitter.com/" and "/status"
 - fallback: "https://gelbooru.com/index.php?page=post&s=view&id=2920561" (the link of the image on Gelbooru)
 
### Deviantart
Example: Jeanne d'arc x Mami Tomoe<br/>
Original post: https://www.deviantart.com/hiwonoafu/art/Jeanne-x-Mami-472520728

 - nsfw: 0 (the image is not NSFW)
 - linkType: "deviantart"
 - link: "https://www.deviantart.com/hiwonoafu/art/Jeanne-x-Mami-472520728" (the link to the post)
 - imageId: "https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/2ef3c01a[...]KasFzQzvk" (not fully displayed in the example because it takes a lot of space, do a right click on the image and copy its URL

### Shikotch
Same as Deviantart but linkType is "shikotch" 

### Yandere
Same as Gelbooru but linkType is "yandere"
