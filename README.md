# StudentPackage

A small demonstration R package built for **R Programming Lab - Experiment 11
(Writing R Packages)**, *Additional Exercise 5: Publish the package through GitHub*.

## Installation

```r
# install.packages("devtools")
devtools::install_github("<your-username>/StudentPackage")
```

## Functions

| Function | Description | Example | Result |
| --- | --- | --- | --- |
| `addNumbers(a, b)` | Adds two numbers | `addNumbers(10, 20)` | `30` |
| `subtractNumbers(a, b)` | Subtracts `b` from `a` | `subtractNumbers(20, 5)` | `15` |
| `multiplyNumbers(a, b)` | Multiplies two numbers | `multiplyNumbers(4, 6)` | `24` |

## Usage

```r
library(StudentPackage)

addNumbers(10, 20)       # 30
subtractNumbers(20, 5)   # 15
multiplyNumbers(4, 6)    # 24
```

## Publishing steps (usethis)

```r
library(usethis)
usethis::use_git()      # initialise a Git repository
usethis::use_github()   # create the GitHub repository and push the code
```

`use_github()` needs a GitHub account and a Personal Access Token.

## License

MIT (c) Student Name
