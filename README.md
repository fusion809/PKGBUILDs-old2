# Arch PKGBUILDs
This repository is composed of PKGBUILDs I have written (or modified from existing packages in the Arch Build Service and Arch User Repository) to help me install packages not in the AUR or pacman repos, or in the case of packages already in either class of repository, these PKGBUILDs have amendments to make them better suit my purposes. The contents of this repository are licensed under GPLv3. This repository was set up prior to when I set up my **Open Build Service Arch_Extra Branch** (**OBSAEB**) in March 2016. Most PKGBUILDs in this repository ended up being moved to this branch. The only exceptions are those that for whatever reason are unsuitable for my OBSAEB.

## Atom
The `atom-editor` package in this repository is designed to not fail, in its build, due to minor Internet connectivity issues which would stump the PKGBUILD in the AUR. The `atom-editor-beta` package, unlike that in the AUR, should also persevere despite intermittent network connectivity issues and **can** be installed alongside `atom-editor` on the same machine. These two packages require Internet access during their build, so I cannot add them to my OBSAEB.

## Linux / Linux Firmware
The `linux`/`linux-firmware` packages are here, as I know sometimes even the [testing] repo of Arch Linux falls behind the latest releases of the Linux kernel.

## Vim
I have also included Vim-related packages, as [Vim updates](https://github.com/vim/vim/releases) come out daily or even hourly, so it is unrealistic to expect the maintainers of the `gvim` and `vim` packages at https://www.archlinux.org/packages/extra/x86_64/gvim and https://www.archlinux.org/packages/extra/x86_64/vim, respectively, to keep them constantly up-to-date. To install the latest gVim using this repository I recommend you run:

```bash
git clone https://github.com/fusion809/PKGBUILDs
cd PKGBUILDs/gvim-git
makepkg -si --noconfirm
```

The `gvim-git` package in this repository is a combination of the `gvim-git` and `vim-runtime-git` packages in the AUR. I merged these packages to save bandwidth and disk space, as both PKGBUILDs clone the same [GitHub repository](https://github.com/vim/vim). Likewise the `gvim` package in this repository is also a combination of the `gvim` and `vim-runtime` packages in the `[extra]` pacman repository, except it is updated more frequently. I have also added the `gvim` package to my [OBSAEB](https://build.opensuse.org/package/show/home:fusion809:arch_extra/gvim) it is also here because the OBS usually takes several hours before any commits I push there will result in an updated package in this repository.
