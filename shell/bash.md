## Tests

In Unix, by convention 0=success, !=0 failure
[ - is a synonym for ‘test’

[[ - is a keyword, more versatile than [, adopted from ksh88

[ ] : portable way
[[ ]] : allows ||, && non-portable 

```bash
if [ $int1 -eq 1 ] && [ $int2 -eq 2 ] 
if [ $int1 -eq 1   -a     $int2 -eq 2 ]

if [ $int1 -eq 1 ] ||    [ $int2 -eq 2 ] 
if [ $int1 -eq 1   -o     $int2 -eq 2 ]

if [[ $int1 -eq 1  &&   $int2 -eq 2 ]]
if [[ $int1 -eq 1   ||     $int2 -eq 2 ]]
```

| Integers| String| File|
|--|--|--|
| -eq, -ne, ge, le, gt, lt | =, !=, \<, \>  (if using [[ you can use <,><br/>-z is null    -n is not null|-e : file exists <br/> -f regular file <br/> -d directory <br/> -b is a block device <br/> -L symlink <br/> -r -w -e : read, write, execute|

### Regex

`[[ $date =~ ^regex$ ]] && echo "matched" || echo "did not match"`

EXPR1 -a EXPR2 True if both expr1 AND expr2 are true.

## Arrays
### Indexed arrays (normal arrays)
```bash
declare -a my_array
```

### Associative Arrays (aka haspMaps/dictionaries)
```bash
declare -A my_array
declare -A MYMAP=( [foo]=bar [baz]=quux [corge]=grault )
```

