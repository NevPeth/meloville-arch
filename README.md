# Meloville for Arch Linux

This repository contains the Arch Linux `PKGBUILD` for [Meloville](https://github.com/NevPeth/meloville).

Meloville is a native Linux music player designed to look modern.

## Installation

### 1. Clone this repository

```bash
git clone https://github.com/NevPeth/meloville-arch
cd meloville-arch
```

### 2. Build the package

Run:

```bash
makepkg -si
```

For those unfamiliar this will automatically add it to pacman, so you can simply do sudo pacman -R meloville-git to uninstall it. (Make sure to put the -git as this directly pulls from the github)

## Updating

To install a newer version, pull the latest packaging files and rebuild:

```bash
cd meloville-arch
git pull
makepkg -si
```

If the `PKGBUILD` has been updated to a newer version, `makepkg` will build the new package and `pacman` will install it.

## Upstream Project

Meloville's source code is maintained separately:

https://github.com/NevPeth/meloville

This repository is only for the Arch Linux packaging.
