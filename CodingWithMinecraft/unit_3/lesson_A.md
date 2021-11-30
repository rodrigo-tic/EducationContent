### @explicitHints 1

# Actividad 3 (Lección A): Crea una brújula

## Paso 1
Crear un nuevo comando de chat ``||Player: on chat||``. Arrastra un bloque ``||Player:on chat command||`` al lienzo de programación y cambia el nombre del comando, por ejemplo, a **brujula"**.

### ~ tutorialhint
``` blocks
player.onChat("brujula", function () {
})

```

## Paso 2 
Ahora, coloca un bloque ``||Blocks:fill with||`` dentro del bloque ``||Player:on chat command||``. 
Modifica el bloque ``||Blocks:fill with||`` para que en lugar de **hierba** tenga el material del que quieras construir tu eje X. Por ejemplo, puedes usar **lana gris** para el eje.

## Paso 3
Pon los valores de coordenadas **(~-10 ~-1 ~0)** en **from** y **(~10 ~-1 ~0)** in **to**. Esto va a dibujar una línea de 21 bloques a lo largo del eje X. La línea de bloques estará por debajo de tus pies y tú estarás situado en el centro de la línea. 

### ~ tutorialhint
``` blocks
    player.onChat("brujula", function () {
        blocks.fill(
        GRAY_WOOL,
        pos(-10, -1, 0),
        pos(10, -1, 0),
        FillOperation.Replace
        )
})
```
## Paso 4
Imprime las direcciones Este y Oeste en los extremos del eje X. Busca el bloque ``||Blocks:print||``. Este bloque imprime palabras a lo largo del eje especificado, utilizando el material que escojas para imprimr las palabras.

## Paso 5
Arrastra dos bloques ``||Blocks:print||`` y colócalos a continuación del bloque ``||Blocks:fill with||``. 
Pon la letra **"O"** en el primer  ``||Blocks:print||`` y la letra **"E"** en el segundo ``||Blocks:print||`` para indicar el Oeste y el Este.

## Paso 6
Selecciona un bloque ``||Blocks:print||`` para imprimir las letras. En este ejemplo, utilizaremos this example, **lana lima** para el Oeste y **lana amarilla** para el Este.

## Paso 7
En ``||Blocks:print||`` **"O"**, pon las coordenadas **(~-11 ~0 ~0)**.

En ``||Blocks:print||`` **"E"**, pon las coordenadas **(~11 ~0 ~0)**.

### ~ tutorialhint
``` blocks
    player.onChat("brujula", function () {
        blocks.fill(
        GRAY_WOOL,
        pos(-10, 0, 0),
        pos(10, 0, 0),
        FillOperation.Replace
        )
        blocks.print(
        "O",
        LIME_WOOL,
        pos(-11, 0, 0),
        WEST
        )
        blocks.print(
        "E",
        YELLOW_WOOL,
        pos(11, 0, 0),
        WEST
        )
})
```

## Paso 8
Repite las acciones para el Norte y el Sur. Coloca un bloque ``||Blocks: fill with||`` dentro de ``||Player:on chat command||``.

Cambia el bloque de **hierba** en el bloque ``||Blocks:fill with||`` al material que quieras construir para el eje Z (Norte / Sur). En este ejemplo utilizaremos **lana negra** para el eje.

## Paso 9
Pon las coordenadas **(~0 ~-1 ~-10)** en **from** y **(~0 ~-1 ~10)** en **to**. Esto dibujará una línea de bloques a lo largo del eje **Z**.

## Paso 10
Arrastra dos bloques ``||Blocks:print||`` al área de programación y colócalos después del bloque ``||Blocks:fill with||`` que acabábamos de colocar.

## Paso 11
Escribe **"N"** en el primer bloque ``||Blocks:print||`` y **"S"** en el segundo bloque ``||Blocks:print||`` para indicar las direcciones del Norte y del Sur.

## Paso 12
Selecciona un bloque de material para imprimir ``||Blocks:print||`` las legras N y S. En este ejemplo utilizaremos **lana azul** para el Norte y lana roja para el Sur.

## Paso 13
En ``||Blocks:print||`` **"N"**, pon las coordenadas **(~0 ~0 ~-11)**. 

En ``||Blocks:print||`` **"S"**, pon las coordenadas **(~0 ~0 ~11)**.

### ~ tutorialhint
``` blocks
    player.onChat("compassrose", function () {
        blocks.fill(
        GRAY_WOOL,
        pos(-10, -1, 0),
        pos(10, -1, 0),
        FillOperation.Replace
        )
        blocks.print(
        "W",
        LIME_WOOL,
        pos(-11, 0, 0),
        WEST
        )
        blocks.print(
        "E",
        YELLOW_WOOL,
        pos(11, 0, 0),
        WEST
        )
        blocks.fill(
        GRAY_WOOL,
        pos(0, -1, -10),
        pos(0, -1, 10),
        FillOperation.Replace
        )
        blocks.print(
        "N",
        BLUE_WOOL,
        pos(0, 0, -11),
        WEST
        )
        blocks.print(
        "S",
        RED_WOOL,
        pos(0, 0, 11),
        WEST
        )
})
```
