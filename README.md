Flatpak repackaging of ZSA Keymapp

Build(and isntall) flatpak from source
```
flatpak build-bundle repo keymapp.flatpak au.id.cocco.packages.flatpak.Keymapp --runtime-repo=https://flathub.org/repo/flathub.flatpakrepo
```
Export standalone installer
```
flatpak build-bundle repo hello.flatpak org.flatpak.Hello --runtime-repo=https://flathub.org/repo/flathub.flatpakrepo
```
