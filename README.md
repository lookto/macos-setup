# **macOS 12.3 Setup**

A brief documentation on how I set up my macOS install (at work) to satisfy my needs (in terms of design and workflow).

## Table of contents

- [Font](#font)
- [Software](#software)
  - [Display Link Manager](#display-link-manager)
  - [Rectangle](#rectangle)
- [Dock Customization](#dock-customization)

# **Font**

Personaly i prefer using Fira Code or UbunutMono Nerd Font Mono, which can be downloaded [here](https://github.com/tonsky/FiraCode) and [here](https://www.nerdfonts.com/font-downloads).

# **Software**

## **Display Link Manager**

Needed to use Monitors connected to a DisplayLink capable docking station.

Download latest stable version here: [synaptics homepage](https://www.synaptics.com/products/displaylink-graphics/downloads/macos)

Install the driver and manager with the docking station **disconnected!** I had some weird bugs and flickering of the connected monitor otherwise.

## **Rectangle**

Adds window snapping feature to macOS, including keyboard shortcuts. Great for using the mouse less and maximising the productivity.

Can be downloaded [here](https://rectangleapp.com/).

# **Dock Customization**

The standard dock does not realy feel snappy or responsive enough. I set the Dock to auto-hide, but the delay for showing the dock when you move the mouse cursor to the edge of the screen is very slow.

Running the following commands will customize these time intervals of the delay and the hide animation.

```zsh
defaults write com.apple.dock autohide-delay -float 0 &&
defaults write com.apple.dock autohide-time-modifier -float 0.5 &&
killall Dock
```

To reset run following commands.

```zsh
defaults delete com.apple.dock autohide-delay &&
defaults delete com.apple.dock autohide-time-modifier &&
killall Dock
```
