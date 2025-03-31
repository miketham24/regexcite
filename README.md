
<!-- README.md is generated from README.Rmd. Please edit that file -->

# regexcite

<!-- badges: start -->

<!-- badges: end -->

The goal of **regexcite** is to make regular expressions in R more
accessible and enjoyable. It provides lightweight helper functions that
wrap around `stringr` to simplify common string operations.

## Installation

You can install the development version of **regexcite** from
[GitHub](https://github.com/jennybc/regexcite) with:

``` r
# install.packages("devtools")
devtools::install_github("jennybc/regexcite")
```

## Example

A common task when working with strings is splitting a single string
into multiple parts. Base R returns a list, but regexcite gives you the
character vector directly.

``` r
library(regexcite)
## basic example code
x <- "alfa,bravo,charlie,delta"
str_split_one(x, pattern = ",")
#> [1] "alfa"    "bravo"   "charlie" "delta"
```

You can also leverage `stringr` features, like controlling the number of
splits or using fixed patterns:

``` r
str_split_one(x, pattern = ",", n = 2)
#> [1] "alfa"                "bravo,charlie,delta"

y <- "192.168.0.1"
str_split_one(y, pattern = stringr::fixed("."))
#> [1] "192" "168" "0"   "1"
```

## Motivation

The `str_split_one()` function simplifies `stringr::str_split()` when
you know you’re working with a single string. It also includes error
handling for longer inputs, making it safer and easier to debug.

## Contributing

Pull requests and suggestions are welcome. For major changes, please
open an issue first to discuss what you’d like to change.

In that case, don’t forget to commit and push the resulting figure
files, so they display on GitHub and CRAN.

## License

MIT © 2025 regexcite authors
