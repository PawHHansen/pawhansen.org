---
title: Quick analysis of mtcars
author: Paw Hansen
date: '2022-08-17'
slug: []
categories:
  - R
tags:
  - style
subtitle: 'Here is my subtitle'
excerpt: ''
draft: yes
series: null
layout: single
editor_options: 
  chunk_output_type: console
---


```r
library(tidyverse)
```

```
## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
## ✔ ggplot2 3.3.6     ✔ purrr   0.3.4
## ✔ tibble  3.1.8     ✔ dplyr   1.0.9
## ✔ tidyr   1.2.0     ✔ stringr 1.4.0
## ✔ readr   2.1.2     ✔ forcats 0.5.1
## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
## ✖ dplyr::filter() masks stats::filter()
## ✖ dplyr::lag()    masks stats::lag()
```

```r
theme_set(theme_minimal())
knitr::opts_chunk$set(cache = TRUE, cache.lazy = FALSE, warning = FALSE, 
                      message = FALSE, echo = TRUE, dpi = 180,
                      fig.width = 7, fig.height = 6)

data("mtcars")
```

Here is a quicki test of what a blog post could look like. 


```r
mtcars %>% 
  ggplot(aes(cyl, mpg)) + 
  geom_boxplot(aes(color = as.factor(cyl)), show.legend = F)
```

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" alt="Here is a cool figure from the mtcvars data" width="1260" />
<p class="caption">Figure 1: Here is a cool figure from the mtcvars data</p>
</div>

