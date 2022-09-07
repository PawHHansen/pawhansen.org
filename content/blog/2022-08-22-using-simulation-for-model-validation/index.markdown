---
title: "Using simulation for model validation"
author: Paw Hansen
date: "2022-08-22"
slug: []
categories:
  - statistical analysis
tags:
  - simulation
subtitle: ''
excerpt: "You've built a model but does it fit the data?"
draft: yes
series: ~
layout: single
---




```r
data(gapminder, package = "gapminder")
gapminder %>% 
  head()
```

```
## # A tibble: 6 × 6
##   country     continent  year lifeExp      pop gdpPercap
##   <fct>       <fct>     <int>   <dbl>    <int>     <dbl>
## 1 Afghanistan Asia       1952    28.8  8425333      779.
## 2 Afghanistan Asia       1957    30.3  9240934      821.
## 3 Afghanistan Asia       1962    32.0 10267083      853.
## 4 Afghanistan Asia       1967    34.0 11537966      836.
## 5 Afghanistan Asia       1972    36.1 13079460      740.
## 6 Afghanistan Asia       1977    38.4 14880372      786.
```

### Create a model

```r
fit <- lm(lifeExp ~ gdpPercap, data = gapminder)
tidy(fit) %>% 
  mutate_if(is.numeric, round, 3) 
```

```
## # A tibble: 2 × 5
##   term        estimate std.error statistic p.value
##   <chr>          <dbl>     <dbl>     <dbl>   <dbl>
## 1 (Intercept)   54.0       0.315     171.        0
## 2 gdpPercap      0.001     0          29.7       0
```


### Simulate replicated data from the model

### Compare replications to the original data
