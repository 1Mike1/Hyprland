# All the themes i took from prasanthrangan
> **Note**
>
> thanks to prasanthrangan's work and Senshi111, I am using the same script and themes for Ubuntu setup. Added all required libraries for Ubuntu  so that they could work in Ubuntu 23.04.<br>
>[prasanthrangan github page](https://github.com/prasanthrangan/hyprdots) 
>[Senshi111 github page](https://github.com/Senshi111/debian-hyprland-hyprdots)


# --// Hyprdots //--


<!-- <p align="center">
  <img width="250" src="https://github-production-user-asset-6210df.s3.amazonaws.com/40372242/263763138-8254e6be-9537-4388-90f8-c418124c8284.png">
</p> -->
    


<!-- ## My Debian Sid Hyprland Config
https://user-images.githubusercontent.com/106020512/235429801-e8b8dae2-c1ad-4e23-9aa2-b1edb6cabe99.mp4

| <!-- --> | <!-- --> |
| --- | --- |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/showcase_1.png) | ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/showcase_2.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/showcase_3.png) | ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/showcase_4.png) |
 -->

### Installation
```shell
sudo add-apt-repository restricted
sudo add-apt-repository universe
sudo add-apt-repository multiverse
sudo add-apt-repository -y ppa:ubuntu-toolchain-r/test
sudo add-apt-repository ppa:pipewire-debian/pipewire-upstream
sudo apt update

sudo apt install -y gcc-13 g++-13
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-13 20
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-13 20
```
<br>
<br>

```shell
sudo apt install -y libxcb-xfixes0-dev libxcb-shape0-dev libxcb-xinerama0-dev libxcb-randr0-dev libxcb-image0-dev libxcb-util0-dev libxcb-keysyms1-dev libxcb-icccm4-dev libxcb-xkb-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev libxkbcommon-dev libx11-xcb-dev libx11-dev libxext-dev libxi-dev libxrender-dev libxrandr-dev libxinerama-dev libxkbcommon-x11-dev
```
<br><br>

```shell
sudo apt install -y meson wget build-essential ninja-build cmake-extras cmake gettext gettext-base fontconfig libfontconfig-dev libffi-dev libxml2-dev libdrm-dev libxkbcommon-x11-dev libxkbregistry-dev libxkbcommon-dev libpixman-1-dev libudev-dev libseat-dev seatd libxcb-dri3-dev libvulkan-dev libvulkan-volk-dev  vulkan-validationlayers-dev libvkfft-dev libgulkan-dev libegl-dev libgles2 libegl1-mesa-dev glslang-tools libinput-bin libinput-dev libxcb-composite0-dev libavutil-dev libavcodec-dev libavformat-dev libxcb-ewmh2 libxcb-ewmh-dev libxcb-present-dev libxcb-icccm4-dev libxcb-render-util0-dev libxcb-res0-dev libxcb-xinput-dev xdg-desktop-portal-wlr
```
<br>

```shell
sudo apt install libwlroots-dev libwayland-dev libxcb1-dev wayland-protocols libinput-dev libxcb-icccm4-dev libxcb-image0-dev libxkbcommon-dev libxcb-util-dev

<br>

```shell
sudo apt install libxcb-render-util0-dev libxcb-glx0-dev libxcb-glx0-dev libgstreamer1.0-dev libxtst-dev libxcb-util-dev libxcb-util0-dev
sudo apt install build-essential libgtk-3-dev scdoc libpam
sudo apt install doxygen cppcheck patch flex bison check
```

<br>

```shell
sudo apt install libpipewire-0.3-dev libspa-0.2-dev
sudo apt install build-essential libgtk-3-dev scdoc libpam-dev
sudo apt install mesa-vulkan-drivers vulkan-tools
sudo apt install hwdata libliftoff-dev
```
<br>

```shell
# Build latest libinput
git clone https://gitlab.freedesktop.org/libinput/libinput
cd libinput
meson setup --prefix=/usr builddir/
ninja -C builddir/
sudo ninja -C builddir/ install

sudo systemd-hwdb update
meson setup --prefix=/usr -Ddocumentation=false builddir/
```
<br>

```shell
# Build latest libliftoff-v0.4.1
wget https://gitlab.freedesktop.org/emersion/libliftoff/-/archive/v0.4.1/libliftoff-v0.4.1.zip
unzip libliftoff-v0.4.1.zip
cd libliftoff-v0.4.1

