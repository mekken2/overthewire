# Retrive Password to Login for bandit7
The password for the next level is stored somewhere on the server so first we need to come at the root by doing `cd /`
and it is saved in `./var/lib/dpkg/info/bandit7.password`. <br>

Enter `cat ./var/lib/dpkg/info/bandit7.password` to retrieve the password, it was `HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs` for me. <br>

This challenge will seem very hard if you go by searching every file manually, this is where we can use `find` command as our advantage. <br>
The challenge has specified three criterias 
1. owned by user bandit7
2. owned by group bandit6
3. 33 bytes in size <br>

But, we can just run `find -size 33c` command at the root of server to find a list of the files and then just reading the names. <br>
we can even use `-user {username}` and `-group {group name}` in find to get specific result