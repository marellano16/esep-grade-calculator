# ESEP Grade Calculator

A small, simple Go library that calculates a final grade from assignments, exams, and essays and coverts it to a letter grade.

## How grades are calculated

The library averages each type of grade, then adds up the averages using these weights:

| Type | Weight |
| --- | --- |
| Assignments | 50% |
| Exams | 35% |
| Essays | 15% |

The weighted result is truncated to a whole number and converted to a letter:

| Score | Letter |
| --- | --- |
| 90 and up | A |
| 80 to 89 | B |
| 70 to 79 | C |
| 60 to 69 | D |
| below 60 | F |

Passing requires a C or better.

## Requirements

- Go (Golang) 1.24 or newer (https://go.dev/dl)
- Git (https://git-scm.com)

## Run the tests

Run unit tests:
```
cd grade_calculator/
go test ./...
```

Add `-v` to see each test by name:

```
go test -v ./...
```

Run unit tests with code coverage:
```
cd grade_calculator/
go test -coverprofile=coverage.txt ./...
```