
<!-- README.md is generated from README.Rmd. Please edit that file -->

# assignmentB2AprilRadford

This repository is for completion of assignment B2 in STAT545 at UBC.
`assignmentB2AprilRadford` counts the missing values (`NA`s) in every
column of a data frame, separately for each level of a grouping column.
It returns one row per group, so you can quickly see where the missing
data is concentrated.

The repository includes the following files and folders:

- README.Rmd
- README.md
- DESCRIPTION
- NAMESPACE
- R/ (the function and its roxygen2 documentation)
- man/ (the generated documentation files)
- tests/ (tests for the function)

## Installation

To install the package, run the following in R:

``` r
library(devtools)
install_github("UBC-STAT545-F2026/assignmentB2AprilRadford", ref = "0.1.0")
```

## Usage

Load the package, then give `count_all_missing_by_group()` your data and
the column to group by:

``` r
library(assignmentB2AprilRadford)

count_all_missing_by_group(airquality, Month)
#> # A tibble: 5 × 6
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0
```

To explore this repository, install the package using the instructions
above, then run `?count_all_missing_by_group` to view the function’s
documentation. Alternatively, you can view the function’s source code in
the `R/` folder.

## AI Disclosure

I used Claude while completing this assignment in the following ways:

- Correctly formatting the `DESCRIPTION` file
- Interpreting `devtools::check()` output and troubleshooting a git
  merge conflict
