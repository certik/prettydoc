# Introduction #

All capabilities are (or should be) tested, so just look at tests to get an idea and examples how to work with prettydoc and then look into `tests/out/*.pdf` for the corresponding output (after running tests, see below).

# Tests #

```
$ nosetests
[...]
----------------------------------------------------------------------
Ran 3 tests in 1.897s

OK
```

The tests pass if all pdf files are generated (i.e. all conversions went through).
It doesn't test for the correctness of the resulting files though.
The resulting pdf files are in `tests/out/*.pdf`, so you can check that they are
ok by hand.