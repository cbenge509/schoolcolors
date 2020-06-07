
<!-- README.md is generated from README.Rmd. Please edit that file -->

# schoolcolors <img src="man/figures/logo.png" align="right" width="120" />

<!-- badges: start -->

[![CRAN
status](https://www.r-pkg.org/badges/version/schoolcolors)](https://CRAN.R-project.org/package=schoolcolors)
[![pkgdown build
status](https://github.com/dermcnor/schoolcolors/workflows/pkgdown/badge.svg)](https://github.com/dermcnor/schoolcolors/actions)
<!-- badges: end -->

[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/0)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/0)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/1)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/1)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/2)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/2)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/3)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/3)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/4)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/4)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/5)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/5)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/6)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/6)[![](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/images/7)](https://sourcerer.io/fame/cbenge509/dermcnor/schoolcolors/links/7)

The goal of schoolcolors is to provide palettes for all possible NCAA
schools. It is built very heavily upon the structure laid out in the
[wesanderson](https://github.com/karthik/wesanderson) package.

## WIP

This is still a Work In Progress. You can’t currently install from CRAN,
and the dev version has only a structure. There are many NCAA schools
and we would love any help that you can for populating the colors for
schools.

The method for populating a school is as follows:

1.  Find School Colors:
      - Search for a school name and color palette. This generally leads
        to a brand site or pdf for that school.
      - Only if there is no branding or web usage site, pull colors from
        [TruColor](http://www.trucolor.net/college-colors-nicknames/college-colors-nicknames-full-index/)
          - The current Institutional Colors should be used.
2.  Populate Colors:
      - Find the line with the school\_name and populate the vector with
        the Primary Colors.
      - If there are any additional colors, put them on a new vector in
        the list and order them according to secondary, tertiary,
        accent, supporting, etc.

### Example: College of William and Mary

  - Initial code
    
    ``` r
    college_of_william_and_mary = list(c())
    ```

  - Populated Colors
    
    ``` r
    college_of_william_and_mary = list(c("#115740", "#B9975B"),
                                       c("#F0B323", "#D0D3D4", "#00B388", "#CAB64B", 
                                         "#84344E", "#64CCC9", "#E56A54", "#789D4A", 
                                         "#789F90", "#5B6770", "#183028", "#00313C"))
    ```

## Installation

You can install the development version from
[GitHub](https://github.com/) by doing the following:

``` r
# install.packages("remotes")
remotes::install_github("dermcnor/schoolcolors")
```

You can install the released version of schoolcolors from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("schoolcolors")
```

## Example

This is a basic example which shows you how to use a palette for a
school.

``` r
library(schoolcolors)
## basic example code
my_pal <- school_palette("college_of_william_and_mary")
as.character(my_pal)
#>  [1] "#115740" "#B9975B" "#F0B323" "#D0D3D4" "#00B388" "#CAB64B" "#84344E"
#>  [8] "#64CCC9" "#E56A54" "#789D4A" "#789F90" "#5B6770" "#183028" "#00313C"
my_pal
```

<img src="man/figures/README-example-1.png" width="100%" />
