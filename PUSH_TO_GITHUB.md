# Publishing StudentPackage to GitHub

Replace `<username>` with your GitHub username.

## Option A - from R (what the lab record uses)

```r
install.packages(c("usethis", "gitcreds"))
usethis::create_github_token()   # opens browser; create a token and copy it
gitcreds::gitcreds_set()         # paste the token
setwd("path/to/StudentPackage")
usethis::use_git()               # initialise Git + first commit
usethis::use_github()            # creates the repo on GitHub and pushes
```

## Option B - from the terminal

1. Create an empty repo named `StudentPackage` at https://github.com/new
   (no README / .gitignore / licence).
2. Run:

```bash
cd StudentPackage
git init
git add .
git commit -m "Initial commit: StudentPackage"
git branch -M main
git remote add origin https://github.com/<username>/StudentPackage.git
git push -u origin main
```

## Verify - install from GitHub

```r
devtools::install_github("<username>/StudentPackage")
library(StudentPackage)
addNumbers(10, 20)       # [1] 30
subtractNumbers(20, 5)   # [1] 15
multiplyNumbers(4, 6)    # [1] 24
```
