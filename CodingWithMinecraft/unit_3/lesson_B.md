### @explicitHints 0
# Actividad: Empresa de mudanzas en Minecraft

## Paso 1
Arrastra tres bloques ``||Player:con el comando de chat||`` al espacio de programación.

Cambia los nombres dentro de estos bloques ``||Player:con el comando de chat||`` a **"inicio"**, **"final"** y **"clonacion"**.

```blocks
player.onChat("inicio", function () { })
player.onChat("final", function () { })
player.onChat("clonacion", function () { })
```

## Paso 2
Vamos a crear dos **variables**. Entra en ``||Variables:VARIABLES||`` y haz clic en el botón **Crear una variable**. 

Llama a la primera variable **posicion_inicial**, y haz clic en **Aceptar**.

## Paso 3
Crea otra variable de nombre **posicion_final**, y haz click en **Aceptar**.

## Paso 4
Vamos a asignar valores a las variables. Coloca un bloque de  ``||Variables:establecer||`` variable dentro del bloque ``||Player:con el comando de chat||`` **"inicio"**.

En el desplegable del bloque ``||Variables:establecer||`` selecciona la variable ``||Variables:posicion_inicial||`` para asignarle inicialmente el valor **0**.

## Paso 5
Arrastra ``||Player:posición del jugador en el mundo||`` dentro de ``||Variables:establecer posicion_inicial||`` para reemplazar al valor **0**.

```blocks
player.onChat("inicio", function () {
    posicion_inicial = player.position()
})
```
## Paso 6
Vamos a sacar algunos mensajes por pantalla. Añade un bloque ``||Player:decir||`` a continuación de ``||Variables:establecer posicion_inicial||``. 

## Paso 7
En los bloques avanzados, entra en ``||Text:TEXTO||``, y coloca ``||Text:unir||`` dentro del bloque ``||Player:decir||``, reemplazando a **":)"**.

En el primer hueco de ``||Text:join||``, escribe **"Punto de inicio: "**.

## Paso 8
A continuación, entra en ``||Variables: VARIABLES||``y arrastra la variable ``||Variables: posicion_inicial||`` al segundo hueco del bloque ``||Text:unir||``.

Es importante que observes detenidamente tu código y que te des cuenta de lo que hará tu programa al ejecutar el comando de chat "inicio". Si tienes dudas, pregúntale al profesor. Puedes salir del CodeBuilder, mover tu jugador y teclear el comando de chat "inicio" para comprobar qué sucede.

```blocks
player.onChat("inicio", function () {
    posicion_inicial = player.position()
    player.say("Punto de inicio establecido: " + posicion_inicial)
})
```

## Paso 9
Vamos a repetir para el comando de chat **"final"** lo mismo que hemos hecho para el comando "inicio". Haz clic con el botón derecho sobre el bloque ``||Player:con el comando de chat||`` **"inicio"** y escoge la opción **Duplicar**. Cambia el nombre del comando  a **"final"** en el bloque que acabas de duplicar. 
Asegúrate que en el bloque ``||Variables: establecer||`` seleccionas la variable ``||Variables: posicion_final||``.
Cambia también el texto del bloque ``||Player: decir||`` para que aparezcan **"Punto opuesto:"** y la variable ``||Variables: posicion_final||`` en los dos huecos del bloque ``||Text: unir||``. 

## Paso 10
Borra ("Eliminar bloque") al hacer clic con el botón derecho del ratón) sobre el **bloque vacío** ``||Player:con el comando de chat||`` **"final"**.

## Paso 11
Vamos a programar ahora el comando **"clonacion"**. Entra en ``||Blocks:BLOQUES||``, y arrastra un bloque ``||Blocks:clonar||`` dentro del bloque ``||Player:con el comando de chat||`` **"clonacion"**.
Date cuenta de que el bloque ``||Blocks:clonar||`` incluye **3 posiciones (coordenadas)**: "clonar **de**", "clonar **a**" y "clonar **en**" 

``` blocks
player.onChat("clonacion", function () {
    blocks.clone(
    pos(~0, ~0, ~0),
    pos(~0, ~0, ~0),
    pos(~0, ~0, ~0),
    CloneMask.Replace,
    CloneMode.Normal
    )
})
```

## Paso 12
Entra en ``||Variables:VARIABLES||`` y arrastra la variable ``||Variables:posicion_inicial||`` a la primera posición (**"de"**) dentro bloque ``||Blocks:clonar||``. Tu primera posición deberia aparecer ahora como **clonar de posicion_inicial**.

## Paso 13
Entra en ``||Variables:VARIABLES||``, y arrastra la variable ``||Variables:posicion_final||`` a la segunda posición (**"a"**) dentro del bloque ``||Blocks:clonar||``. El bloque bería aparecer ahora como **clonar de posicion_inicial a posicion_final**.

```blocks
player.onChat("clonacion", function () {
    blocks.clone(
    posicion_inicial,
    posicion_final,
    pos(~0, ~0, ~0),
    CloneMask.Replace,
    CloneMode.Normal
    )
})
```

## Paso 14
Prueba ahora tu programa en Minecraft. En primer lugar deberás construir una estructura sencilla con bloques (una casa, una torre, etc.), que a través de nuestro programa vamos a clonar en otra posición distinta a las coordenadas en las que ha sido construida originalmente. 
Mueve tu jugador a una de las esquinas inferiores de tu estructura, abre la **ventana de chat** en Minecraft (con la letra **t**) y teclea en ella el comando "**inicio**". 

## Paso 15
Desplaza ahora tu jugador en diagonal a la esquina superior de tu estructura  (opuesta en diagonal al punto que has marcado anteriormente en el comando "inicio"). Tal vez tengas que utilizar alguna escalera para subir a ese punto opuesto en diagonal. Una vez allí, abre una ventana de chat en Minecraft y teclea el comando "**final**".
A continuación, desplaza a tu jugador a un espacio abierto dentro del mundo, abre una ventana de chat y teclea el comando "**clonacion**". Si el programa funciona correctamente, debería de replicarse exactamente la estructura en la posición en la que se encuentre ahora el jugador. Fíjate que en el bloque verde clonar ``||Blocks: clonar||`` le estamos diciendo que clone la estructura **en** la posición **(~0, ~0, ~0)**. Recuerda que el símbolo **~** delante de las coordenadas significa que estamos trabajando con coordenadas relativas a la posición del jugador. **Posible pregunta de examen**: ¿Qué posición representan las coordenadas **(~0, ~0, ~0)**?

``` blocks
player.onChat("inicio", function () {
    posicion_inicial = player.position()
    player.say("Punto de inicio: " + posicion_inicial)
})
player.onChat("final", function () {
    posicion_final = player.position()
    player.say("Punto opuesto: " + posicion_final)
})
player.onChat("clonacion", function () {
    blocks.clone(
    posicion_inicial,
    posicion_final,
    pos(~0, ~0, ~0),
    CloneMask.Replace,
    CloneMode.Normal
    )
})
```
    
