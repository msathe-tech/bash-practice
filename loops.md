'C' - style loops
'for' loops over items 'in' lists

```shell script
mkdir loops
cd loops
for (( i=0; i < 20; i++ ))
do 
    echo $i
    echo $i > file${i}.txt
done
```

## for - in
```shell script
for f in $(ls *txt)
do 
    echo "File $f contains: $(cat $f)"
done
```

If there are spaces in file name then watch out.

# While loops
```shell script
n=0 
while [ ! -a newfile ]; do
  ((n++))
  echo "In iteration $n"
  if [[ $(cat file${n}.txt) == "15" ]]
  then 
    touch newfile
  fi    
done
```

```shell script
a=1
case "$a" in
    1) echo 'a is 1'; echo 'ok';;
    2) echo 'a is 2'; echo 'ok';;
    *) echo 'a is unmatched'; echo 'failure';;
esac
```