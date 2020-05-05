```shell script
hostname
echo "My hostname is: hostname"
echo "My hostname is: $(hostname)"
# notice difference between " and '
echo 'My hostname is: $(hostname)'
# Symbol `command` has same effect as $(command)
echo "My hostname is: `hostname`"
# So what is diff between `` and $()
mkdir "itb_cmdsub"
cd itb_cmdsub
touch a b
ls a b
ls $(echo a $(echo b))
# diff is ability to nest, $() is useful for nesting, `` is not
ls `echo a `echo b``
```