---
title       : Aplicaciones Web con Shiny
description : Vamos a repasar cómo es una página Web y cómo se construyen con Shiny desde R.
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise lang:r xp:100 skills:1 key:2f5735fd66
## <<<Conociendo R Shiny>>>

*** =instructions

Shiny es framework (marco) para desarrollos web vía R, el mismo consta de un web Socket que permite construir páginas HTML, y tener un servidor lógico de operaciones, todo escrito en lenguaje R, además tiene características integradas con RStudio® la cual son altamente recomendables.

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
success_msg("¡Muy Bien!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:4edcf5dc7b
## <<<Sigamos el ejemplo!>>>

la arquitectura de shiny esta conformada por un sistema de archivos sencillos que permiten estructurar la aplicación sin necesariamente conocer en lenguajes como HTML, JavaScript o CSS.

La misma viene dada por 2 archivos, uno que contiene la interfaz del usuario (ui.R) y otra que contiene el servidor lógico (server.R), además, tambien posee una opcion de aplicaciones cortas que se pueden escribir en un solo archivo (app.R).

la manera más simple para introducirnos en las potencialidades de Shiny es a través de los ejemplos. el paquete "Shiny" contiene un conjunto de ejemplos válidos para observar varias aspectos.  


*** =instructions

Vamos a observar los ejemplos que trae el paquete "Shiny" por defecto a través del comando runExample.  

*** =hint

tipee runExample() en la consola para ver los ejemplos válidos.

*** =pre_exercise_code
```{r}
library("shiny")
```

*** =sample_code
```{r}
#introduzca el comando para ver los ejemplos por defecto


```

*** =solution
```{r}
runExample()
```

*** =sct
```{r}
#no sct
success_msg("¡Excelente!")
```


