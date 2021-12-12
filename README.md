# grpc-go-3

We modified gRPC-go-9280052d36656451dd7568a18a836c2a74edaf6c by doing the two changes:

1. We replace all 'func (s) Test' with 'func Test' by executing the following command. 

```
$ grep -rl 'func (s) Test' ./ | xargs sed -i 's/func (s)/func/g'
```

2. We comment out the body of ```func check(efer Errorfer, timeout time.Duration)``` in file internal/leakcheck/leakcheck.go.



