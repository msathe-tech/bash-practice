#Basics 
`export` a variable to export a local variable to a new shell.

`unset` a variable 

Use `"` for a value to reference another variable. 
`ASENTENCE="this is a sence with $ASTRING"`

`readonly R_VAR="a readonly variable"` 

`env;
declare; 
declare -f `
 `compgen -v`


# Arrays
```declare -a
echo $BASH_VERSION
echo $BASH_VERSINFO
echo ${BASH_VERSINFO[0]}
echo ${BASH_VERSINFO[1]}
```

# Globbing
`touch file1 file2 file3`
`ls *`
`echo ls *`
`echo ls '*'`
`ls file[12]`
```ls file[a-z]
ls file[a-z][0-9]
ls file[0-9]
ls file?
```
dot files are hidden by default. 
 `echo .*` to list all dot files. 
 
## Grep
```shell script
 echo text > afile
grep text afile
grep '*' afile
grep '.*' afile
```




