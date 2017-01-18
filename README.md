# test-gcov
Test gcov coverage analysis tool

### Prerequisites

* GCC
* LCOV

### Usage example

```
git clone https://github.com/gmacario/test-gcov
cd test-gcov

# Compile sources (will create `testcov` and `testcov.gcno`)
gcc -o testcov -Wall -fprofile-arcs -ftest-coverage testcov.c

# Run program (will create `testcov.gcda`)
./testcov
```

### License and Copyright

License: See [LICENSE](LICENSE)

Copyright 2017, [Gianpaolo Macario](https://gmacario.github.io/)

<!-- EOF -->
