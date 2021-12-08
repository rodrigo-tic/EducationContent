### @explicitHints 0

# Last Stand at the Alamo 

```template
mobs.spawn(mobs.monster(ZOMBIE), pos(0, 0, 5))
``` 

## Paso 1
Reacciona al evento "zombie muerto": Entra en la sección ``||Mobs:CRIATURAS||`` y arrastra un bloque **gestor de eventos** ``||Mobs:en animal matado||`` al área de programación.

```blocks
mobs.onMobKilled(CHICKEN, function () {
})
```

## Paso 2
Vamos a hacer que nuestro **gestor de eventos** ``||Mobs: en animal matado||`` reaccione solamente a la muerte de **monstruos** (no de animales): Entra en ``||Mobs:CRIATURAS||`` y arrastra un bloque con un desplegable de huevos de ``||Mobs:monstruo||`` para reemplazar al huevo de ``||Mobs:animal||`` que teníamos por defecto en nuestro gestor de eventos . 
Utiliza el menú desplegable para seleccionar un huevo de **zombie**.

## Paso 3
¡Vamos a engendrar más zombies! Entra en ``||Mobs:CRIATURAS||`` y arrastra  un bloque  ``||Mobs:huevo de animal||`` dentro del gestor de eventos ``||Mobs:en monstruo matado||``.

```blocks
mobs.onMobKilled(mobs.monster(ZOMBIE), function () {
mobs.spawn(CHICKEN, pos(0, 0, 0))
})
```

## Paso 4
Al igual que hiciste en el paso 2, reemplaza el huevo de animal por un huevo de ``||Mobs:monstruo||`` de la sección ``||Mobs:CRIATURAS||``.

```blocks
mobs.onMobKilled(mobs.monster(ZOMBIE), function () {
mobs.spawn(mobs.monster(ZOMBIE), pos(0, 0, 0))
})
```

## Paso 5
Dos zombies dan más miedo que uno. Vas a engendrar dos zombies por cada uno que mates, así que entra en ``||Loops:BUCLES||`` y arrastra un bucle ``||Loops:repetir||`` al área de programación. Este bucle ``||Loops:repetir||`` lo colocarás dentro del gestor de eventos ``||Mobs:en mostruo matado||`` y tu bloque ``||Mobs:huevo de monstruo||`` irá dentro del bucle ``||Loops:repetir||``.

En el bucle ``||Loops:repetir||`` escribe el número **2**. 

```blocks
mobs.onMobKilled(mobs.monster(ZOMBIE), function () {
    for (let index = 0; index < 2; index++) {
        mobs.spawn(mobs.monster(ZOMBIE), pos(0, 0, 0))
    }
})
```

## Paso 6
Vamos a hacer que los zombies aparezcan en un lugar aleatorio: sustituye las coordenadas **(~0 ~0 ~0)** por un bloque ``||Positions:escoger posición aleatoria||``.

## Paso 7
Vamos a establecer el rango de coordanadas aleatorio en el que pueden aparecer los zombies: en el bloque ``||Positions:escoger posición aleatoria||``, escribe en **de** las coordenadas **(~10 ~0 ~10)** y en **a** las coordenadas **(~-10 ~0 ~-10)**.


## Paso 8
Prueba tu programa en Minecraft y comprueba que cada vez que matas un zombie aparecen otros dos en posiciones aleatorias
