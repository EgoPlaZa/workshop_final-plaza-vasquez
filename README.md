# 馃捇 RVfpga SoC THE IMAGINATION UNIVERSITY PROGRAMME

Se realizaron los dos primeros laboratorios RVfpga de IMAGINATION. Se hizo uso de los conocimientos adquiridos a lo largo del semestre en la materia arquitectura para computadores de la UIS, con la ayuda de las herramientas verilog, verilator, gtkwave entre otros. 

## 馃捇 Lab1

En este primer laboratorio se nos ense帽a la construcci贸n del subconjunto SweRVolfX de RISC-V en un chip (SoC) a partir de bloques de construcci贸n. 

Se realizaron los siguientes pasos:

1. Se empieza con la instalaci贸n del programa Verilog, en el cual se desarrollara el laboratorio.
2. Se crea el proyecto con la ayuda de la gu铆a en el documento RVfpgaSoC.
3. Se ingresa a la creacion del dise帽o de bloques.
4. Se agregan los modulos necesarios para el dise帽o.
5. Se realizan las conexiones internas, entre los modulos del dise帽o, pin por pin o bus por bus dado el caso.
6. Se continua con las conexiones externas.
7. Finalizando el dise帽o y procediendo a generar el archivo verilog con la descripci贸n de este mismo.
8. Por ultimo se configura la creaci贸n del bitstream para luego generarlo.


En el siguiente link se encuentra el PDF con todas las [conexiones entre modulos.](BlockDesign.pdf) (Para una mayor facilidad de lectura descargar el PDF)

### 馃幆 Resultados

![Alt text](https://i.imgur.com/mNLRNXc.png)

C贸mo se puede observar por el gr谩fico anterior se lleg贸 hasta la 煤ltima parte como se nos indic贸 en la gu铆a, generando el bitstream de manera correcta.

## 馃捇 Lab2

En este segundo laboratorio se nos indica como ejecutar programas escritos en el lenguaje C o en el lenguaje Assambly en el subconjunto SweRVolfX creado en el primer laboratorio haciendo uso de la herramienta Vivado block.

Se realizaron los siguientes pasos:

1. Se deben instalar los programas VSCode (en este se hace la instalaci贸n de PlatformIO), cygwin (en este se hace la instalaci贸n de verilator) y GTKWave.
2. Se obtiene del primer laboratorio el archivo BD.v en el cual se verifica que cada nombre de los modulos terminen en _0_0.
3. Se generan el binario para RVfpgaSim dentro de la terminal de cygwin.
4. Se obtiene el archivo trace.vcd realizando la simulaci贸n en PlatformIO.
5. Se muestran las se帽ales en el GTKWave.

En el siguiente link se encuentra el archivo [trace.vcd](https://drive.google.com/file/d/1rNC20zOZOhfziusyGDlmFjSkUsuzrFOx/view) generado. 

### 馃幆 Resultados

Se obtuvieron las siguientes se帽ales en GTKWave, las cuales se dividir谩n en 3 instrucciones aritm茅tico-l贸gicas de las primeras y segundas iteraciones del bucle.

- Primera: 
![Alt text](https://i.imgur.com/Ua98Wy5.png)
- Segunda:
![Alt text](https://i.imgur.com/V4yUK1t.png) 
- Tercera:
![Alt text](https://i.imgur.com/s18a98r.png)

Se obtuvo de manera correcta las se帽ales y los ciclos como lo mostraba la gu铆a.

### 馃敄 Errores
- Es importante descargar las versiones que se indican en la guia de instalaci贸n, se obtuvieron problemas al momento de generar el bitstream puesto que se us贸 una versi贸n posterior a la 2019.2.
- El tener un buen procesador facilita y acelera el uso de las herramientas como vivado. Se tuvo que dejar durante varias horas encendido el computador para la generaci贸n del bitstream por los bajos recursos que presenta el procesador. 
- Al intentar hacer el bitstream se encontro un error donde no encontraba los modulos que componian el dise帽o. Se hizo la busqueda y los modulos estaban donde se especificaba, pero el projecto no los reconocia, para solucionarlo se tuvo que comenzar a hacer de nuevo todo el proyecto.

![Alt text](image.png)

- En windows, cuando se buscaba el archivo generado trace.vcd este no aparec铆a en ninguna carpeta. Fue necesario el uso de otro sistema operatico como lo es Linux para hacer la generaci贸n de este.
- Durante el desarrollo del segundo laboratorio encontramos un error al momento de hacer la generaci贸n de bits para el RVfpgaSim, el cual se muestra en la siguiente imagen.

![Alt text](https://i.imgur.com/95wToyx.png)

Este error se pudo arreglar agregando las siguientes librerias al c贸digo en C++ verilated.cpp, este archivo se encuentra dentro de la carpeta dentro de la carpeta cywin64 en archivos de programa y siguiendo la ruta que se nos muestra junto al error.
```
#include <limits>
#include <cstddef>
#include <iostream>
```

### 馃敄 Conclusiones
- Al hacer un modulo es necesario hacer un etiquetado diciente de los terminales, en este laboratorio se podia intuir hacia donde iban o como era la conexi贸n pertinente, haciendo facil este trabajo.
- En el momento de crear el archivo vivado del dise帽o creado, Vivado arroja una alerta indicando que todos los terminales que no esten interconectados seran enviados a tierra "0".
- Se realizaron las correctas simulaciones en el laboratorio 2, esto se puede inferir al momento de realizar la comparaci贸n de las se帽ales obtenidas en gtwave con sus instrucciones.
- Al tener un pipelined de 9 etapas, el programa tarda en empezar a realizar todas las instrucciones estos 9 retardos, por esto primero el procesador se va preparando y pasando por cada etapa, para luego mostrar los resultados de cada instrucci贸n, finalmente se repite el ciclo.

### 馃敄 Referencias
- Curso de RISC-V [link](https://university.imgtec.com/resources/download/rvfpgasoc-v1-0/)
- Xilinx distribuidor de Vivado, programa usado en el laboratorio 1. [link](https://www.xilinx.com/)
- Visual Studio Code, programa usado en el laboratorio 2. [link](https://code.visualstudio.com/)
- Verilator, programa usado en el laboratorio 2. [link](https://verilator.org/guide/latest/index.html)
- Cygwin, programa usado en el laboratorio 2 para windows. [link](https://www.cygwin.com/)
- Gtkwave, programa usado en el laboratorio 2. [link](https://sourceforge.net/projects/gtkwave/)

### Autores
Diego Julian Plaza Quintero - Est. Ingenieria electr贸nica - 2172310
<br/>
egoplaza20@gmail.com
<br/>
Carlos Alberto V谩squez Serrano - Est. Ingenieria electr贸nica - 2170449
<br/>
carlosalvase@gmail.com
