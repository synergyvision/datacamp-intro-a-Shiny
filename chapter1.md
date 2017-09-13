---
title       : Aplicaciones Web con Shiny
description : Vamos a repasar cómo es una página Web y cómo se construyen con Shiny desde R.
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise lang:r xp:100 skills:1 key:774b72b901
## Conociendo R Shiny

Shiny es framework (marco) para desarrollos web vía R, el mismo consta de un web Socket que permite contruir páginas HTML, y tener un servidor lógico de operaciones todo escrito en lenguaje R, además tiene características integradas con RStudio® la cual son altamente recomendables.

Para utilizar dicho framework debes instalar el paquete "shiny" desde el CRAN

*** =instructions

- Instalar paquete desde la consola.
- Activar Librería

*** =hint

ejecuta las instrucciones desde la consola

*** =pre_exercise_code

```{r}
#pre
```

*** =sample_code
```{r}
# descarga e instala el paquete shiny 
install.packages()
library()

# de esta manera podremos iniciar

```

*** =solution
```{r}
# descarga e instala el paquete shiny 
install.packages("shiny")
library("shiny")

# de esta manera podremos iniciar

```

