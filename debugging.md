debugging.R
================
lalexander
2020-01-27

``` r
# Given this function, use `trace()` to add a `browser()` statement before the
# stop
# Hint: Use as.list(body(fun)) and [[c(1, 2, 3)]] to descend into the expression
# tree.
# fun <- function() {
#   for (i in 1:10000) {
#     if (i == 9876)
#       stop("Ohno!")
#   }
# }

fun <- function(x = 3) {
  x + 1
}

x <- as.list(body(fun))
x
```

    ## [[1]]
    ## `{`
    ## 
    ## [[2]]
    ## x + 1

``` r
# as.list(x[[2]])
# 
# as.list(x[[c(2, 4)]])
# 
# as.list(x[[c(2, 4, 2)]])
# 
# as.list(x[[c(2, 4, 2, 3)]])

# trace(fun, browser, at = list(c(2, 4, 2, 3)))
fun()
```

    ## [1] 4

``` r
# added comment
```
