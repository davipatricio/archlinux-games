# archlinux-wine


Useful packages to run Windows games & apps flawlessly on Arch-based distros (Endeavour, Manjaro, Artix etc).

If you cannot open Steam Games with Proton, you must install/update your gpu graphics driver.

---

## Graphics

Source: [here](https://github.com/NoXPhasma/protondb_faq/wiki/Graphics-driver-installation)

Please check [here](https://en.wikipedia.org/wiki/Vulkan_(API)#Compatibility) if your GPU support Vulkan in general! if not then your game will not work with DXVK or vkd3d.

### Intel
```sh-session
sudo pacman -S lib32-vulkan-intel vulkan-intel lib32-mesa lib32-vulkan-icd-loader vulkan-tools llvm lib32-llvm lib32-llvm-libs llvm-libs
```

### NVIDIA
```sh-session
sudo pacman -S lib32-nvidia-utils lib32-opencl-nvidia opencl-nvidia nvidia nvidia-utils
```

### AMD
```sh-session
sudo pacman -S vulkan-radeon lib32-vulkan-radeon lib32-mesa lib32-vulkan-icd-loader vulkan-tools llvm lib32-llvm lib32-llvm-libs llvm-libs
```

Add & install the 2 repo's [mesa-git](https://wiki.archlinux.org/index.php/unofficial_user_repositories#mesa-git) & [llvm-svn](https://wiki.archlinux.org/index.php/unofficial_user_repositories#llvm-svn)

---

## Sound

Source: [here](https://bbs.archlinux.org/viewtopic.php?pid=1054578#p1054578)

May fix games not detecting Sound Cards or not having sound at all.

```sh-session
sudo pacman -S lib32-alsa-plugins lib32-libpulse lib32-openal
```
