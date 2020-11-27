# Retrive Password to Login for bandit6
The password is saved in `./maybehere07/.file2` file in `inhere` folder. <br>
1. Do `cd inhere` to get inside the folder
2. Enter `cat ./maybehere07/.file2` to retrieve the password, it was `DXjZPULLxYr17uwoI01bNLQbtFemEgo7` for me. <br>

This challenge will seem very hard if you go by searching every file manually, this is where we can use `find` command as our advantage. <br>
The challenge has specified three criterias 
1. human-readable
2. 1033 bytes in size
3. not executable <br>

So, we can just run `find -readable -size 1033c` command inside `inhere` folder to find the specific file.