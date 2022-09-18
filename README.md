# Bash TLE parser
A pipeable TLE parser written in Bash.

This Bash script takes raw two-line element (TLE) set data and turns each record into a comma-separated list of each of the record's fields. The TLE format is used to describe the orbit of a satellite orbiting Earth.

## Usage
The TLE parser can either have raw TLE data input piped into it:

```shell
$ cat "iss.txt" | tle
ISS (ZARYA),25544,U,98,067,A,22,255.73370370,.00008229,00000+0,15112-3,0,999,9,25544,51.6420,262.8647,0002292,226.1291,116.9782,15.50169761,35875,6
$
```

or an input file can be passed as a parameter:

```shell
$ tle "iss.txt"
ISS (ZARYA),25544,U,98,067,A,22,255.73370370,.00008229,00000+0,15112-3,0,999,9,25544,51.6420,262.8647,0002292,226.1291,116.9782,15.50169761,35875,6
$
```

## Tests
Tests are avaialble in the `tests` directory. A `test` Bash script has been written to test the TLE parser against the various input files. Simply run:

```shell
$ test
```

in the `tests` directory to run all the tests and view their results.

## References
- [Sample data from CelesTrak.org](https://celestrak.org/NORAD/elements/)
- [TLE format description from CelesTrak.org](https://celestrak.org/NORAD/documentation/tle-fmt.php)