meson setup build/
ninja -C build/
cd build
ninja install
cd ../..
```
<br>

```shell
# waybar
wget https://codeload.github.com/Alexays/Waybar/zip/refs/tags/0.9.22
unzip Waybar-0.9.22.zip
cd Waybar-0.9.22
meson setup build/
ninja -C build/
cd build
ninja install

cd ../..
```

```shell
# sudo apt install waybar (if you dint build waybar above use this)
```

> **Warning**
>
> When you installing rustup, select nightly version othervise you wont be able to build pacakge
> Also if you have nvidia gpu, go to Hyprland nvidia page and aplay sugestions For more details, please refer [Hyprland Nvidia](https://wiki.hyprland.org/Nvidia/) 
   

After minimal (or any other) Debian install (with grub), clone and execute -
```shell
sudo apt install git
git clone https://github.com/Senshi111/debian-hyprland-hyprdots.git
cd ~/debian-hyprland-hyprdots/build-hyprland-and-apps
./install-all.sh

cd ~/debian-hyprland-hyprdots/Theme/Scripts
./install.sh

```

> **Note**
>
> You can also create your own list (for ex. `custom_apps.lst`) with all your favorite apps and pass the file as a parameter to install it -
>```shell
>./install.sh custom_apps.lst
>```

Please reboot after the install script completes and takes you to sddm login screen (or black screen) for the first time.   
For more details, please refer [installation.md](https://github.com/prasanthrangan/hyprdots/blob/main/installation.md)


### Theming
To add your own custom theme, please refer [theming.md](https://github.com/prasanthrangan/hyprdots/blob/main/theming.md)
- Available themes
    - [x] Catppuccin-Mocha
    - [x] Catppuccin-Latte
    - [x] Decay-Green
    - [x] Rosé-Pine
    - [x] Tokyo-Night
    - [x] Material-Sakura
    - [x] Graphite-Mono
    - [x] Cyberpunk-Edge
    - [ ] Gruvbox-Retro (maybe later)
    - [ ] Nordic-Blue (maybe later)

- Contributors themes
    - [x] Frosted-Glass by T-Crypt

| Catppuccin-Mocha |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_mocha_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_mocha_2.png) |

| Catppuccin-Latte |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_latte_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_latte_2.png) |

| Decay-Green |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_decay_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_decay_2.png) |

| Rosé-Pine |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_rosine_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_rosine_2.png) |

| Tokyo-Night |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_tokyo_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_tokyo_2.png) |

| Material-Sakura |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_maura_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_maura_2.png) |

| Graphite-Mono |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_graph_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_graph_2.png) |

| Cyberpunk-Edge |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_cedge_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_cedge_2.png) |

| Frosted-Glass |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_frosted_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_frosted_2.png) |


### Styles

| Theme Select |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/theme_select.png) |

| Wallpaper Select |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/walls_select.png) |

| Launcher Style Select |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_sel.png) |

| Launcher Styles |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_2.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_3.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_4.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_5.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_6.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/rofi_style_7.png) |

| Wlogout Menu |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/wlog_style_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/wlog_style_2.png) |

| Game Launchers |
| :-: |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/game_launch_1.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/game_launch_2.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/game_launch_3.png) |
| ![](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/game_launch_4.png) |


<details>
<summary><h4>Packages</h4></summary>

| tools | |
| :-- | --- |
pipewire | audio and video server
pipewire-alsa | for audio
pipewire-audio | for audio
pipewire-jack | for audio
pipewire-pulse | for audio
wireplumber | audio and video server
network-manager | network manager
network-manager-gnome | nm tray
bluez | for bluetooth
blueman | bt tray
brightnessctl | brightness control for laptop

| login | |
| :-- | --- |
sddm-git | display manager for login
qt5-wayland | for QT wayland XDP
qt6-wayland | for QT wayland XDP

| hypr | |
| :-- | --- |
hyprland-git | main window manager 
dunst | graphical notification daemon
rofi-lbonn-wayland | app launcher
waybar | status bar
swww | wallpaper app
swayidle | idle management daemon
wlogout | logout screen
grim | screenshot tool
slurp | selects region for screenshot/screenshare
swappy | screenshot editor
cliphist | clipboard manager

| dependencies | |
| :-- | --- |
polkit-kde-agent | authentication agent
xdg-desktop-portal-hyprland-git | XDG Desktop Portal
xdg-desktop-portal-gtk | XDG Desktop Portal file picker
imagemagick | for kitty/neofetch image processing
qt5-imageformats | for dolphin thumbnails
pavucontrol | audio settings gui
pamixer | for waybar audio

| theming | |
| :-- | --- |
nwg-look | theming GTK apps
kvantum | theming QT apps
qt5ct | theming QT5 apps

| applications | |
| :-- | --- |
firefox | browser
kitty | terminal
neofetch | fetch tool
dolphin | kde file manager
visual-studio-code | gui code editor
vim | text editor
ark | kde file archiver

| shell | |
| :-- | --- |
zsh | main shell
exa | colorful file lister
oh-my-zsh-git | for zsh plugins
pokemon-colorscripts-git | display pokemon sprites

</details>


<details>
<summary><h4>Keybindings</h4></summary>

| Keys | Action |
| :--  | :-- |
| `Super` + `Q`| quit active/focused window
| `Super` + `Del` | quit hyprland session
| `Super` + `W` | toggle window on focus to float
| `Alt` + `Enter` | toggle window on focus to fullscreen
| `Alt` + `J` | toggle layout
| `Super` + `G` | toggle window group
| `Super` + `T` | launch kitty terminal
| `Super` + `E` | launch dolphin file explorer
| `Super` + `V` | launch Vs code
| `Super` + `F` | launch firefox
| `Super` + `A` | launch desktop applications (rofi)
| `Super` + `Tab` | switch open applications (rofi)
| `Super` + `R` | browse system files (rofi)
| `F10` | mute audio output (toggle)
| `F11` | decrease volume (hold)
| `F12` | increase volume (hold)
| `Super` + `L` | lock screen
| `Super` + `Backspace` | logout menu
| `Super` + `P` | screenshot snip
| `Super` + `Alt` + `P` | print current screen
| `Super` + `RightClick` | resize the window 
| `Super` + `LeftClick` | change the window position
| `Super` + `MouseScroll` | cycle through workspaces
| `Super` + `Shift` + `←` `→` `↑` `↓` | resize windows (hold)
| `Super` + `[0-9]` | switch to workspace [0-9]
| `Super` + `Shift` + `[0-9]` | move active window to workspace [0-9]
| `Super` + `Alt` + `S` | move window to special workspace
| `Super` + `S` | toogle to special workspace
| `Super` + `Alt` + `→` | next wallpaper
| `Super` + `Alt` + `←` | previous wallpaper
| `Super` + `Alt` + `↑` | next waybar mode
| `Super` + `Alt` + `↓` | previous waybar mode
| `Super` + `Shift` + `T` | theme select menu
| `Super` + `Shift` + `A` | rofi style select menu
| `Super` + `Alt` + `G` | disable hypr effects for gamemode

</details>


<details>
<summary><h4>Playlist</h4></summary>

| youtube |
| --- |
| [![IMAGE ALT TEXT](https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/yt_playlist.png)](https://www.youtube.com/watch?v=_nyStxAI75s&list=PLt8rU_ebLsc5yEHUVsAQTqokIBMtx3RFY) |

</details>


<details>
<summary><h4>To-Do</h4></summary>

- [x] Wallpaper change script (ver2)
- [x] Theme selector script
- [x] Theme change script (ver2)
- [x] Update rofi configs
- [x] Clipboard manager in waybar
- [x] Add options to install script (ver2)
- [x] Dynamic waybar config generator script
- [x] Media control mpris module for waybar
- [x] Update Volume control script/notification (ver2)
- [x] Rofi config change script + add new configs
- [x] Make wlogout configs dynamic and sync with theme
- [ ] Wallpaper select script with rofi menu
- [ ] Fix rofi configs/scripts for dynamic scaling
- [ ] Sync PC/keyboard hw rgb with current theme (themeswitch.sh + openrgb)
- [ ] Add battery and brightness indicator/notification for laptop users
- [ ] Replace waybar with Eww? (maybe later)

</details>


<details>
<summary><h4>Known Issues</h4></summary>

- [ ] Random lockscreen crash, refer https://github.com/swaywm/sway/issues/7046
- [ ] Waybar launching rofi breaks mouse input (added `sleep 0.1` as workaround), refer https://github.com/Alexays/Waybar/issues/1850
- [ ] Flatpak QT apps does not follow system theme

</details>

