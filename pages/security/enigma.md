---
title: Enigma
tags: [security, network_security, enigma]
keywords:
summary: "This posts will be written in spanish, because scholar necessities."
sidebar: security_sidebar
permalink: enigma.html
folder: security
---
## Cómo funcionaba la maquina enigma?

### ¿Qué es?
Como toda buena criptografia, enigma es facíl de entender, pero dificil de romper.

En la frontera de lo mecanico y lo electrico, por fuera enigma luce como una maquina de escrbir con un tamaño descomunal.

Es una maquina de encriptación usada por lo Alemaia durante la Segunda Guerra Mundial, para transmitir mensajes codificados, una maquina Enigma permite codificar un mensaje en millones y millones de formas.

### Cómo funciona?
El sistema esta construido alrededor de tres rotores, cada uno de los rotores toma una letra y devuelve una diferente; Una letra pasa por los tres rotores y al final rebota en un "reflector" que la hace pasar por los mismos tres rotores pero en orden contrario.

El tablero en la caja enciende una luz para mostrar el resultado de la letra encriptada, y el primer rotor rota una posición cambiando así la salida incluso si la entrada es la misma letra que la anterior.

Cuando el primer rotor a rotado en 26 posiciones, el segundo comienza a rotar, cuando el segundo ha hecho los mismo, el tercer rotor hace lo mismo, dandonos asi mas de 17 mil combinaciones posibles hasta que proceso de encriptación se repita

### Esquema de funcionamiento
{% include image.html file="enigma.svg" url="http://jekyllrb.com" alt="Jekyll" caption="Esquema de funcionamiento" %}

1. Se tipea cada letra del mensaje en un teclado estandar.
2. La señal pasa a traves de un panel de conexiones donde cambiar de una letra a otra.
3. Tres rotores, internamente cableados como spagetti, cada uno cambiar la letra de salida antes de que un reflector haga que la letra vuelva a pasar por los rotores  en dirección contraria.
4. Para agregar complejidad, el primer rotor rota un paso luego de cada entrada.
5. La señal reflejada hace una segunda pasada a traves del panel de conexiones.
6. Finalmente la señal enciende una letra en un tablero.
7. El remitente copia el mensaje encriptado y lo envia en clave morse.
8. El destinatario recibe un aparante garimatias(lenguaje dificil de comprender), al presionar la letra A, se enciende una letra F y poco a poco el mensaje encriptado se vuelve claro.