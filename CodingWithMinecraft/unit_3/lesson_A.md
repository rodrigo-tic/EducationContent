### @explicitHints 0

# Actividad 3 (Lección A): Crea una brújula

## Paso 1
Crear un nuevo comando de chat. Arrastra un bloque ``||Player:con el comando de chat||`` al espacio de programación y cambia el nombre del comando, por ejemplo, a **brujula"**.

``` blocks
player.onChat("brujula", function () {
})

```

## Paso 2 
Ahora, coloca un bloque ``||Blocks:rellenar con||`` dentro del bloque ``||Player:con el comando de chat||``. 
Modifica el bloque ``||Blocks:rellenar con||`` para que en lugar de **hierba** tenga el material del que quieras construir tu **eje X**. Por ejemplo, puedes usar **lana gris** para el eje.

## Paso 3
Pon los valores de coordenadas **(~-10 ~-1 ~0)** en **de** y **(~10 ~-1 ~0)** in **a**. Esto va a dibujar una línea de 21 bloques a lo largo del eje X. La línea de bloques estará por debajo de tus pies y tú estarás situado en el centro de la línea. 

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
Imprime las direcciones Este y Oeste en los extremos del eje X. Busca el bloque ``||Blocks:imprimir||``. Mediante este bloque vamos a imprimir letras o palabras a lo largo del eje especificado, utilizando el material que escojas para imprimr las palabras.

## Paso 5
Arrastra dos bloques ``||Blocks:imprimir||`` y colócalos a continuación del bloque ``||Blocks:rellenar con||``. 
Pon la letra **"O"** en el primer bloque  ``||Blocks:imprimir||`` y la letra **"E"** en el segundo bloque ``||Blocks:imprimir||`` para indicar el Oeste y el Este.

## Paso 6
Selecciona un bloque ``||Blocks:imprimir||`` para imprimir las letras. En este ejemplo, utilizaremos **lana lima** para el Oeste y **lana amarilla** para el Este.

## Paso 7
En el bloque ``||Blocks:imprimir||`` **"O"**, pon las coordenadas **(~-11 ~0 ~0)**.

En el bloque ``||Blocks:imprimir||`` **"E"**, pon las coordenadas **(~11 ~0 ~0)**.

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
En este momento, te recomiendo que pruebes en Minecraft si tu programa dibuja correctamente el eje E/O de la brújula. Vete a un espacio abierto, abre una ventana de chat (tecla **t**) y escribe el comando **brujula**. Si el eje E/O no se ha creado correctamente, revisa las coordenadas que has puesto en el código de tu programa.

## Paso 8
Repite las acciones para el Norte y el Sur. Coloca un bloque ``||Blocks:rellenar con||`` dentro de ``||Player:con el comando de chat||``.

Cambia el bloque de **hierba** en el bloque ``||Blocks:rellenar con||`` al material que quieras construir para el **eje Z (Norte / Sur)**. En este ejemplo utilizaremos **lana negra** para el eje.

## Paso 9
Pon las coordenadas **(~0 ~-1 ~-10)** en **de** y **(~0 ~-1 ~10)** en **a**. Esto dibujará una línea de bloques a lo largo del **eje Z**.

## Paso 10
Arrastra dos bloques ``||Blocks:imprimir||`` al área de programación y colócalos después del bloque ``||Blocks:rellenar con||`` que acabábamos de colocar.

## Paso 11
Escribe **"N"** en el primer bloque ``||Blocks:imprimir||`` y **"S"** en el segundo bloque ``||Blocks:imprimir||`` para indicar las direcciones del Norte y del Sur.

## Paso 12
Selecciona algún material para imprimir mediante los bloques ``||Blocks:imprimir||`` las legras N y S. En este ejemplo utilizaremos **lana azul** para el Norte y **lana roja** para el Sur.

## Paso 13
En el primer bloque ``||Blocks:imprimir||`` **"N"**, pon las coordenadas **(~0 ~0 ~-11)**. 

En el segundo bloque ``||Blocks:imprimir||`` **"S"**, pon las coordenadas **(~0 ~0 ~11)**.

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

## Paso 14
Ahora, prueba tu programa en Minecraft. Vete a un espacio abierto, abre la ventana de chat (con la letra **t**) y escribe el comando **brujula**. Comprueba si se han creado los dos ejes N/S y E/O correctamente. Si no, revisa tu programa, puede que no hayas escrito las coordenadas correctamente.
