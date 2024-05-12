<h1>Aula 2</h1>

Esta clase consiste en realizar una introducción al PIC 18F45K22, estudiando los recursos con los que cuenta este microcontrolador.

<h2>PIC 18F45K22</h2>

El PIC 18F45k22 es un microcontrolador PIC (Peripheral Interface Controller) de 40 pines de la familia de 8 bits de Microchip. La CPU es de tipo RISC, el cual ofrece alta velocidad de procesamiento mayor a 10 MIPs (64MHz).

![Características PIC 18F45K22](image.png)

Fuente: Datasheet PIC 18F45K22

![Características PIC 18F45K22](image-1.png)

Fuente: Datasheet PIC 18F45K22

![PIC 18F45K22](image-2.png)

Fuente: Datasheet PIC 18F45K22 y Proteus

Puertos digitales y análogos:
- 5 puertos digitales (A, B, C, D y E)
- 28 canales análogos

Alimentación:
- 2 pines de Vdd (+5V) 
- 2 pines de Vss (0V) 

Periféricos:

- 3 pines externos para interrupciones
- 4 interrupciones por teclado (detección de los dos flancos)
- 28 canales para conversión A/D a 10 bits 
- 2 USART (comunicación serial - Rx y Tx) 
- 2 MSSP (master synchronous serial port) para SPI e I2C *
- 7 timers (4 de 16 bits y 3 de 8 bits)
- 5 modulos de PWM*

Frecuencia de oscilación:
- 2 pines de Clock 

![Clock externo](image-3.png)

Fuente: Datasheet PIC 18F45K22

<h3>OSCCON</h3>

Es un registro que permite configurar la fuente de oscilador del PIC 18F45K22.

![OSCCON](image-4.png)

![OSCCON bits](image-5.png)

* El oscilador secundario es un cristal externo de baja potencia (32 kHz a 100 kHz) 
* El reloj primario son osciladores externos, resonadores de cristal de cuarzo, resonadores cerámicos y circuitos Resistencia-Capacitor (RC).

<h3>ANSEL, TRIS, LAT y PORT</h3>

Son registros internos de los microcontroladores, con los cuales cada puerto puede ser configurado de diferente forma, deseando el tipo de conexión (entrada o salida). Por tanto, cada puerto tiene tres registros para su operación, TRIS (1=entrada / 0=salida), LAT y PORT; sin embargo, se debe configurar inicialmente el registro ANSEL, que es el que controla los pines como análogos (1) o digitales (0).

![TRIS, LAT y PORT](image-6.png)

<h2>PIC Kit v3.0</h2>

El PIC Kit v3.0 es un hardware que permite programar los microcontroladores de Microchip. Además, entre sus funciones está la depuración (debugging) del código.

![PIC Kit v3.0](image-7.png)

Fuente: Datasheet PIC Kit 3.0

![Conexiones PIC y PIC Kit v3.0](image-8.png)

Fuente: Datasheet PIC Kit 3.0






