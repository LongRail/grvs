
Debian
====================
This directory contains files used to package grvsd/grvs-qt
for Debian-based Linux systems. If you compile grvsd/grvs-qt yourself, there are some useful files here.

## grvs: URI support ##


grvs-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install grvs-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your grvsqt binary to `/usr/bin`
and the `../../share/pixmaps/grvs128.png` to `/usr/share/pixmaps`

grvs-qt.protocol (KDE)

