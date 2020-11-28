# Retrive Password to Login for bandit13

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. <br>

1. Create a directory `mkdir /tmp/myname123`
2. Copy the `data.txt` to the newly created directory, `cp data.txt /tmp/myname123`
3. Navigate to the directory `cd /tmp/myname123`
4. Do a reverse hex dump and store the file with its original name `data` using the command `cat data.txt | xxd -r > data`
5. Check the file type using `file data`, it returned `data: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix` in my case which clearly shows its a gzip compressed data
6. Rename the file to add `.gz` extension, do `mv data data2.gz`
7. Now decompress the gzip data by `gzip -d data2.gz`
8. Check the file type again by `file data2`, it returned `data2: bzip2 compressed data, block size = 900k` for my case
9. Now we will again add extension `.bz` by `mv data2 data2.bz`
10. Decompress the bzip file now `bzip2 -d data2.bz`
11. check the file type `file data2`, it returned `data2: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix` for my case.
12. Add `.gz` extension by `mv data2 data4.gz`
13. Decompress the gzip file by `gzip -d data4.gz`
14. Check the file type again `file data4`, it returned `data4: POSIX tar archive (GNU)` for my case.
15. Add `.tar` extension by `mv data4 data5.tar`
16. Decompress the tar file now `tar -xf data5.tar`
17. Check the  file type `file data5.bin`,it returned `data5.bin: POSIX tar archive (GNU)` for my case.
18. Add extension `.tar` by `mv data5.bin data6.tar`
19. Decompress `.tar` by `tar -xf data6.tar`
20. Check the file type by `file data6.bin`, it returned `data6.bin: bzip2 compressed data, block size = 900k` for my case.
21. Add extension `.bz` by `mv data6.bin data7.bz`
22. Decompress the file by `bzip2 -d data7.bz`
23. Check the file type by `file data7`, it returned `data7: POSIX tar archive (GNU)` for my case.
24. Add extension `.tar` by `mv data7 data8.bz`
25. Decompress `data8.bz` by `bzip2 -d data8.bz`
26. Check file type by `file data8.bin`, it returned `data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix` for my case.
27. Add extension `.gz` by `mv data8.bin data9.gz`
28. Decompress `data9.gz` by `gzip -d data9.gzip`
29. check file type `file data9`. it returned `data9: ASCII text` for my case.
30. Now just do `cat data9` to get the password --  `The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL`