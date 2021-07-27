---
title: '2-Mecanizado CNC'
date: 2020-06-17T19:30:08+10:00
draft: false
weight: 2
summary: Encargo 3 Mecanizado CNC
---

<!-- Ejemplos de códigos Markdown -->

# <a name="top"></a>Encargo 3:  
---



En el siguiente encargo, se nos pidió trabajar a partir de un producto en específico: silla Fresia. Para este ejercicio se empleó como guía los tutoriales dispuestos para luego reescribir y redactar los diversos pasos. A continuación se presentará una contextualización e información del mecanizado CNC como también imágenes de apoyo que muestren este ejercicio llevado a cabo fuera de lo digital. 

## Un poco de historia e información 

La sigla CNC resume **"control numérico por computadora"** lo que implica una función de mecanizado que será determinada por un programa que le dicte (controle) ciertos movimientos de herramientas o máquina a realizar. 
Recordar el incio de las computadora con le segunda guerra mundial es crucial para tener una idea de cuánto se ha avanzado tecnológicamente para poder lograr el uso que actualmente se tiene con máquinas cnc guiadas por un computador -hoy de dimensiones más pequeñas de las vistas a mitad del siglo XX-. 


El ingeniero John Parsons, resulta personaje clave para la existencia de CNC. Sus trabajos e intentos lo llevaron a generar un sistema de cinta perforada que entregaba coordenadas de posición para controlar la máquina. Con los años, este sistema fue tomado por las Fuerzas Aéreas de Estados Unidos. 



![Sistema de cinta](/img/mecanizado/cinta.jpg)



Luego, el origen de CNC nos lleva hasta los años 50 y al MIT, lugar donde se logró automatizar por primera vez una fresadora. Las primeras máquinas de CNC trabajaban bajo herramientas que ya existían y que se modficaron con motores que movían controles que seguían puntos -agujeros- en el sistema de cinta perforada de Parsons. 

Las máquinas CNC logra realizar movimientos simples como también complejos, gracias al control de movimientos que implica regular la posición y velocidad de los motores que activan los ejes de las máquinas. Así se le da órdenes a las máquinas para que ejecuten actividades como hacer una ranura en la madera, bajorrelieves, etc. 

### Funcionamiento

Tal como se explicó brevemente en la sección anterior, para que CNC funcione, se necesita un computador que controle los movimientos de la máquina elegida para realizar el trabajo. Se relacionan a través de un programa que los comunique, software propio. El controlador de CNC trabaja y se mueve en base a motores (servomotores y motores paso a paso), y también de componenetes de accionamiento que realizan desplazamientos en los ejes de la máquina para que esta ejecute los movimientos ingresados en el computador (programados). 

A continuación se presenta un diagrama del funcionamiento de una máquina CNC típica, provista de servomotores. 

![diagrama](/img/mecanizado/diagrama.gif)


Tal como se observa, la máquina CNC se compone de 6 elementos: 
* Dispositivo de entrada
* Controlador
* Máquina herramienta
* Sistema de accionamiento
* Dispositivo de realimentación (servomotores)
* Monitor

---
## Procedimiento Silla Fresia

#### Paso 1
Como primer paso, debemos generar una tabla -plancha- de trabajo a través de Sketch y generando un rectángulo de 1220 mm x 1220 mm. Luego, lo extruímos para que tenga un grosor de 15 mm. 

![paso1](/img/mecanizado/1.png)

#### Paso 2
Con la tecla *Move/copy* copiamos pieza por pieza, las partes de la silla y las fijamos en la plancha de trabajo. Para esto, las debemos alienar, dejándolas todas en la **misma dirección** desde el plano seleccionado. 
*Se selecciona la cara que no tiene calado de la pieza y se alinea con la plancha. De esta manera todas estarán en la misma dirección* 

![paso2](/img/mecanizado/2.png)

Repetimos este paso con todas las piezas y las acomodamos. 
 
#### Paso 3
Ya que tenemos las piezas en la plancha, dejamos sin visualizar la plancha, y cambiamos del modoo Design a Manufacture. En esta sección vamos a *Setup* para configurar la herramienta a usar: Autodesk CNC de 3 ejes genérica. 

Luego, debemos seleccionar la plancha *-con stock/from solid-* y las piezas con las que trabajaremos para cortar. La orientación del corte debe ser en eje Z y plano XY, también indicamos que el punto de origen de la máquina es el punto izquierdo superior de nuestra plancha. 

#### Paso 4
Realizamos *2d contour* en las piezas, para esto seleccionamos los contornos inferiores de los orificios de cada pieza. Seleccionamos la máquina que se mencionó en paso 3. 

![paso3](/img/mecanizado/3.png)

**Como nuestra máquina no alcanza de una sola vez a perforar la plancha, debemos editar nuestra profundidad en *passes/Multiple Depths* y cambiamos el Maximum Roughing a 3 mm. La fresa generará un paso de 5 veces por el  mismo lugar para abarcar la profundidad**


#### Paso 5

Realizamos *2D Pocket Countour* para esto seleccionamos las partes de las piezas correspondientes y nos aseguramos que la máquina elegida sea la misma que la anterior. 

![paso4](/img/mecanizado/4.png)

**Debemos fijarnos en la misma acotación señalada en el paso anterior, sobre la profundidad**

#### Paso 6

Nuevamente usamos *2D Contour*, pero de manera externa, es decir, el contorno de cada pieza. 

![paso5](/img/mecanizado/5.png)

El cuidado que se debe tener es de fijar bien los Tabs de las piezas, puesto que sin estos, las piezas que se cortan al inicio podrían moverse y generarían probelmas con las siguientes. Agregamos *Tabs* de altura 3 mm y una amplia distancia entre estos de 350 mm. 

###### Así se ven los pasos entregados, en las patas traseras de la silla: 

![paso6](/img/mecanizado/6.png)

#### Asiento

Para trabajar con el asiento debemos modificar el paso 1. Puesto que la plancha que generaremos es de 9 mm. Las otras dimensiones de la plancha deben corresponder a un contorno holgado de este, fijándonos en la dirección del eje Z. Luego trabajamos de la misma manera en base a los paso 2 y 3. 

Luego, con *2D Tracer* nos fijamos en las curvas internas de esta pieza. Modificamos Stock to Leave para que sea de 4.5 mm, de esta manera, la fresa no completa el trazado en la tabla, lo que la hace maleable.




## Imágenes

A continuación se presentan las imágenes editadas con Adobe Illustrator para este ejercicio, en formato planimetría.

{{< gallery dir="/img/planenc2/" />}} {{< load-photoswipe >}} 


{{< iframe-fusion link="https://alumnos4792.autodesk360.com/shares/public/SH56a43QTfd62c1cd96868ff56253a97ff74?mode=embed" >}}

---

### Galería ejemplos
{{< gallery dir="/img/mecgaleria/" />}} {{< load-photoswipe >}}





---
### Fuentes

[cncsur](https://cncsur.cl/cnc-la-historia-del-control-numerico/)

https://wiki.ead.pucv.cl/Introducci%C3%B3n_al_control_num%C3%A9rico_computarizado_(CNC) 




[[Volver Arriba]](#top)