My algorithm cheatsheet.

## Prototypes

### Round Robin Scheduling

ref: [Round-Robin轮询调度法及其实现原理 - konglingbin - 博客园](https://www.cnblogs.com/klb561/p/15048252.html)



```pseudo
j = i;
do {
    j = (j + 1) mod n;
    i = j;
    return Si;
} while (j != i);
return NULL;
```



### Weighted Round-Robin Scheduling

```pseudo
while (true) {
  i = (i + 1) mod n;
  if (i == 0) {
     cw = cw - gcd(S);
     if (cw <= 0) {
       cw = max(S);
       if (cw == 0)
         return NULL;
     }
  }
  if (W(Si) >= cw)
    return Si;
}
```


