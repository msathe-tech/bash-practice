Tests return true (0) or false (1).
Non-zero exit code means not-true. 

```shell script
[ 1 = 0 ]
echo $?
[ 1 = 1 ]
echo $?
[ 1 == 1 ]
echo $?
```

## Compare variables
```shell script
A=1
[ $A = 1 ]
echo $?
[ $A = 0 ]
echo $?
[ $(hostname) = "Madhavs-MacBook-Pro.local" ]
echo $?
```

## && 
```shell script
doesnotexist && echo here
doesnotexist || echo here
echo $?
mkdir tmp && cd tmp^c
[ ! 1 = 1 ]
echo $?

([ 1 = 1 ] || [ 1 != 1 ] ) && [ 2 = 2 ]
echo $?
```

## [[]]
```shell script
[[ 1 = 1 ]]
echo $?
unset DOESNOTEXIST
[ $DOESNOTEXIST = `` ]
[[ $DOESNOTEXIST = '' ]]
echo $?

[ x = 'x' ]
echo $?
[[ x$DOESNOTEXIST = 'x' ]]
echo $?
```

## unary operators

```shell script
echo $PWD
[ -z "$PWD" ]
echo $?
[ -a /path/to/file ]
[ -d /path/to/ ]
```

## Comparison
```shell script
# here bash treats them as strings 
[[ 10 < 2 ]]
echo $?

[[ '10' < '2' ]]
echo $?

[[ 10 -ls 2 ]]
echo $?
```

## if 
```shell script
if [[ 10 -lt 2 ]]
then
  echo 'wrong'
elif [[ 10 -gt 2 ]]
then 
    echo 'right'
else 
    echo 'impossible'
fi
```