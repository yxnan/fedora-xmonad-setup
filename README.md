# My XMonad Setup on Fedora Workstation

This `xmonad.hs` is based on [DistroTube's setup](https://gitlab.com/dwt1/dotfiles/-/blob/master/.xmonad/xmonad.hs).

## Setup procedures

1. Grab [GHCup](https://www.haskell.org/ghcup/)

1. Install XMonad compiling dependencies

	```bash
	sudo dnf install gmp-devel libX11-devel libXrandr-devel libXScrnSaver-devel
	```

1. Compile XMonad and Contrib extensions

	```bash
	cabal install xmonad
	cabal install --lib xmonad-contrib
	```
1. Install XMonad from distro repository to get a better system integrity

	```bash
	sudo dnf install xmonad
	```
1. Install utilities

	```bash
	# X11 utilities
	sudo dnf install xrdb xset xsettingsd xdotool

	# compton:      compositor
	# xmobar:       status bar
	# alacritty:    terminal emulator
	# fish:         shell
	# dmenu:        dynamic menu for X
	# slock:        screen lock0
	# pactl:        volume control
	# light:        brightness adjust
	# fehbg:        wallpaper setting
	# lxappearance: gtk2 app theme setting
	sudo dnf install compton xmobar alacritty fish dmenu slock xdotool pulseaudio-utils light feh lxappearance

	# import RPM Sphere repository to get trayer
	# RPM Fusion is enabled by default in Fedora 35 Desktop,
	# so we can directly grab the `rpmsphere-release` package
	# from their website: https://rpmsphere.github.io/
	# After adding this repo, install trayer by:
	sudo dnf install trayer
	```
Almost done!

## Some other Apps I use
|Package Name | Usage|
|---|---|
|gnome-keyring | Secret Service|
|keepassxc | Password Manager|
|polkit-gnome | Graphical Authentication Agent|
|kdeconnectd | Mobile Phone Control|
|shutter | Screenshot & Editing Tool|

## Fonts I use
1. WenQuanYi Micro Hei (for CJK UI)
1. Font Awesome (for icons)
1. Fira Code
1. Mononoki Nerd Font
1. Sarasa Gothic