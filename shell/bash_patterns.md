## Write big template string and pipe to a command
```bash
cat<<EOF | kubectl apply -f -
test me
$VAR
EOF
```
