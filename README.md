# Laboratorio-OLED-I2C


## Descripción del proyecto

Este repositorio contiene el desarrollo del laboratorio de comunicación serial I2C entre un microcontrolador Raspberry Pi Pico y una pantalla OLED basada en el controlador SSD1306. El proyecto se realizó utilizando MicroPython y el entorno de desarrollo Thonny, con el propósito de implementar la comunicación, controlar las funciones de la pantalla y analizar las tramas transmitidas mediante un analizador lógico.

Durante la práctica se utilizó el software Logic 2 para observar y decodificar las señales de reloj (SCL) y datos (SDA), identificar la dirección del dispositivo, reconocer las respuestas ACK y NACK y analizar los códigos hexadecimales enviados a la pantalla.

## Objetivos

### Objetivo general
Implementar y analizar la comunicación I2C entre un Raspberry Pi Pico y una pantalla OLED SSD1306, verificando el intercambio de información mediante un analizador lógico.

### Objetivos específicos
- Identificar los elementos que componen una trama I2C.
- Reconocer las condiciones START y STOP, la dirección del dispositivo, el bit de lectura/escritura y las respuestas ACK y NACK.
- Realizar pruebas con direcciones válidas e incorrectas.
- Identificar la dirección I2C de la pantalla OLED.
- Analizar los comandos hexadecimales utilizados para controlar la pantalla.
- Observar las señales SCL y SDA mediante Logic 2.

## Componentes y herramientas

### Hardware
- Raspberry Pi Pico.
- Pantalla OLED SSD1306.
- Protoboard y cables de conexión.
- Analizador lógico.
- Computador.

### Software
- MicroPython.
- Thonny IDE.
- Logic 2.

## Conexiones

La pantalla OLED se conecta al microcontrolador mediante las líneas de alimentación y las señales del bus I2C.

| Pantalla OLED | Raspberry Pi Pico | Función |
|---|---|---|
| VCC | 3V3(OUT) | Alimentación |
| GND | GND | Tierra |
| SDA | GP14 | Datos I2C |
| SCL | GP15 | Reloj I2C |

Para el análisis lógico, el canal CH0 se conecta a SCL (GP15), el canal CH1 a SDA (GP14) y GND del analizador a la tierra común del circuito.

## Desarrollo del laboratorio

### Parte 1. Análisis de tramas I2C y pruebas ACK-NACK

Se estudió la estructura de las tramas I2C mediante las señales capturadas en Logic 2. Se identificaron los campos de dirección, escritura, datos y reconocimiento.

Se realizaron las siguientes pruebas:

1. **ACK esperado:** envío de una dirección válida para comprobar el reconocimiento del dispositivo.
2. **Dirección incorrecta:** envío de una dirección diferente para observar la respuesta NACK.
3. **Comparación:** análisis de las diferencias entre las dos respuestas.

### Parte 2. Identificación de la dirección y análisis de códigos hexadecimales

Se ejecutó un escaneo del bus I2C mediante MicroPython para encontrar la dirección de la pantalla OLED. La dirección detectada fue **0x3C**.

Posteriormente, se analizaron diferentes instrucciones para controlar el SSD1306:

| Función | Código hexadecimal |
|---|---|
| Apagar pantalla | 0xAE |
| Encender pantalla | 0xAF |
| Configurar contraste | 0x81 |
| Invertir visualización | 0xA7 |
| Visualización normal | 0xA6 |
| Enviar datos gráficos | 0x40 |

También se realizaron pruebas de limpieza de pantalla, visualización de texto y ejecución de una animación breve.

## Resultados

Las capturas obtenidas con Logic 2 permitieron observar el intercambio de información entre el microcontrolador y la pantalla OLED. Se identificó la dirección I2C 0x3C y se verificó la respuesta ACK durante las comunicaciones reconocidas.

La prueba con una dirección incorrecta permitió observar una respuesta NACK. Asimismo, se identificaron los comandos utilizados para encender, apagar, modificar el contraste e invertir la visualización de la pantalla.

Las pruebas de texto, limpieza y animación permitieron observar la transmisión de múltiples bytes de datos gráficos hacia el controlador SSD1306.

## Estructura del repositorio

La organización del repositorio puede incluir los siguientes elementos:

- **Código:** programas desarrollados en MicroPython.
- **Capturas:** imágenes de Logic 2 y evidencias de las pruebas.
- **Informe:** documento con el procedimiento, análisis de resultados y conclusiones.
- **README.md:** descripción general del proyecto.

## Integrantes

- **Ediem Valero**
- **Paula Quintero**

## Referencias

1. NXP Semiconductors, *UM10204 I2C-bus specification and user manual*.
2. HeTPro, “I2C – Puerto, introducción, trama y protocolo.” https://hetpro-store.com/TUTORIALES/i2c/
3. Wray Castle, “SDA and SCL.” https://wraycastle.com/es/blogs/knowledge-base/sda-and-scl
4. Digital Samba, “What are ACK and NACK?” https://www.digitalsamba.com/es/blog/what-are-ack-and-nack
5. Programar Fácil, “SSD1306: Pantalla OLED con Arduino.” https://programarfacil.com/blog/arduino-blog/ssd1306-pantalla-oled-con-arduino/
6. ITP Physical Computing, “Lab: OLED Screen Display using I2C.” https://itp.nyu.edu/physcomp/lab-oled-screen-display-using-i2c/
7. Tektronix, “Logic Analyzer Fundamentals.” https://www.tek.com/en/documents/primer/logic-analyzer-fundamentals

---

**Proyecto académico — Comunicación I2C con pantalla OLED SSD1306**
