# The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

1. `cd /etc/bandit_pass`
2. `cat bandit14` to view the password - `4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`
3. `echo "4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e" | nc localhost 30000` to get the password for next level -- `BfMYroe26WYalil77FoDi9qh59eK5xNr`