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

la arquitectura de shiny esta conformada por un sistema de archivos sencillos que permiten estructurar la aplicación sin necesariamente conocer lenguajes como HTML, JavaScript o CSS.

La misma viene dada por 2 archivos, uno que contiene la interfaz del usuario (ui.R) y otra que contiene el servidor lógico (server.R), además, también posee una opción de para desarrollar aplicaciones cortas que se pueden escribir en un solo archivo (app.R).

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



--- type:NormalExercise lang:r xp:100 skills:1 key:205e741e77
## Estructura y Componentes Principales

Vamos a aprender como están estructuradas las aplicaciones en shiny, las mismas no son más que un conjunto de directorios y archivos que contienen un script de R ```app.R``` en el caso de las aplicaciones sencillas. En este caso tanto la interfáz del usuario como el servidor lógico se definen como objetos a través de funciones especificas como ```pageWithSideBar``` , ```fluidPage```, ```fixedPage``` para el ui y para el servidor lógico ```function(input, output)``` del paquete shiny. al final el script debe contener la sentencia ```shinyApp(ui, server)``` que hace que la aplicación levante.

*** =instructions

Primero cargar el paquete "Shiny" a través de la instrucción __library()__.
defina la intefáz de usuario con la función __pageWithSideBar__.
defina el servidor lógico a través de la función __function(input, output)__.
coloque la sentencia para levantar la aplicación.

*** =hint

Cargue el paquete usando library("shiny").
ui <- ...
server <- ...
shinyApp(ui, server)

*** =pre_exercise_code
```{r}
library(shiny)
```

*** =sample_code
```{r}

#Cargue el paquete Shiny



#defina la interfaz de usuario

#ui <-

#defina el servidor lógico

#server <- 

#coloque la sentencia para levantar la aplicación

#

```

*** =solution
```{r}

#Cargue el paquete Shiny

library("shiny")

#defina la interfaz de usuario

#ui <- pageWithSideBar()

#defina el servidor lógico

#server <- function(input, output) {}

#shinyApp(ui, server)

```

*** =sct
```{r}
success_msg("¡Excelente!")
```


--- type:NormalExercise lang:r xp:100 skills:1 key:2b2df8f7aa

## Estructura y Componentes Principales *Interfaz de Usuario*

En la parte de la interfaz de usuario las zonas de la aplicación se determinan a través de 3 funciones: el título se establece  a través de la función ``` headerPanel()```, panel lateral de opciones  con la función```  sidebarPanel() ``` y el panel principal con ```mainPanel()``` todo esto en el caso que se utilice la función ```pageWithSideBar``` para establecer la interfaz de usuario de su aplicación y separando cada función con coma ","  y las funciones para definir las zonas serán escritas como parámetros de la función principal. 

*** =instructions

Colocar "Vision With DataCamp" como título de su aplicación.
establezca la región del panel lateral y del panel principal vacios

*** =hint

usar ``` headerPanel()```, ```  sidebarPanel() ``` y ```mainPanel()``` respectivamente.

*** =pre_exercise_code
```{r}
library("shiny")
```

*** =sample_code
```{r}
# Define la interfaz de usuario con la función mencionada en la descripción del ejecicio

#ui <- 

  # Título de la Aplicación
  #                         ,
  
  # Panel Lateral
  #                         ,
  
  # Panel Principal
  #                         )
```

*** =solution
```{r}
# Define la interfaz de usuario con la función mencionada en la descripción del ejecicio

#ui <- pageWithSidebar(

  # Título de la Aplicación
  # headerPanel("Vision with DataCamp"),
  
  # Panel Lateral
  # sidebarPanel(),
  
  # Panel Principal
  # mainPanel() )
```

*** =sct
```{r}
success_msg("sígue así")
```



--- type:NormalExercise lang:r xp:100 skills:1 key:134f82e24f

## Estructura y Componentes Principales *Interfaz de Usuario* (continuación)

Otra de las opciones para definir la interfaz de usuario es la función ``` fluidPage() ```  y análogamente se utilizan funciones especificas para definir las zonas de la aplicación la unica diferencia es que las fuciones correspondientes a los paneles internos (lateral y principal) van escritos dentro de la función ```sidebarLayout()``` esto más adelante nos permitirá realizar configuraciones adicionales para mostrar varias salidas y ordenarlas en una estructura definida.


*** =instructions

Colocar "Vision With DataCamp fluidPage" como título de su aplicación.
establezca la región del panel lateral y del panel principal vacios


*** =hint

recuerde colocar las funciones de los paneles lateral y principal como parámetros dentro de la función ```sidebarLayout()``` 

*** =pre_exercise_code
```{r}

library("shiny")

```

*** =sample_code
```{r}
# Define la interfaz de usuario con la función mencionada en la descripción del ejecicio

# ui <- 

    # Título de la Aplicación
    #                         ,
  
  #
  
    # Panel Lateral
    #                         ,
  
    # Panel Principal
    #                         )
  
  #)
 

```

*** =solution
```{r}
# Define la interfaz de usuario con la función mencionada en la descripción del ejecicio

# ui <- fluidPage(

    # Título de la Aplicación
    # titlePanel("Vision With DataCamp fluidPage"),
  
  #sidebarLayout(
  
    # Panel Lateral
    # sidebarPanel(),
  
    # Panel Principal
    # mainPanel())
  
  #)
  
```

*** =sct
```{r}
success_msg("muy bien, rumbo a tu primera aplicación con R Shiny")
```
