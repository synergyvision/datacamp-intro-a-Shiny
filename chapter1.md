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
msg = "¡Buen Inicio!"
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
msg = "Aprendiendo con la acción"
success_msg("¡Excelente!")
```



--- type:NormalExercise lang:r xp:100 skills:1 key:205e741e77
## Estructura y Componentes Principales

Vamos a aprender como están estructuradas las aplicaciones en shiny, las mismas no son más que un conjunto de directorios y archivos que contienen un script de R ```app.R``` en el caso de las aplicaciones sencillas. En este caso tanto la interfaz del usuario como el servidor lógico se definen como objetos a través de funciones especificas como ```pageWithSideBar``` , ```fluidPage```, ```fixedPage``` para el ui y para el servidor lógico ```function(input, output)``` del paquete shiny. al final el script debe contener la sentencia ```shinyApp(ui, server)``` que hace que la aplicación levante.

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
msg = "¡Ánimo!"
success_msg("¡Excelente!")
```


--- type:NormalExercise lang:r xp:100 skills:1 key:2b2df8f7aa

## Estructura y Componentes Principales UI

En la parte de la interfaz de usuario las zonas de la aplicación se determinan a través de 3 funciones: el título se establece  a través de la función ``` headerPanel()```, panel lateral de opciones  con la función```  sidebarPanel() ``` y el panel principal con ```mainPanel()``` todo esto en el caso que se utilice la función ```pageWithSideBar``` para establecer la interfaz de usuario de su aplicación y separando cada función con coma ","  y las funciones para definir las zonas serán escritas como parámetros de la función principal. 

*** =instructions

Colocar "Vision With DataCamp" como título de su aplicación.
establezca la región del panel lateral y del panel principal vacíos

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
msg = "¡Ya conoces los elementos fundamentales!"
success_msg("sígue así")
```



--- type:NormalExercise lang:r xp:100 skills:1 key:134f82e24f

## Estructura y Componentes Principales UI (continuación)

Otra de las opciones para definir la interfaz de usuario es la función ``` fluidPage() ```  y análogamente se utilizan funciones especificas para definir las zonas de la aplicación la única diferencia es que las funciones correspondientes a los paneles internos (lateral y principal) van escritos dentro de la función ```sidebarLayout()``` esto más adelante nos permitirá realizar configuraciones adicionales para mostrar varias salidas y ordenarlas en una estructura definida.


*** =instructions

Colocar "Vision With DataCamp fluidPage" como título de su aplicación.
establezca la región del panel lateral y del panel principal vacíos


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
msg = "Conociendo otras opciones"
success_msg("muy bien, rumbo a tu primera aplicación con R Shiny")
```



--- type:NormalExercise lang:r xp:100 skills:1 key:aceaef451b
## Componentes de Entradas y Salidas.  

la interfaz de usuario de las aplicaciones en R Shiny contiene elementos para ingresar datos y otros elemento donde se muestran las salidas luego de ser procesadas por las funciones  escritas en R a través del servidor lógico.

corriendo el primer ejemplo por defecto que trae el paquete shiny con la siguiente instrucción:

```
library("shiny")  
runExample("01_hello")

```
obtenemos


