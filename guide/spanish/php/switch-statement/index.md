---
title: Switch statement
localeTitle: Cambiar la declaración
---
# Cambiar

`Switch` es una estructura de control de selección que seleccionará una instrucción de cambio y la ejecutará desde la lista de candidatos. El interruptor consiste en un `case` y un `default` opcional. La ejecución se puede detener utilizando un `break` o `return` .

## Sintaxis
```
switch(x) 
 { 
    case valor1: 
      // se ejecuta si x = valor1 
      break; 
    case value2: 
      // se ejecuta si x = valor2 
      break; 
 
    ... 
 
    default: 
      se ejecuta si x es distinto a los valores candidatos
 } 
```

## Ejemplo

```php
<?php 
 // inicializa una variable con un valor entero aleatorio en un rango
 $valorDado = mt_rand(1, 6); 
 
 // inicializa una cadena vacía a la que luego asignaremos un valor 
 $numText = ""; 
 
 // llamada al switch
  switch($valorDado) 
  { 
  case 1: 
    $numText = "Uno"; 
    break; 
  case 2: 
    $numText = "Dos"; 
    break; 
  case 3: 
  case 4: 
    // case 3 and 4 will go to this line 
    $numText = "Tres o Cuatro"; 
    break; 
  case 5: 
    $numText = "Cinco"; 
    echo $numText; 
    // break; // sin especificar break o return continuará la ejecución al siguiente caso 
  case 6: 
    $numText = "Seis"; 
    echo $numText; 
    break; 
  default: 
    $numText = "desconocido"; 
  } 
 
  // resultado 
  echo 'El dado muestra el número '.$numText.'.'; 
 
 ?> 
```

## Salida
```
si case es 1 
 > El dado muestra el número Uno. 
 
si case es 2 
 > El dado muestra el número Dos. 

si case es 3 
 > El dado muestra el número Tres o Cuatro. 
 
si case es 4 
 > El dado muestra el número Tres o Cuatro. 
 
si case es 5 
 > CincoSeisEl dado muestra el número Seis. 
 
si case es 6 
 > SeisEl dado muestra el número Seis. 
 
si case no coincide con ningún valor
 > El dado muestra el número desconocido. 

```

## Más información:
[PHP.net - Switch](https://secure.php.net/manual/es/control-structures.switch.php)
