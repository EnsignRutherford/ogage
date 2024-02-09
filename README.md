# ogage for RGB10/OGA BE (1.1)

Prequisites
===========
- brightnessctl
- rustc
- evdev_rs

Build
=====
```
git clone https://github.com/christianhaitian/ogage.git
cd ogage
cargo build --release
strip target/release/ogage
```
ogage executable will be in the target/release folder.

If you have issues with Cargo, do the following: (Thanks to romadu for the find)
================================================================================
```
apt remove cargo
apt autoremove
apt remove rustc
apt install brightnessctl rustc autotools-dev automake libtool libtool-bin libevdev-dev
```

If compiling in ArkOS the version of rust available through the Ubuntu repo there is old. Do the following:
```
sudo apt remove -y rustc
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh (Do the customize install, choose the default options, but for profile do minimal.)
source "$HOME/.cargo/env"
```
