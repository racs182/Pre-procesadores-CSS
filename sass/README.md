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