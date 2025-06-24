### Flatpak repackaging of ZSA Keymapp

#### Build(and install) flatpak from source
```
flatpak run org.flatpak.Builder --force-clean --user --install-deps-from=flathub --repo=repo --install builddir au.id.cocco.packages.flatpak.Keymmap.yaml
```

#### Export standalone installer
```
flatpak build-bundle repo keymapp.flatpak au.id.cocco.packages.flatpak.Keymapp --runtime-repo=https://flathub.org/repo/flathub.flatpakrepo
```

#### Device access
See this for udev rules to make your keyboard accessible to the application:
https://github.com/zsa/wally/wiki/Linux-install#2-create-a-udev-rule-file

Personally I think the rules a little too broad with giving other a lot of access the hidraw etc. In my personal setup
I have a keymapp group that I've added my user to and used them instead of plugdev and only extended the additional
R/W permissions to the group level.
