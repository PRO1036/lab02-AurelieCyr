Lab 02 - Plastic waste
================
Aurélie Cyr
15/09/25

## Chargement des packages et des données

``` r
library(tidyverse) 
library(ggplot2)
```

``` r
plastic_waste <- read_csv("data/plastic-waste.csv")
```

Commençons par filtrer les données pour retirer le point représenté par
Trinité et Tobago (TTO) qui est un outlier.

``` r
plastic_waste <- plastic_waste %>%
  filter(plastic_waste_per_cap < 3.5)
```

``` r
glimpse(plastic_waste)
```

    ## Rows: 188
    ## Columns: 10
    ## $ code                             <chr> "ALB", "DZA", "AGO", "AIA", "ATG", "A…
    ## $ entity                           <chr> "Albania", "Algeria", "Angola", "Angu…
    ## $ continent                        <chr> "Europe", "Africa", "Africa", "North …
    ## $ year                             <dbl> 2010, 2010, 2010, 2010, 2010, 2010, 2…
    ## $ gdp_per_cap                      <dbl> 9927.182, 12870.603, 5897.683, NA, 19…
    ## $ plastic_waste_per_cap            <dbl> 0.069, 0.144, 0.062, 0.252, 0.660, 0.…
    ## $ mismanaged_plastic_waste_per_cap <dbl> 0.032, 0.086, 0.045, 0.010, 0.051, 0.…
    ## $ mismanaged_plastic_waste         <dbl> 29705, 520555, 62528, 52, 1253, 15777…
    ## $ coastal_pop                      <dbl> 2530533, 16556580, 3790041, 14561, 66…
    ## $ total_pop                        <dbl> 3204284, 35468208, 19081912, 15358, 8…

## Exercices

### Exercise 1

``` r
ggplot(plastic_waste, aes(x = plastic_waste_per_cap)) +
  geom_histogram(binwidth = 0.2) +
  facet_wrap(~continent)
```

![](lab-02_files/figure-gfm/plastic-waste-continent-1.png)<!-- -->

### Exercise 2

``` r
ggplot(plastic_waste, aes(x = plastic_waste_per_cap, fill = continent, color = continent)) +
  geom_density(alpha = 0.5)
```

![](lab-02_files/figure-gfm/plastic-waste-density-1.png)<!-- -->

Réponse à la question…

### Exercise 3

Boxplot:

``` r
# insert code here
```

Violin plot:

``` r
# insert code here
```

Réponse à la question…

### Exercise 4

``` r
# insert code here
```

Réponse à la question…

### Exercise 5

``` r
# insert code here
```

``` r
# insert code here
```

Réponse à la question…

## Conclusion

Recréez la visualisation:

``` r
# insert code here
```
