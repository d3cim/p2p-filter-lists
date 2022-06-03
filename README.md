p2p-filter-lists
================

Download several lists from https://www.iblocklist.com/lists and concatenate them into one `.p2p` file. Particularly useful for qBottirrent, but can be used for other softwares too.

This type of file can be directly loaded in several Bittorrent clients like qBittorent, Ktorrent or others... Currently, these lists are downloaded, but you can easily add or remove some by editing the script:

- level1
- level2
- level3
- ads
- badpeers
- bogon
- edu
- pedophile
- rangetest
- spyware

For Linux
=========

You can simply run the script `dl-p2p-lists.sh`. The final file will be created in `/tmp/qbittorrent_lists_$USER.p2p`.

For Windows
===========

You can run the script by simply double clicking on `dl-p2p-lists.vbs`. Nothing visible will happen until it is finished (1 or more minutes depending on your Internet connection), where a popup will show telling you the script is finished.

For Windows, you need the `bin` folder as it contains an executable for `wget`, to download the lists.

The created file will be located in `%TEMP%\qbittorrent\list.p2p`, so usually in `C:\Users\<username>\AppData\Local\Temp\qbittorrent\list.p2p`.

**NOTE:** Compared to the Linux script, nothing is parallelized (one download and one extraction at a time). Moreover, for some reasons, the Windows script adds a lot of duplicated lines in the final file. So you may think that the Linux script is missing stuff, but it is more like the reverse. Anyway, it still works fine enough.

With qBittorrent
================

You can setup the path to the created link in *Tools -> Options... -> Connections*. At the bottom of the page, you have the section *IP filtering* where you can put the correct path, that depends on your OS (see above).

Every now and then (like every 2 days), you can run the script, and once it is finished, simply refresh the IP filtering in qBittorrent by clicking on the green arrow.
