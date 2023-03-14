# W5100S-EVB-Pico

![download](https://user-images.githubusercontent.com/60374861/224969947-e1d869c5-703a-43d3-8955-cc515909a129.png)


## W5100S-EVB-Pico

W5100S-EVB-Pico es una placa de evaluación de microcontroladores basada en Raspberry Pi RP2040 y un controlador TCP/IP totalmente cableado W5100S, y básicamente funciona igual que la placa Raspberry Pi Pico pero con Ethernet adicional a través de W5100S.

- Raspberry Pi Pico Clone
- Ethernet (W5100S Hardwired TCP/IP CHIP)
- AWS IoT Core Qualified
- Microsoft Azure Device Certified

## Características

- Microcontrolador RP2040 con 2MByte Flash
  - Cortex M0+ de doble núcleo a hasta 133 MHz
  - SRAM multibanco de alto rendimiento de 264kByte
  - Flash Quad-SPI externo con eXecute In Place (XIP)
  - Tejido de autobús de barra transversal completa de alto rendimiento
  - 30 E/S multifunción de propósito general (4 se pueden usar para ADC)
    - Voltaje de E/S de 1,8 a 3,3 V (NOTA: el voltaje de E/S de Pico se fija en 3,3 V)
  - Convertidor analógico a digital (ADC) de 12 bits y 500 ksps
  - Varios periféricos digitales
    - 2 × UART, 2 × I2C, 2 × SPI, 16 × canales PWM
    - 1 × temporizador con 4 alarmas, 1 × contador en tiempo real
  - 2 bloques de E/S programable (PIO), 8 máquinas de estado en total
  - E/S de alta velocidad flexible y programable por el usuario
  - Puede emular interfaces como tarjeta SD y VGA
- Incluye W5100S
  - Admite protocolos de Internet cableados: TCP, UDP, WOL sobre UDP, ICMP, IGMPv1/v2, IPv4, ARP, PPPoE
  - Admite 4 SOCKET de hardware independientes simultáneamente
  - Memoria interna de 16 Kbytes para búferes TX/ RX
  - Interfaz SPI
- Puerto Micro-USB B para alimentación y datos (y para reprogramar el Flash)
- PCB de 40 pines 21x51 estilo 'DIP' de 1 mm de grosor con pines de orificio pasante de 0,1" también con bordes almenados
- Puerto de depuración de cable serie (SWD) ARM de 3 pines
- 10/100 Ethernet PHY integrado
- Admite negociación automática
  - Dúplex completo / semidúplex
  - Basado en 10 / 100
- RJ45 incorporado (RB1-125BAG1A)
- LDO incorporado (LM8805SF5-33V)

## Especificaciones de Hardware

![w5100s-evb-pico-1 1-pinout-106c570db291aee2fa8b1e973d2ee535](https://user-images.githubusercontent.com/60374861/224967543-83620ff3-2304-4e76-9d1d-7ec80bceeb02.png)


El pinout W5100S-EVB-Pico está directamente conectado al GPIO de RP2040 como se muestra en la imagen de arriba. Tiene el mismo pinout que la placa Raspberry Pi Pico. Sin embargo, GPIO16, GPIO17, GPIO18, GPIO19, GPIO20, GPIO21 están conectados a W5100S dentro de la placa. Estos pines permiten la comunicación SPI con W5100S para usar la función Ethernet. Si está utilizando la función Ethernet, estos pines no se pueden utilizar para ningún otro propósito.


El GPIO RP2040 utilizado dentro de W5100S-EVB-Pico es el siguiente.

|I/O|Nombre del pin|Descripción|
|:----|:----|:----|
|I|GPIO16|Conectado a MISO en W5100S|
|O|GPIO17|Conectado a CSn en W5100S|
|O|GPIO18|Conectado a SCLK en W5100S|
|O|GPIO19|Conectado a MOSI en W5100S|
|O|GPIO20|Conectado a RSTn en W5100S|
|I|GPIO21|Conectado a INTn en W5100S|
|I|GPIO24|Detección de VBUS: alta si VBUS está presente, de lo contrario, baja|
|O|GPIO25|Conectado al usuario LED|
|I|GPIO29|Usado en modo ADC (ADC3) para medir VSYS/3|


## Condición de operación. 

|Artículo|Descripción|
|:----|:----|
|Temperatura de funcionamiento MÁX.|85C (incluido el autocalentamiento)|
|Temperatura de operación MÍN.|-20C|
|VBUS|5 V CC (+/- 10 %)|
|VSYS mín.|CC 4,3 V|
|VSYS máx.|CC 5,5 V|

