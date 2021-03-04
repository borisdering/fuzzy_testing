# Fuzz Testing With Clang++

## Compile And Run

```
$ clang++ main.cpp --std=c++14 -g -fsanitize=fuzzer,address
$ ./a.out
```