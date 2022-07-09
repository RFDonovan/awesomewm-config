# Exploring Awesome Window Manager

Just for my own satisfaction, I wanted to install `AwesomeWM` to my Pop Os and see.
It's pretty straightforward, we can `Super+S` to get help.
## Installation 
```shell
sudo apt install awesome xterm nitrogen rofi picom dmenu
```
`picom` or `compton` is a program that can enable transparency
`dmenu` to replace the default prompt of Awesome (win+r)

## Configuration 
As I'm still a noob into tiling window manager, I followed the tutorial of a guy on youtube. His name is `MAKC`.
(https://www.youtube.com/watch?v=nC_e8Gw1XlA&list=PLIYVhRocqRoRVCyLOW7xnzaSXXQU_HaOD)

```shell
mkdir ~/.config/awesome
cp -p /etc/xdg/awesome/rc.lua ~/.config/awesome
```
From there we can add few things to the `rc.lua` file to customize awesome

`beautiful.useless_gap = 5`: adding gaps between windows
`nitrogen`: run nitrogen when awesome restart

### Plugin to move floating window

```shell
    mkdir -p ~/.config/awesome
    cd ~/.config/awesome
    git clone https://github.com/Elv13/collision
```
I'm already pleased with what I get here. Few things I need to change are `Dark Theme` and the `wibar`.
###  Alacritty as a Terminal Emulator

`sudo apt install alacritty` or `cargo install alacritty` is fine.

When using cargo, the binary for alacritty is not automatically added into the $PATH. You have to set it manually or create a soft link
`ln -s /path/to/cargo/alacritty /usr/bin/alacritty`

Once installed I took a config file from DT(DistroTube)'s repo and adapted it to my own
* Font as `FiraCode Nerd Font Mono `
* Opacity to 0.80

(see the `alacritty` folder for conf)
Then I changed the default terminal from launcher to `alacritty`
