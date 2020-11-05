# PIC C Ejemplo 14: Sistema de registro de datos

![Build](../../workflows/Build/badge.svg)
![Test](../../workflows/Test/badge.svg)

En este ejemplo se implementará un sistema de registro de datos con las siguientes características:

1. El sistema debe contar cuantas veces se presiona cada tecla (TEC1, TEC2, TEC3 o TEC4).
2. Si recibe la letra `'Q'` por puerto serie, debe responder enviando un informe con esas cantidades.
    Por ejemplo:
    ```shell
    Informe de teclas:
    ---------------------
        TEC1: 12
        TEC2: 4
        TEC3: 6
        TEC4: 17
    ---------------------
    ```
3. Recuerda que para que cualquier terminal detecte el fin de línea se debe enviar `\r\n`.
4. Cuando se recibe la letra `'D'` por puerto serie, debe reiniciar los contadores de las teclas.
5. Si se recibe un comando válido debe parpadear el led verde (100 ms).  
   Si se recibe un comando inválido debe parpadear el led rojo (100 ms).

Se utiliza el entorno de desarrollo MPLAB X v5.30 y el compilador XC8 v2.20.

## Archivos base del proyecto de MPLAB X IDE

- nbproject/configurations.xml
- nbproject/project.xml
- Makefile
- main.c

## Archivos adicionales

- circuit.pdsprj:  
    Proyecto de `Proteus Design Suite 8.9` utilizado para simulación.

- mplab_conf.zip:  
    Archivo de opciones exportado del `MPLAB X IDE`.  
    Se puede importar a partir del menú `Tools -> Options -> Import...`.

- .gitignore:  
    Archivo para configurar qué directorios debe ignorar `git`.
