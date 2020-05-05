```shell script
function myfunc {
    echo Hello World
}
myfunc

# Functions can have args
function myfunc {
    echo $1
echo $2 
}
myfunc hello world
myfunc "hello world" "how are you"
```
# Variables
```shell script
MYVAR="Hi from outside the function"
function myfunc() {
    echo $MYVAR
}
myfunc


function myfunc() {
       local MYVAR="Hi from inside myfunc"
   echo $MYVAR
   }
local MYVAR="some variable"
```

## Builtin
```shell script
builtin ls
builtin cd
type cd
type ls
```

What happens if function name clashes with a builtin.

```shell script
function cd() {
  echo "No!"
}
cd /tmp
declare -F # show all declared functions
unset -f cd #to unset function 
```

## Alias
```shell script
alias k=kubectl
unalias k
```
