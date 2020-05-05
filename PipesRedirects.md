```shell script
cd itb_pipes_redirects/
 echo "contents of file" > sometext
cat sometext | grep -c filev
cat doesnotexist | grep -c file
```

## standard output vs standard error
cat sometext results in output to stdout.
cat doesnotexist results in error so to stderr.
| only sends stdout, not stderrs.

By defaul every process gets 3 FDs.
0 - stdin
1 - stdout
2 - stderr

```shell script
 echo sometext 1> afile
cat afile
commanddoesnotexist > afile
cat afile
commanddoesnotexist 2> afile
cat afile
```

```shell script
grep -c file < sometext
 echo sometext >> afile 
 echo sometext >> afile 
cat afile
```

* \> sends stdout to a file
* 1> is same as >
* 2> sends stderr to a file

Advanced but often seen
* 2>&1  sends standard error to whatever standard output is pointed at.
       A way of sending ‘all’ output to a file.
       

