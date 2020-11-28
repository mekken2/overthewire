# The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

1. we need to use openssl to handle ssl encryption `echo "BfMYroe26WYalil77FoDi9qh59eK5xNr" | openssl s_client -connect localhost:30001 -ign_eof`
2. it will show us password at the end - `cluFn7wTiGryunymYOu4RcffSxQluehd`