![](http://s3.amazonaws.com/assets.datacamp.com/production/course_5138/datasets/shinyExample1.png)  

Como se aprecia en la gráfica la interfaz de ejemplo consta de 3 elementos bien diferenciados que son el título, el panel lateral y el panel principal. En general el título sirve para identificar la aplicación, el panel lateral sirve para colocar los *input* o entradas de datos a procesar, y el panel principal para colocar los elementos de salidas o *output* como resultados después del procesamiento del servidor. ahora veremos cuales son los tipos de elementos de entrada disponibles a continuación:

+ numericInput  
+ sliderInput   
+ textInput    
+ selectInput  
+ radioButtons  
+ checkboxGroupInput  
+ checkboxInput  
+ dateInput  
+ dateRangeInput  
+ actionButton  
+ submitButton  
+ fileInput  

Estos elementos son funciones que tiene parámetros que más adelante lo vamos a definir con detalle. Es de notar que estos elementos deben estar insertados dentro de la función ```sidebarPanel()``` además tienen un parámetro en común que es el "InputId" que no es más que el identificador o el nombre con lo cual el sistema ubica dicho elemento.  


*** =instructions

Coloque un elemento para ingresar números cuyo identificador sea "primero" y uno para ingresar texto identificador sea "abecedario" y que el parámetro "label" sea igual a "Vision" dentro de la interfaz de usuario.

*** =hint

Use los entradas numericInput y textInput dentro del ambiente sidebarPanel.

*** =pre_exercise_code
```{r}
library("shiny")
```

*** =sample_code
```{r}
# ui <- fluidPage(

    # titlePanel("Vision With DataCamp fluidPage"),
  
  # sidebarLayout(
  
    # sidebarPanel(

        #           ,
        #           ),
  
    # mainPanel())
  
  #)
```

*** =solution
```{r}
# ui <- fluidPage(

    # titlePanel("Vision With DataCamp fluidPage"),
  
    # sidebarLayout(
    # sidebarPanel(

        # numericInput(inputId = "primero"),
        # textInput(inputId = "abecedario", label = "Vision")),
  
    # mainPanel())
  
  #)
```

*** =sct
```{r}
msg = "¡Asombroso! ya puedes contruir una interfaz de usuario"
success_msg("Excelente estás ampliando tu interfaz")
```



--- type:NormalExercise lang:r xp:100 skills:1 key:09b800273c
## Componentes de Salida.

Los componentes de salidas en las aplicaciones shiny generalmente se colocan en el panel principal, por lo cual se deben colocar como argumentos dentro de la función ```mainPanel()```, además los mismo deben ser configurados en el servidor lógico ```server.R```, por tanto cada salida tiene su contraparte en el servidor lógico, a continuación te mostramos las principales salidas con sus contraparte en el archivo ```server.R```. Además estas funciones también debe colocarsele sus identificadores 

| mainPanel          | server.R        |
|--------------------|-----------------|
| textOutput         | renderText      |
| verbatimTextOutput | renderPrint     |
| htmlOutput         | renderPrint     |
| tableOutput        | renderTable     |
| imageOutput        | imageOutput     |
| uiOutput           | renderUI        |
| downloadButton     | downloadHandler |


*** =instructions

+ Coloque como argumento de la función ```mainPanel()``` una salida de texto cuyo identificador sea "abecedarioOutput"


*** =hint

Debe elegir la función "textOutput()" 

*** =pre_exercise_code
```{r}
library("shiny")
```

*** =sample_code
```{r}
# ui <- fluidPage(

    # titlePanel("Vision With DataCamp fluidPage"),
  
    # sidebarLayout(
    # sidebarPanel(

        # textInput(inputId = "abecedario", label = "Vision")),
  
    # mainPanel(
    
    #coloque una función de salida para texto
    #
    
    #))
  
  #)
```

*** =solution
```{r}
# ui <- fluidPage(

    # titlePanel("Vision With DataCamp fluidPage"),
  
    # sidebarLayout(
    # sidebarPanel(

        # textInput(inputId = "abecedario")),
  
    # mainPanel(
    
    #coloque una función de salida para texto
    # textOutput(outputId = "abecedarioOutput")
    
    #))
  
  #)
```

*** =sct
```{r}
msg = "¡Genial! ya puedes configurar tus salidas"
success_msg("Excelente")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:6997f0f5fe
## Servidor Lógico __server.R__

El Servidor Lógico es el que ejecuta  y procesa las acciones requeridas en las aplicaciones R Shiny, el mismo recibe instrucciones mediante los input y los procesos son expresados en script de R. Estos se colocan como parte de la variable server dentro de la función ```function(input, output){...}```, los mismos se llaman a través de variables y funciones de la forma ```output$"Id-output" <- render"*"({...})``` donde el __Id-output__: es el nombre o identificador del elemento de salida en la interfaz de usuario y "*" es la contraparte del servidor lógico de la salida en la UI. ejemplo para un ```verbatimOutput("primeroOutput")``` correspondiente a una salida numérica en la UI, y con un ```numericInput("primero")``` como entrada de datos, la configuración quedaría:

```
server <- function(input, output){

output$primeroOutput <- renderPrint({

  input$primero
})

}

```


*** =instructions

Configurar a través del servidor lógico la salida de la interfaz de usuario descrita en el código de ejemplo.

*** =hint

Use la función ```renderText()``` dentro del ambiente del servidor lógico

*** =pre_exercise_code
```{r}
library(shiny)
```

*** =sample_code
```{r}
# ui <- fluidPage(

    # titlePanel("Vision With DataCamp fluidPage"),
  
    # sidebarLayout(
    # sidebarPanel(

        # textInput(inputId = "abecedario", label = "Vision")),
  
    # mainPanel(
    
    #coloque una función de salida para texto
    # textOutput(outputId = "abecedarioOutput")
    
    #))
  
  #)
  
# server <- function(input, output) {

    #output$... <- render...({

  #input$...

#})

#}
  
  
```

*** =solution
```{r}
# ui <- fluidPage(

    # titlePanel("Vision With DataCamp fluidPage"),
  
    # sidebarLayout(
    # sidebarPanel(

        # textInput(inputId = "abecedario", label = "Vision")),
  
    # mainPanel(
    
    #coloque una función de salida para texto
    # textOutput(outputId = "abecedarioOutput")
    
    #))
  
  #)
  
# server <- function(input, output) {

    #output$abecedarioOutput <- renderText({

  #input$abecedario

#})

#}
  
# shinyApp(ui, server)  
```

*** =sct
```{r}
msg = "¡Lo hiciste! ya puedes hacer tus aplicaciones con R"
success_msg("Felicitaciones ya tienes los elementos básicos para construir una aplicación R Shiny")
```
