```shell script
mkdir "subshells" && cd subshells
VAR1='the original variable'
(
echo inside a subshell
echo ${VAR1}
VAR2='second variable'
echo ${VAR2}
)

# try modifying VAR1 inside subshell
(
echo inside a subshell
VAR1='new value'
echo ${VAR1}
VAR2='second variable'
echo ${VAR2}
)
```