# Retrive Password to Login for bandit12

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been [rotated by 13 positions](https://en.wikipedia.org/wiki/ROT13). <br>

Here, we can use `tr` command in our advantage <br>
we can run `cat data.txt | tr "[A-Za-z]" "[N-ZA-Mn-za-m]"`, and it will return `The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu` in this case which shows the password we need.