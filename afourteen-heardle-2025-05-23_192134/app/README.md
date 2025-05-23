# youtube-heardle-template2

A template for a Youtube based Heardle (instead of Soundcloud)

Original code [here](https://github.com/sarvarghese/heardle-template)

HOW TO MAKE YOUR OWN HEARDLE

1. Remix this project to create your own copy of the code
1. Settings -> Edit Project Details -> customize the name and description
1. Open `main.js` and modify the values in the CUSTOMIZATION section at the top of the file


## About the songList

- The song list can be as many entries as you wish. Just add more lines.
- The songs in the list must follow the format:
  
```
{ arist: "artist name", name: "song name", youtubeId: "Youtube ID" },
```

- To get the ID of a Youtube link, click the **Share** button and copy the text after the **youtu.be/** 
    
    e.g., in **https://youtu.be/dQw4w9WgXcQ**, the ID would be **dQw4w9WgXcQ**

## About the icon_url

You can upload an icon image to the Assets section of your project, which will show up as your site's icon if you bookmark it.

A square image is recommended.

Once you have uploaded the image, you can get it's URL and set the `icon_url` value in `main.js`

## Notes

- The order of the songs match the order that the Heardles will appear, so if you want to play, maybe best to have someone shuffle them for you!

- Glitch auto-saves your code, so your changes should be available as soon as the code is edited.

## Known Issues

- Sometimes the play button doesnt work because the Youtube video might not be available.

## Extra Nerd Notes

If you're familiar with command-line utilities, there's a quick way to get a list of all the URLs in a Youtube playlist using [yt-dlp](https://github.com/yt-dlp/yt-dlp) and [jq](https://github.com/jqlang/jq)

```
yt-dlp --dump-json --flat-playlist "https://www.youtube.com/playlist?list=SOME_PLAYLIST_ID" | jq -r '"\(.title)\nhttps://youtu.be/\(.id)\n"'
```

Which you can output to a file by putting `> file.txt` on the end of that command.