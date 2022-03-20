# Week1_R_markdown_ritesh
---
title: "Diamond sizes"
author: "Ritesh Tikhade"
date: '2021'
output: word_document
 
---

``` {r, echo = FALSE}
 
```

```{r setup, include = FALSE}
library(ggplot2)
library(dplyr)
```

```{r, include = FALSE}
smaller <- diamonds %>% 
  filter(carat <= 2.5)
```

```{r, echo = FALSE}
```

We have data about `r nrow(diamonds)` diamonds. Only 
`r nrow(diamonds) - nrow(smaller)` are larger than
2.5 carats. The distribution of the remainder is shown
below:

``` {r, echo = FALSE}
```

```{r, echo = FALSE}
smaller %>% 
  ggplot(aes(carat)) + 
  geom_freqpoly(binwidth = 0.01)
```

```{r, echo = FALSE}
```
