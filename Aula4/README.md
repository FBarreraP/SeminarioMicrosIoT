<h1>Aula 4</h1>

Esta clase consiste en entender la comunicación serial UART.

<h2>Comunicación UART</h2>

La comunicación serial (simplex, half o full duplex) permite transmitir y/o recibir datos bit a bit, punto a punto (microcontroladores, PC, sistema embebido) de forma asíncrona (UART) o síncrona (USART). 

![Comunicaciones](image.png)

Fuente: http://tutosrafaz.blogspot.com/2015/06/comunicacion-serial-rs232-pic16f887a.html

<h3>Tipos de comunicación serial</h3>

El modo simplex

![alt text](image-2.png)

El modo half duplex

![Half Duplex](image-3.png)

El modo full duplex

![Full Duplex](image-4.png)

<h3>Trama de comunicación UART</h3>

RS232 y RS485 son dos comunicaciones seriales de tipo asíncrona (UART), las cuales tienen el estándar de transmisión serie que define la trama más conocida como 8N1 (8 bits de datos, Ninguno de paridad y 1 bit de stop).

![Ejemplo](image-5.png)

Fuente: https://github.com/Obijuan/open-fpga-verilog-tutorial/wiki/Cap%C3%ADtulo-21:-Baudios-y-transmisi%C3%B3n

![Trama UART](image-1.png)

Fuente: https://github.com/Obijuan/open-fpga-verilog-tutorial/wiki/Cap%C3%ADtulo-21:-Baudios-y-transmisi%C3%B3n

$$T_b=\frac{1}{V_t}$$

$$T_b=\frac{1}{9600 bits/s}$$

$$T_b=104.167 \mu s$$

<h3>FTDI</h3>

El conversor de USB a TTL (FTDI), puede alimentar +5V del PIC puede conectarse a una fuente externa o a los +5V del FTDI

![FTDI](image-6.png)

https://deepbluembedded.com/usb-ttl-converter-tutorial-pc-control-for-microcontrollers/

<h3>HC-05</h3>

![alt text](image-7.png)

https://deepbluembedded.com/usb-ttl-converter-tutorial-pc-control-for-microcontrollers/

<h3>Comunicación UART en el PIC 18F45K22</h3>

Es un protocolo de comunicación que consiste en una salida y una entrada de datos, TX (Transmisión) y RX (Recepción), respectivamente. El PIC 18F45K22 tiene dos canales de comunicación EUSART. TXREGx y RCREGx son registros del modulo EUSART del PIC 18F45K22 para cargar el byte a transmitir y para guardar el byte recibido, respectivamente.

![Pines UART PIC](image-8.png)

Para configurar la comunicación serial en el PIC18F45K22 es necesario tener en cuenta los siguientes pasos:

1. Configurar el pin RXx como entrada en el puerto C o D
2. Configurar el pin TXx como salida en el puerto C o D
3. Inicializar el valor de la velocidad de transmisión (baudios) a través del registro SPBRGx.
4. Configurar el registro de recepción (RCSTAx).
5. Configurar el registro de transmisión (TXSTAx).

