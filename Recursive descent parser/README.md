### Description

[Prolog](http://teyjus.cs.umn.edu/) parser using [recursive descent method](https://en.wikipedia.org/wiki/Recursive_descent_parser) with custom lexer

### Build & run

* Main program
```
cmake .
make
./parser <filename>
```

* Tests
```
cd test/
cmake .
make
./parserTest
```

* Benchmarks
```
cd benchmark/
./benchmark_install.sh
cmake .
make
./parserBenchmark

