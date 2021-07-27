---
title: '3 - Mecanizado 2.5 Ejes'
date: 2020-06-17T19:30:08+10:00
draft: false
weight: 2
summary: Encargo 3 - Mecanizado 2.5 Ejes
---

<!-- Ejemplos de códigos Markdown -->

# <a name="top"></a>Mecanizado 2.5:  
---



En el siguiente encargo, trabajamos a partir de una parte de la silla empleada en el ejercicio anterior, de esta manera se sucede una conexión entre ejercicios que ayudan a generar mayor comprensión de los procesos enseñados en los tutoriales. Nuevamente, hacemos uso del software *Fusion 360* .

Tal como en el ejercicio anterior, debemos poner en contexto el ejemplo que estamos ad portas de desarrollar, para eso recordaremos el proceso de la máquina CNC de 3 ejes y lo compararemos con el ejercicio de este encargo que compete el uso de cortes de 2.5 ejes.


## Información y comparación

Recordemos que la sigla CNC resume **"control numérico por computadora"** lo que implica una función de mecanizado que será determinada por un programa que le dicte (controle) ciertos movimientos de herramientas o máquina a realizar, ya sea cepillado, fresado o corte, entre otros. 

En esta oportunidad nos enfocaremos en un mecanizado con la estrategia de corte de 2.5 ejes, tal como lo vimos en videos en clases, esto implica que la máquina puede y está capacitada para trasladarse y moverse entre los ejes X,Y y Z, pero no de manera alterna, es decir, no puede se puede desplazar en las 3 coordenadas mencionadas de manera simultánea. De esta manera, ejecuta solo cortes en 2 de los 3 ejes mencionados en un mismo instante. Este tipo de mecanizado, es útil para cuando se busca realizar un trabajo específico y de piezas más simples, en donde quizás no se busque la perfección al detalle, es por eso que es utlizada en este ejercicio del respaldo de la Sill Fresia.   

Contrastando esta información con las operaciones en los ejes simultáneos, vemos que estas últimas logran ser más "rápidas" en términos de eficacia y eficiencia, ya que logra actuar en los 3 eje en las trayectorias de cortes que se generan, como se puede ejemplificar como lo visto, con la máquina fresadora, se emplea así, en objetos en que se busca la precisión para generar un resultado más prolijo en sus acabados.




![diferencias](/img/mec2.5/diferenciasejes.jpg)

* Cabe destacar que en mi experiencia, el ejercicio desarrollado a partir del tutorial, no salió exacto al de muestra. Pero de todas maneras, seguí desarrollando el ejercicio. 


---
## Procedimiento en Respaldo de Silla Fresia

#### Paso 1
##### Exportar respaldo

En primer lugar, habiendo exportado la silla Fresia, debemos generar un nuevo documento en Fusion, pero solo del respaldo.

![paso1.1](/img/mec2.5proceso/paso1.1.jpg)

##### Posición del respaldo

Luego de haber exportado el respaldo, buscamos ubicarlo lo más cercano al orgien, para esto empleamos el comando **Align** para que quede de manera ortogonal con respecto a los ejes del software. A continuación, generamos un *Sketch* en torno al respaldo, de manera que el rectángulo que dibujemos esté por afuera del respaldo y con espacio de sobra. 

![paso1.2](/img/mec2.5proceso/paso1.2.jpg)

![paso1.3](/img/mec2.5proceso/paso1.3.jpg)

![paso1.4](/img/mec2.5proceso/paso1.4.jpg)


#### Paso 2
##### Extruir 

Luego que tenemos el rectángulo que es más amplio que el área del respaldo, con el comando **Extrude** extruímos el rectángulo de manera que sobrepase el respaldo en su altura. 

![paso2.1](/img/mec2.5proceso/paso2.1.jpg)

![paso2.2](/img/mec2.5proceso/paso2.2.jpg)

Bajamos la opacidad para poder divisar bien el trabajo a realizar, a un 20%. 

![paso2.3](/img/mec2.5proceso/paso2.3.jpg)

![paso2.4](/img/mec2.5proceso/paso2.4.jpg)


 
#### Paso 3
##### Modo Fabricación 

![paso3.1](/img/mec2.5proceso/paso3.1.jpg)

Una vez que seleccionamos el modo fabricación o manufactura, tenemos que elegir la máquina a usar, por lo que seleccionamos la misma que habíamos empleado en el tutorial anterior "Autodesk Generic 3-axis". 

![paso3.2](/img/mec2.5proceso/paso3.2.jpg)

En el material, en el modo, buscamos desde un sólido, que vendría siendo el respaldo. Y el orientación, seleccionamos "eje o plano Z y eje X" 

![paso3.3](/img/mec2.5proceso/paso3.3.jpg)

![paso3.4](/img/mec2.5proceso/paso3.4.jpg)

