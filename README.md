# Hyprland guide EndeavourOS (Arch)
This is a guide for beginners to get through the hyprland setup easily! Normal arch may be hard for beginners so thats why im going to write about endeavouros a distro based on arch


**info:were going to use dotfiles of ml4w https://github.com/mylinuxforwork/dotfiles**
# REQUIREMENTS:

**USB-STICK**

**Free diskspace	15 GB**

**Processor	64-bit Dual core Intel/AMD**

**Offline:3 GB RAM**

**Online:4 GB**

# Heads Up!
If you didn't know,in Linux,the Windows Key is called the "Super Key"
# EOS Installation

**SKIP THIS IF YOU ALREADY HAVE THE DISTRO**


First of all go to https://endeavouros.com/ and download the .iso for the country you live in,then you get your usb stick,plug it in your computer and flash the iso with balena etcher,rufus or something you like.

If you flashed the iso you boot into firmware recovery,turn off secure boot to boot into eos.

**Memorize your username and password in the setup because you will be needing that.**

In the setup choose your keyboard layout etc. choose grub in bootloader options and if you get the question "What Desktop Enviroment?" make sure to pick none. Wait for eos to install then reboot at the end.

# Hyprland Installation


Now you should see a terminal in your screen asking for as login,just enter your username and then your password.
1. Get hyprland with this command

   `sudo pacman -S hyprland`

3. Get the greeter and activate it

   `sudo pacman -S sddm`

   `sudo systemctl enable sddm`

5. Go to hyprland

   `hyprland`

   If that doesnt work just type `reboot` it should work afterwards
# Configuring Hyprland


you should see a warning at the top with instructions how to get into the terminal.

**Warning!:If pressing `Super Key + Q` doesn't bring you to the terminal,press `CTRL + ALT + F5`,enter your login data like before and install kitty:**

`sudo pacman -S kitty`

and then type in `hyprland` or `reboot` if that doesn't work.

Now open the terminal with `SUPER KEY + Q` 

1. Replace your .config to remove the warning

 `curl https://githubusercontent.com/hyprwm/Hyprland/main/example/hyprland.conf -o ~/.config/hypr/hyprland.conf`

1.5 Change your keyboard layout if it isn't US Qwerty
   
   `sudo nano ~/.config/hypr/hyprland.conf`

   Click arrow down repeadetly till you see something like: 

   #############
   ####INPUT####
   #############

  layout=us


  change us to your layout

  2. Get Waybar

    `sudo pacman -S waybar`

  3. Get the dotfiles

    bash <(curl -s https://raw.githubusercontent.com/mylinuxforwork/dotfiles/main/setup-arch.sh)

   go through the installation and you're done,enjoy!
