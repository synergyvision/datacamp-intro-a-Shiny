---
title       : Aplicaciones Web con Shiny
description : Vamos a repasar cómo es una página Web y cómo se construyen con Shiny desde R.
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise lang:r xp:100 skills:1 key:2f5735fd66
## <<<Conociendo R Shiny>>>

*** =instructions

Shiny es framework (marco) para desarrollos web vía R, el mismo consta de un web Socket que permite contruir páginas HTML, y tener un servidor lógico de operaciones todo escrito en lenguaje R, además tiene características integradas con RStudio® la cual son altamente recomendables.

Para utilizar dicho framework debes instalar el paquete "shiny" desde el CRAN

*** =hint

ejecuta las instrucciones desde la consola

*** =pre_exercise_code
```{r}
library("shiny")
```

*** =sample_code
```{r}
# descarga e instala el paquete shiny 
library()
```

*** =solution
```{r}
library("shiny")
```

*** =sct
```{r}
#no sct
```
