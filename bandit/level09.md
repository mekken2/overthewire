# Retrive Password to Login for bandit9

The password for the next level is stored in the file `data.txt` in home directory and is the only line of text that occurs only once.
So, we can just do `sort data.txt | uniq -u` to retrieve the password, it was `UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR` for me.