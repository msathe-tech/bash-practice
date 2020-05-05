Set following at the beginning of a script. 
* set -o errexit
* set -o xtrace
* set -o nounset
* or set -eux as a shorter version 

```shell script
mkdir imiell
cd imiell
ls 
echo $?
doesnotexist
echo $?

#new bash shell
bash 
function trycmd {
  $1
  if [[ $? -eq 127 ]]
  then 
    echo "what are you doing?"
  fi
}
```

* 0 - ok
* 1 - general error
 2 - misuse of shell builtin
 126 - cant execute
 127 - not file match found
 128 - invalid exit value
 (128 + n) - process killed with signal 'n'
 
```shell script
bash
function trycmd() {
  $1 
  if [[ $? -eq 127 ]]
  then 
    echo "what are you doing?"
  fi
}
```

```shell script
if grep not_there /dev/null
then 
    echo there
else
    echo not there
fi
```

## Special variable
PS4 is a special variable 
`PS4=$(date "+%s%N ==> ")`

## Detecting syntx error 
```shell script
bash -n your-script.sh
```