# There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

We need to use `diff` command to check which line is different. Do `diff passwords.old passwords.new` to get the password <br>
It will return 2 passwords, the later is the one we need as its in `passwords.new` - `kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd`