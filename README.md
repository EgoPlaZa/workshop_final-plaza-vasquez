# 💻 RVfpga SoC THE IMAGINATION UNIVERSITY PROGRAMME

Desarrollo de los laboratorios RVfpga de IMAGINATION. Se hará uso de los conocimientos adquiridos a lo largo del semestre, utlizando las herramientas verilog, verilator, gtkwave entre otros. Se realizarán los dos primeros laboratorios del curso de IMAGINATION.

## 💻 Lab1

En este primer laboratorio se nos enseña la construcción del subconjunto SweRVolfX de RISC-V en un chip (SoC) a partir de bloques de construcción.

1. Se empieza con la instalación del programa Verilog, en el cual se desarrollara el laboratorio.
2. Se crea el proyecto con la ayuda de la guía en el documento RVfpgaSoC.
3. Se ingresa a la creacion del diseño de bloques.
4. Se agregan los modulos necesarios para el diseño.
5. Se realizan las conexiones internas, entre los modulos del diseño, pin por pin o bus por bus dado el caso.
6. Se continua con las conexiones externas.
7. Finalizando el diseño y procediendo a generar el archivo verilog con la descripción de este mismo.
8. Por ultimo se configura la creación del bitstream para luego generarlo.


En el siguiente link hay un PDF con todas las [conexiones entre modulos.](BlockDesign.pdf) (Para una mayor facilidad de lectura descargar el PDF)

### 🎯 Resultados

![Alt text](https://i.imgur.com/mNLRNXc.png)

Cómo se puede observar por el gráfico anterior se llegó hasta la última parte como se nos indicó en la guía, generando el bitstream de manera correcta.

## 💻 Lab2


### 🎯 Resultados

Obtención de las señales en GTKWave:

![Alt text](https://i.imgur.com/frx1Q0x.png)


### 🔖 Errores
- Es importancia descargar las versiones que se indican en la guia de instalación, se obtuvieron problemas al momento de generar el bitstream puesto que se usó una versión posterior a la 2019.2.
- El tener un buen procesador facilita y acelera el uso de las herramientas como vivado. Se tuvo que dejar durante varias horas encendido el computador para la generación del bitstream por los bajos recursos que presenta el procesador. 

- Durante el desarrollo del segundo laboratorio encontramos un error al momento de hacer la generación de bits para el RVfpgaSim. S

![Alt text](https://i.imgur.com/VwpLzZA.png)

Este error se pudo arreglar agregando las siguientes ibrerias en la dirección donde se encontraba el archivo verilated.cpp en la carpeta de cygdrive.
```
#include <limits>
#include <cstddef>
#include <iostream>
```

### 🔖 Conclusiones
- Al hacer un modulo es necesario hacer un etiquetado diciente de los terminales, en este laboratorio se podia intuir hacia donde iban o como era la conexión pertinente, haciendo facil este trabajo.
- En el momento de crear el archivo vivado del diseño creado, Vivado arroja una alerta indicando que todos los terminales que no esten interconectados seran enviados a tierra "0".

### 🔖 Referencias
- Curso de RISC-V [link](https://riscv.org/risc-v-learn-online/)

### Autores
Diego Julian Plaza Quintero - Est. Ingenieria electrónica - 2172310
<br/>
egoplaza20@gmail.com
<br/>
Carlos Alberto Vásquez Serrano - Est. Ingenieria electrónica - 2170449
<br/>
carlosalvase@gmail.com
