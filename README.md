# acestream-openelec
Acestream engine for OpenElec / LibreElec on Raspberry Pi (2-3). 

The acestream engine that comes bundled with the plexus addon is a very old version. This results in many acestream links failing to open (this annoying 'Failed to load file' error).
In order to fix that, we 're going to update the acestream engine that's used by Plexus.

The version included currently in this repo is acestream engine: 3.1.19.1.

In order to use this acestream engine the plexus addon is needed. For downloading plexus addon check [this quide](https://seo-michael.co.uk/tutorial-how-to-install-plexus-program-add-on-kodi/).

As soon as plexus addon is installed, we have to replace the bundled acestream engine with the latest one (3.1.19.1) in our case. To do that, issue the following commands:

```bash
# ssh into the rpi (OpenElec / LibreElec)
ssh <kodi ip>
rm -rf ~/.kodi/userdata/addon_data/program.plexus/acestream

# exit from the rpi
exit

# Now we 'll copy the new acestream engine
scp -r acestream <kodi ip>:~/.kodi/userdata/addon_data/program.plexus/
```

Now acestream engine should be working again.
