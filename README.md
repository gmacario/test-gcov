# test-gcov
Test gcov coverage analysis tool

### Prerequisites

* [GCC](https://gcc.gnu.org/) - including [gcov](https://gcc.gnu.org/onlinedocs/gcc/Gcov.html)
* [LCOV](https://github.com/linux-test-project/lcov)

### Usage example

```
git clone https://github.com/gmacario/test-gcov
cd test-gcov

# Compile sources (will create `testcov` and `testcov.gcno`)
gcc -o testcov -Wall -fprofile-arcs -ftest-coverage testcov.c

# Reset counters
lcov --directory . --zerocounters

# Run program (will create `testcov.gcda`)
./testcov

# Capture the current coverage to file `testcov.info`
lcov --directory . --capture --output testcov.info

# Generate HTML report `index.html`
genhtml testcov.info

# Now open file index.html from a web browser
```

### License and Copyright

License: See [LICENSE](LICENSE)

Copyright 2017, [Gianpaolo Macario](https://gmacario.github.io/)

<!-- EOF -->
