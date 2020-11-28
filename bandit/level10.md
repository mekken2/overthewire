# Retrive Password to Login for bandit10

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters. <br>
Here, we can use `strings` command to get the human readable strings from `data.txt` file and then grep the lines preceded by `=`
So, we can do `strings data.txt | grep =` which will return
`========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`

And we can clearly see that password is `truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk` in this case.