# 💻 RVfpga SoC THE IMAGINATION UNIVERSITY PROGRAMME

Desarrollo de los laboratorios RVfpga de IMAGINATION. Se hará uso de los conocimientos adquiridos a lo largo del semestre, utlizando las herramientas verilog, verilator, gtkwave entre otros. Se realizarán los dos primeros laboratorios del curso de IMAGINATION.

## 💻 Lab1

En este primer laboratorio se nos enseña la construcción de un sistema RISC-V en un chip (SoC) a partir de bloques de construcción.

Se empieza con la instalación y posterior uso de Verilog, crearemos nuestro proyecto con la ayuda de la guía que se nos envía en el documento RVfpgaSoC.

En la creacion por bloques se agregan los modulos necesarios para el sistema y luego se hacen las conexiones entre estos, pines o buses, ya sean internas entre modulos o externas, el diagrama se presenta a continuación:

![Alt text](https://i.imgur.com/o1L9O9A.jpg)

### 🎯 Resultados

![Alt text](https://i.imgur.com/mNLRNXc.png)

Cómo se puede observar por el gráfico anterior se llegó hasta la última parte como se nos indicó en la guía, generando el bitstream de manera correcta.

## 💻 Lab2




### 🔖 Conclusiones
- En la creación del diagrama de bloques se agregan los modulos necesarios y estos tienen sus terminales bien marcados, donde se puede hacer las conexiones necesarias internamente, las otras se hacen con conexiones externas teniendo en cuenta que las que no fueron conectadas, vivado entiende que se conectaran a tierra "0". En las conexiones se diferencian los pines a los buses con una linea mas gruesa para los buses.
-Es importancia descargar las versiones que se indican en la guia de instalación, se obtuvieron problemas al momento de generar el bitstream puesto que se usó una versión posterior a la 2019.2.
-El tener un buen procesador facilita y acelera el uso de las herramientas como ivado. Se tuvo que dejar durante varias horas encendido el computador para la generación del bitstream por los bajos recursos que presenta el procesador. 

### 🔖 Referencias
- 
-
-

### Autores
Diego Julian Plaza Quintero - Est. Ingenieria electrónica - 2172310
<br/>
egoplaza20@gmail.com
<br/>
Carlos Alberto Vásquez Serrano - Est. Ingenieria electrónica - 2170449
<br/>
carlosalvase@gmail.com
