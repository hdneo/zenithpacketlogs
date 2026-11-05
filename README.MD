## Zenith - The last city (Packet log repo)
This repository is for sharing all your logs you made with the sniffer.

## How to capture

Get the sniffer from the server repository [Zenith the last city server project](https://github.com/hdneo/zeniththelastcityserver/releases).
There is also the source code for the sniffer so you could also check out how it was build.

Follow the [setup instruction](https://github.com/hdneo/zeniththelastcityserver/blob/main/docs/05_Sniffer.md).
Run the sniffer in proxy mode then we get the best results.

So in Administrator Powershell start the sniffer (see docs) after you generate certs and add the hosts entries. 
The hosts entries will redirect the server connection to your local proxy (so if you dont want to use the sniffer anymore just comment out the hosts entries or remove them).


### Sharing a capture
Befor you upload / create a PR a capture please use the Sniffers Export command for it.
The raw files have some have extra sensible data - so the export command removes them properly.


```bash
ZenithSniffer.exe export captures\20261104-210818-proxy-export
```

This creates `…-proxy-export\` and `…-proxy-export.zip` next to it. You are free to upload the zip or the proxy folder. 
You can just add it to the root of this git project.
If there is one file bigger than 100 MB and the zip is less than 100 MB - just add only the zip of it.

IF you upload the folder pls add a content.txt and explain short what you made in the game and what you captured.
It doesnt need a long text just something like "killed some mobs, did some quests, teleport".
It is also ok if you do it as a commit message if you dont want to add the file or just forget it. 

### What to capture ?
Near everything that is relevant. Do actions often.
It will be hard to replicate the world as it was but as more packet logs exists we could run parsers later over it to get most of the server data.
Quests will be a bit harder but play as much as you can. 

2 Player actions would be nice to have from different captures also PvP battles.


