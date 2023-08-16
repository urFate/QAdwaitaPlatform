QAdwaitaPlatform
==========

<div align="center">
    <img alt="AUR version" src="https://img.shields.io/aur/version/qadwaitaplatform-qt6-git?style=flat-square&logo=archlinux&label=AUR">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues/urFate/QAdwaitaPlatform?style=flat-square">
    <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/urFate/QAdwaitaPlatform?style=flat-square">
    <img alt="GitHub" src="https://img.shields.io/github/license/urFate/QAdwaitaPlatform?style=flat-square">
</div>

<h3 align="center">The project was abandoned and is now unmaintained due to irrelevance. It is recommended to use an alternative in the form of <a href="https://github.com/FedoraQt/QAdwaitaDecorations">QAdwaitaDecorations</a>.</h3>
<p align="center">QAdwaitaPlatform is QGnomePlatform fork that implements modern LibAdwaita window decoration look to Qt applications.</p>

## Result

| ![](https://camo.githubusercontent.com/3824639d74ec1e1c6b14b52c8509a15f723113de8643e961e0283e180619176c/68747470733a2f2f692e696d6775722e636f6d2f6931777a6279582e706e67) | ![](https://camo.githubusercontent.com/ccf8ae7f5623b6ab3c77a2633c991b232b9271e0f67f2d726137440a6259a860/68747470733a2f2f692e696d6775722e636f6d2f68785367514c562e706e67) |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <p align="center">🌑 Dark Scheme</p>                                                                                                                                    | <p align="center">☀️ Light Scheme</p>                                                                                                                                   |


## How to compile

This library uses private Qt headers and will likely not be forward nor backward compatible. This library will have to be recompiled with every Qt update.

### Step-by-step guide
1. Create 2 directories for Qt 5 and Qt 6 builds

    `mkdir build-qt6 build-qt5`
2. Change the directory to one of the previously created ones, **depending on for which version of Qt you are building**. (e.g. `cd build-qt6`)
3. Run cmake command

    `cmake -DUSE_QT6=false ..` - for Qt 5 build
    
    `cmake -DUSE_QT6=true ..` - for Qt 6 build
4. Build & install QAdwaitaPlatform

    `make && sudo make install`

### Build dependencies
Packages names are depends on what distribution are you using. There is list for ArchLinux below.
- adwaita-qt6, adwaita-qt5
- qt6-wayland, qt5-wayland, qt5-quickcontrols2
- cmake, git, gtk3

## Usage

This library is used automatically in Gtk based desktops such as Gnome, Cinnamon or Xfce.

This platform theme can also be used by setting the QT_QPA_PLATFORMTHEME environment variable to "gnome". For example, put the following command in `.bashrc`:

```
export QT_QPA_PLATFORMTHEME='gnome'
```

## License
Most code is under [LGPL 2.1](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.en.html) with the "or any later version" clause. New code should be contributed under this license.

This project also incorporates some code from the Qt Project. Because of that the so-called combined work is licensed under [LGPL 3.0-only](https://www.gnu.org/licenses/lgpl-3.0), [GPL 2.0](https://www.gnu.org/licenses/old-licenses/gpl-2.0), [GPL 3.0](https://www.gnu.org/licenses/gpl-3.0), or any later GPL version approved by the [KDE Free Qt Foundation](https://kde.org/community/whatiskde/kdefreeqtfoundation/).
