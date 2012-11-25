SASS Lang
=========

SASS es una Gema Ruby la cual permite pre-procesar CSS incluyendo: funciones (mixin), variables, creacion de cascada de manera dinamica (selectores anidados), herencias y entre otras cosas.

## Sintaxis CSS

SASS maneja los mismos selectores y sintaxis por defecto de CSS, pero tambien permite usar sintaxis que no necesita los parentesis ni los ";" al final de cada linea, solo necesita indentacion y salto de lineas. Esta seleccion de sintaxis se hace por medio de la terminacion del archivo fuente SASS, si el archivo tiene como terminacion .scss la sintaxis sera la similar a la de CSS; Si la terminacion es .sass se usara la sintaxis simplificada (tipo python).

## Reglas CSS

Este ejemplo colocaremos una entrada de un archivo SASS y su respectiva salida salida en CSS.

### Sintaxis basica SASS

```sass
  // Selector de id
  #indentificador {
    propiedad: valor;
  }
  
  // Selector de class
  .clase {
    propiedad: valor;
  }
  
  // Selector anidado
  .clase_superior {
    propiedad: valor;
    .clase_interna {
      propiedad: valor;
    } 
  }
```

>NOTA: no existe en css ninguna propiedad llamada propiedad ni ningun valor llamado valor, eso hace referencia a cualquier propiedad css y a cualquier valor posible para dicha propiedad.
  
### Salida CSS al ejemplo anterior

```css

  #indentificador {
    propiedad: valor;
  }
  .clase {
    propiedad: valor;
  }
  .clase_superior {
    propiedad: valor;
  }
  .clase_superior .clase_inferior {
    propiedad: valor;
  }
  
```
## Variables

### Declaracion de variables

```sass
  $nombre_variable_1: valor1;
  $nombre_variable_2: valor2;

  #identificador {
      propiedad: $nombre_variable_1;
      propiedad: $nombre_variable_2;
  }

  etiqueta {
    propiedad: $nombre_variable_1;
  }
```

### Ejemplo en SASS

 ```sass
    $color: #3bbfce;
    $margen: 16px;

    .contenido {
    border-color: $color;
    color: darken($blue, 9%);
    }

    .borde {
    padding: $margen / 2;
    margin: $margen / 2;
    border-color: $color;
    }
```

### Salida en CSS 

```css
  .contenido {
  border-color: #3bbfce;
  color: #2b9eab;
  }

  .border {
  padding: 8px;
  margin: 8px;
  border-color: #3bbfce;
   }
```


## Funciones

### Declaracion de las Funciones
