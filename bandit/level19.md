# The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH
Here we can't just directly read the `readme`, so we need to `ssh` the host and port from `bandit17` for `bandit18` to get the password for `bandit19` <br>
we can do this by `ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat ~/readme"` and Entering the password for `bandit18` -- `kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd` when prompted. <br>
we will get the pass for `bandit19` now -- `IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x`