Luego, en máquina configuramos el sistema de coordenadas que dan origen desde el rectángulo extruido. luego en modelo seleccionamos el cuerpo (repaldo).  

![paso3.5](/img/mec2.5proceso/paso3.5.jpg)

![paso3.6](/img/mec2.5proceso/paso3.6.jpg)



#### Paso 4
##### Modo Diseño 

Ahora pasamos al modo diseño, generamos un nuevo sketch sobre el respaldo (sbre el stock)  

![paso4.1](/img/mec2.5proceso/paso4.1.jpg)

![paso4.2](/img/mec2.5proceso/paso4.2.jpg)

![paso4.3](/img/mec2.5proceso/paso4.3.jpg)

Seleccionamos el modo manufactura 

![paso4.4](/img/mec2.5proceso/paso4.4.jpg)

Buscamos la limpieza adaptativa 
![paso4.5](/img/mec2.5proceso/paso4.5.jpg)

Configuramos 
![paso4.6](/img/mec2.5proceso/paso4.6.jpg)

El contorno de material, será una selección, es decir, la cadena que se generó en el paso anterior, las líneas moradas. 
![paso4.7](/img/mec2.5proceso/paso4.7.jpg)

![paso4.8](/img/mec2.5proceso/paso4.8.jpg)

![paso4.9](/img/mec2.5proceso/paso4.9.jpg)


#### Paso 5
##### Modo Fabricación 

Configuramos la carga óptima de la máquina seleccionada, de 6mm a 3mm. 

![paso5.1](/img/mec2.5proceso/paso5.1.jpg)

Trayectoría formada:

![paso5.2](/img/mec2.5proceso/paso5.2.jpg)

![paso5.3](/img/mec2.5proceso/paso5.3.jpg)

**Luego de que está lista la función, y se formó la trayectoria por capas y líneas (la fresa lo hace) con una altura especifica. En mi caso la fresa entró haciendo una elipse o espiral desde una de las *esquinas* y no desde el centro del material. A diferencia del tutorial, que entra desde el centro.**


#### Paso 6

Ahora vamos a hacer una terminación paralela **parallel finishing** usando la misma fresa anterior y en geometría, seleccionaomos en *machine boundarie* el área máxima en donde se mueve la fresa, en modelo seleccionamos el respaldo. Recordar que en la sección *model* no se debe hacer click en el “include setup model”.

![paso6.1](/img/mec2.5proceso/paso6.1.jpg)

En  modelo seleccionamos el respaldo:
![paso6.2](/img/mec2.5proceso/paso6.2.jpg)

Resultado:
![paso6.3](/img/mec2.5proceso/paso6.3.jpg)

Luego debemos hacer la ternminacion paralela en en sentido perpendicular.

Para eso duplicaremos la terminación paralela recién hecha.
![paso6.4](/img/mec2.5proceso/paso6.4.jpg)

Configuramos el ángulo **Pass Direction** a 90 grados y el **Stepover** debe quedar en 2mm.
![paso6.5](/img/mec2.5proceso/paso6.5.jpg)

Resultado:
![paso6.6](/img/mec2.5proceso/paso6.6.jpg)

Vamos a **Tool Library** y configuramos la herramienta en uso, ya que esta generaba tope (zonas rojas) en los primeros intentos:


![paso6.7](/img/mec2.5proceso/paso6.7.jpg)

Para esto, en **cutter** modificamos el largo bajo el tope que tiene la herramienta, lo dejamos en 40mm (en mi caso tuve que dejarlo en 50mm para un correcto funcionamiento).

![paso6.8](/img/mec2.5proceso/paso6.8.jpg)


Luego, cambiamos todas las fresas en los procesos que nos indique en rojo.

![paso6.9](/img/mec2.5proceso/paso6.9.jpg)



#### Resultado de las trayectorias: 

![paso7](/img/mec2.5proceso/paso7.jpg)

#### Video del proceso 



{{< video-local src="videotrayectoriafinal.mp4" >}}


## Iframe Silla y Respaldo

A continuación se presentan las imágenes editadas con Adobe Illustrator para este ejercicio, en formato planimetría.

{{< gallery dir="/img/planenc2/" />}} {{< load-photoswipe >}} 

---
Silla

{{< iframe-fusion link="https://alumnos4792.autodesk360.com/shares/public/SH56a43QTfd62c1cd96868ff56253a97ff74?mode=embed" >}}

Respaldo 

{{< iframe-fusion link="https://alumnos4792.autodesk360.com/shares/public/SH56a43QTfd62c1cd968343f21cfeb6dba47?mode=embed" >}}



---

### Galería del proceso de manera real, que van de la mano con los procesos llevados a cabo

{{< gallery dir="/img/mec2.5real/" />}} {{< load-photoswipe >}}



---



[[Volver Arriba]](#top)