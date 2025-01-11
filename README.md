# Hyprland guide! (Arch)
This is a guide specially made for beginners to get through the hyprland setup easily!

# DE Removal

**WARNING: This step is only needed if you want to switch to hyprland entirely**

First press `CTRL + ALT + F5` on your keyboard to get to the tty,whatever DE you have,remove it like this:

`sudo pacman -R [DE]`

**`[DE]` needs to be your desktop enviroments package name,I recommend searching up the package name for your DE**

# Hyprland Installation

1. Get hyprland with this command

   `sudo pacman -S hyprland`

2. Get the terminal (kitty)

   `sudo pacman -S kitty`

3. Get the greeter and activate it

   `sudo pacman -S sddm`

   `sudo systemctl enable sddm`

4. Go to hyprland

   `hyprland`

   If that doesnt work just type `reboot` it should work afterwards
# Configuring Hyprland


you should see a warning at the top with instructions how to get into the terminal.

2. Replace your .config to remove the warning

 `curl https://raw.githubusercontent.com/hyprwm/Hyprland/main/example/hyprland.conf -o ~/.config/hypr/hyprland.conf`

2.5 Change your keyboard layout if it isn't US Qwerty
   
   `sudo nano ~/.config/hypr/hyprland.conf`

   Hold arrow down and stop if you see something like this: 

   #############
   ####INPUT####
   #############

  layout=us


  Change `us` to your layout

  3. Get Waybar

    `sudo pacman -S waybar`

  4. Get Wofi

    `sudo pacman -S wofi

  5. Get a clipboard (enter `CTRL + SHIFT + V` to patse things with it)

    `sudo pacman -S wl-clipboard
  
  6. Enter `WIN + R` on your keyboard and open firefox using wofi
  
  7. Search for dotfiles of waybar that you really like,on the website follow the instructions given (I use the dotfiles of https://github.com/mylinuxforwork/dotfiles)

**Go through the installation and you're done,enjoy!**
