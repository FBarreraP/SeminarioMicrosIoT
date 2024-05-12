<h1>Aula 3</h1>

Esta clase consiste en estudiar la pantalla GLCD (KS0108).

<h2>Pantalla GLCD</h2>

Las pantallas gráficas de cristal líquido (GLCD) son monocromáticas. Consumen poca energía eléctrica, siendo su principal ventaja. Así mismo, hay diferentes controladores, como el chip KS0108 de Samsung.

![GLCD](image.png)

<h2>GLCD 128x64</h2>

![GLCD 128x64](image-1.png)

Fuente: https://www.electronicwings.com/pic/glcd-128x64-interfacing-with-pic18f4550-microcontroller

![Pinout GLCD](image-3.png)

Fuente: Fuente: https://www.pjrc.com/teensy/td_libs_GLCD.html

![Especificación de pines GLCD](image-2.png)

![Conexiones PIC y GLCD](image-4.png)

![CS1 y CS2 GLCD](image-5.png)

Fuente: https://openlabpro.com/guide/ks0108-graphic-lcd-interfacing-with-pic18f4550-part-1/

![Direccionamiento GLCD](image-6.png)

Fuente: https://www.electronicwings.com/sensors-modules/glcd-128x64

![Ejemplo >](image-7.png)

Fuente: https://www.electronicwings.com/sensors-modules/glcd-128x64

![Ejemplo P](image-8.png)

<h3>Registros GLCD</h3>

![Registros GLCD](image-9.png)

```c
//GLCD
#define D 0x3F
#define SAy 0x40
#define SAx 0xB8
#define DSL 0xC0
```

<h3>Ejemplo 1</h3>

Utilizar una pantalla GLCD 128x64 para visualizar los ejemplos analizados anteriormente (> y P).

<h3>Ejemplo 2</h3>

Utilizar una pantalla GLCD 128x64 para escribir texto (palabras y números), teniendo en cuenta el software GLCDFastLcdFontCreator.jar el cual creará un vector de 1024 bytes.

![Texto GLCD](image-10.png)

<h3>Ejemplo 3</h3>

Utilizar una pantalla GLCD 128x64 para visualizar una imagen, utilizando el software Image2GLCD.

![Imagen GLCD](image-11.png)






