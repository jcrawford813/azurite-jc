# Custom Atomic Image "Azurite"

This is my personal atomic image that I use to build my own flavor of Fedora Kinote (KDE Atomic). I have taken the latest (Version 40, as of right now) Kinoite image, removed Firefox, and added the following:

- Distrobox
- QEMU, libVirt, and virt-manager
- RPM Fusion Repos for libheif
- Kate (the Flatpak is non-existant)
- Gwenview (Doesn't support heic from iPhones in the Flatpak)
- Okular
- Fish
- Custom Wallpapers from UBlue (I really like the dinosaurs)

I was inspired and used (*ahem* stole) the setup from Jorge Castro, based on his post [here](https://www.ypsidanger.com/building-your-own-fedora-silverblue-image/). As such, feel free to take this work and build your own. If you'd like to just use this image, without any support, guarantees, or warranty, you can do the following:

First, do an install of the latest version of Kinoite or Silverblue, and perform a full update:

```
rpm-ostree update
systemctl reboot
```

Then you can rebase to this untrusted image:
```
rpm-ostree rebase --experimental ostree-unverified-registry:ghcr.io/jcrawford813/azurite-jc:latest
systemctl reboot
```

Note that all of the above need to be done as root.

The Action rebuilds the image every night, so it should remain relatively up-to-date. I will change the image from time to time based on my personal needs.