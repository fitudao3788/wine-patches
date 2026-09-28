# wine-patches
Some useful patches for Wine

## Usage
### Debian / Ubuntu (amd64)
```bash
# install dependency
sudo apt update
sudo apt install -y build-essential bison flex \
     gcc-multilib gcc-mingw-w64 libasound2-dev bluez \
     libpulse-dev libdbus-1-dev libfontconfig-dev libfreetype-dev \
     libgnutls28-dev libgl-dev libunwind-dev libx11-dev \
     libxcomposite-dev libxcursor-dev libxfixes-dev libxi-dev \
     libxrandr-dev libxrender-dev libxext-dev libwayland-bin \
     libwayland-dev libegl-dev libxkbcommon-dev libxkbregistry-dev \
     libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev \
     libsdl2-dev libudev-dev libvulkan-dev libcapi20-dev \
     libcups2-dev libgphoto2-dev libsane-dev libkrb5-dev \
     samba-dev ocl-icd-opencl-dev libpcap-dev libusb-1.0-0-dev \
     libv4l-dev

# clone Wine
git clone -b wine-11.0 https://gitlab.winehq.org/wine/wine.git wine-11.0

# download patches
curl -O https://raw.githubusercontent.com/fitudao3788/wine-patches/refs/heads/wine-11.0/patch/softdenchi-fixes.patch
# or
wget https://raw.githubusercontent.com/fitudao3788/wine-patches/refs/heads/wine-11.0/patch/softdenchi-fixes.patch

# patch Wine
cd wine-11.0
git apply ../softdenchi-fixes.patch

# build Wine
make -j$(nproc)

# install Wine
sudo make install
```

## License
This patch modifies files that are part of [Wine](https://www.winehq.org/),
which is licensed under the GNU Lesser General Public License version 2.1
(or, at your option, any later version).

Copyright (C) 2026 fitudao3788

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public License
as published by the Free Software Foundation; either version 2.1 of
the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public
License along with this project; if not, see the [`LICENSE`](LICENSE)
file, or <https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html>.
