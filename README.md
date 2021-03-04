# Fuzz Testing With Clang++

## General 
LibFuzzer is in-process, coverage-guided, evolutionary fuzzing engine.

LibFuzzer is linked with the library under test, and feeds fuzzed inputs to the library via a specific fuzzing entrypoint (aka “target function”); the fuzzer then tracks which areas of the code are reached, and generates mutations on the corpus of input data in order to maximize the code coverage. The code coverage information for libFuzzer is provided by LLVM’s SanitizerCoverage instrumentation. - https://llvm.org/docs/LibFuzzer.html 2020

## Compile And Run

```
$ clang++ main.cpp --std=c++14 -g -fsanitize=fuzzer,address
$ ./a.out
```