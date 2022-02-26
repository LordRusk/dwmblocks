# NOTICE
This program is poorly written, there is many errors that you will find that simply cannot be solved without extensive knowledge of C that nobody else is experiencing. This desperately needs a rewrite. PLEASE REWRITE THIS IN C OR GO I'M BEGGING YOU!!

edit: It's been a while since I wrote this comment. Though the project has grown immensly and probably doesn't have the errors and problems it did 2 years ago, the project is still massive for a statusbar. If you want what you were originally looking for with dwmblocks, what I was looking for 2 years ago, I made it. [Gocaudices](https://github.com/lordrusk/gocaudices): A fast dwmblocks alternative written in go in less than 100 SLOC, currently at 85 SLOC.

# dwmblocks
Modular status bar for dwm written in c.
# modifying blocks
The statusbar is made from text output from commandline programs.
Blocks are added and removed by editing the blocks.h header file.
# Rusk's bulid
I have dwmblocks read my preexisting scripts [here in my dotfiles repo](https://github.com/LordRusk/artixdwm/tree/master/.local/bin/statusbar).
So if you want my build out of the box, download those and put them in your `$PATH`.
# signalling changes
For example, the audio module has the update signal 10 by default.
Thus, running `kill -$((34+10)) $(pidof dwmblocks)` will update it.

# clickable modules
Like i3blocks, this build allows you to build in additional actions into your scripts in response to click events.
See the above linked scripts for examples of this using the `$BLOCK_BUTTON` variable.

For this feature to work, you need the appropriate patch in dwm as well. See [here](https://gist.github.com/danbyl/54f7c1d57fc6507242a95b71c3d8fdea).
Credit for those patches goes to Daniel Bylinka (daniel.bylinka@gmail.com).
