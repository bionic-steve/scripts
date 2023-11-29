Some various scripts and things I use for misc functions, like downloading porn
;)

these will all be linux scripts, most likely bash or python

I run Fedora linux with the i3 window manager.  I started using i3 years ago on
arch based on a youtube video from Luke Smith - https://youtu.be/GKviflL9XeI?si=UmCulLvwoN0MRcpS
He called his i3 configuration "larbs" and I've been using and modifying it
ever since.

# newsboat helper scripts
His i3wm config came with a console based rss reader called newsboat and his
"linkhandler" script to handle opening links from within newsboat.

in newsboat's config file, you can configure its "browser" to be a script to open links
associated with an rss feed item

~~~
$ grep linkhandler .config/newsboat/config
browser linkhandler
macro i set browser "linkhandler %u %F"; open-in-browser ; set browser linkhandler
~~~

I cut the cable cord years ago and I get 90% of my tv/movie content using
sonarr/radarr - these track the media and will use "indexers" to grab the files
and download via either usenet (via .nzb files), or bittorrent.   Many of these
indexers also provide rss feeds for their content, so newsboat can be
configured with a rss feed for the latest movie releases, latest music
releases, latest XXX releases, etc ...

My version of linkhandler has an extra case stanza to handle nzb files and
routes the nzb links to a script called getnzb to download the nzb file and
feed it into the usenet downloader , e.g. sabnzbd

