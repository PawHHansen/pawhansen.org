---
title: Quick analysis of mtcars
author: Paw Hansen
date: '2022-08-17'
slug: []
categories: ["Data science"] 
tags: []
subtitle: 'Here is my subtitle'
excerpt: ''
draft: yes
series: null
layout: single
editor_options: 
  chunk_output_type: console
---



Here is a quick test of what a blog post could look like. 


```r
mtcars %>% 
  ggplot(aes(cyl, mpg)) + 
  geom_boxplot(aes(color = as.factor(cyl)), show.legend = F)
```

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" alt="Here is a cool figure from the mtcvars data" width="1260" />
<p class="caption">Figure 1: Here is a cool figure from the mtcvars data</p>
</div>

