# archlinux-wine


Useful packages to run Windows games & apps flawlessly on Arch-based distros (Endeavour, Manjaro, Artix etc).

---

## Graphics

If you cannot open some Steam Games with Proton or Lutris, you must install/update your gpu graphics driver.

Source: [here](https://github.com/NoXPhasma/protondb_faq/wiki/Graphics-driver-installation)

Please check [here](https://en.wikipedia.org/wiki/Vulkan_(API)#Compatibility) if your GPU support Vulkan in general! If not then your game will not work with DXVK or vkd3d.

### Intel
```sh-session
sudo pacman -S --needed lib32-vulkan-intel vulkan-intel lib32-mesa lib32-vulkan-icd-loader vulkan-tools llvm lib32-llvm lib32-llvm-libs llvm-libs vulkan-icd-loader
```

### NVIDIA
```sh-session
sudo pacman -S --needed lib32-nvidia-utils lib32-opencl-nvidia opencl-nvidia nvidia nvidia-utils
```

### AMD
```sh-session
sudo pacman -S --needed vulkan-radeon lib32-vulkan-radeon lib32-mesa lib32-vulkan-icd-loader vulkan-tools llvm lib32-llvm lib32-llvm-libs llvm-libs
```

Add & install the 2 repo's [mesa-git](https://wiki.archlinux.org/index.php/unofficial_user_repositories#mesa-git) & [llvm-svn](https://wiki.archlinux.org/index.php/unofficial_user_repositories#llvm-svn)

---

## Sound

Source: [here](https://bbs.archlinux.org/viewtopic.php?pid=1054578#p1054578)

May fix games not detecting Sound Cards or not having sound at all.

```sh-session
sudo pacman -S --needed lib32-alsa-plugins lib32-libpulse lib32-openal
```
