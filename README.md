# Laboratorio-OLED-I2C
# Laboratorio de Comunicación I2C con Pantalla OLED

## Descripción del proyecto

Este repositorio contiene el desarrollo del laboratorio de comunicación I2C con una pantalla OLED. El proyecto tiene como propósito estudiar el funcionamiento de esta interfaz de comunicación serial, implementar el control de una pantalla OLED mediante código en Python y analizar las señales generadas durante las diferentes operaciones realizadas.

Para el desarrollo de la práctica se empleó el software Saleae Logic, con el cual se capturaron y analizaron las señales de comunicación. Las capturas permiten observar las transacciones realizadas durante las pruebas de encendido, apagado, limpieza de pantalla, ajuste de contraste, animación, visualización de texto y envío de comandos y datos RAW.

El repositorio reúne el código fuente, los archivos de captura del analizador lógico y la documentación correspondiente al laboratorio, facilitando la consulta, reproducción y análisis de las pruebas.

## Objetivo general

Implementar y analizar la comunicación entre un sistema de control y una pantalla OLED mediante el protocolo I2C, verificando las operaciones realizadas a través de la captura e interpretación de las señales con un analizador lógico.

## Objetivos específicos

- Comprender el funcionamiento de la comunicación serial I2C y sus señales principales.
- Implementar el control de una pantalla OLED mediante un programa desarrollado en Python.
- Realizar diferentes operaciones sobre la pantalla, como encendido, apagado, limpieza, visualización de texto y animación.
- Capturar las señales de comunicación mediante Saleae Logic.
- Examinar las transacciones correspondientes al envío de comandos y datos.
- Documentar los procedimientos y resultados obtenidos durante el laboratorio.

## Materiales y herramientas

- Pantalla OLED.
- Sistema de control y conexión de comunicación I2C.
- Computador con Python.
- Analizador lógico y software Saleae Logic.
- Código fuente y documentación de la práctica.

## Desarrollo del laboratorio

Durante el laboratorio se realizaron diferentes pruebas para verificar el funcionamiento de la pantalla OLED y estudiar las señales de comunicación.

Las pruebas documentadas incluyen:

1. Encendido y apagado de la pantalla.
2. Limpieza de la pantalla.
3. Ajuste de contraste.
4. Visualización de texto de demostración.
5. Ejecución de animaciones.
6. Envío de comandos RAW.
7. Envío de datos RAW.
8. Pruebas de inversión con los valores 0 y 1.
9. Pruebas correspondientes a los puntos 1, 2 y 3.
10. Análisis de frecuencia de las señales.

Las capturas obtenidas con Saleae Logic se almacenan en el repositorio para facilitar su revisión y comparación.

## Estructura del repositorio

```text
Laboratorio-OLED-I2C/
├── README.md
├── codigo/
│   └── CODIGO_OLED.py
├── capturas_saleae/
│   ├── ANIMACION.sal
│   ├── APAGAR.sal
│   ├── COMANDO RAW.sal
│   ├── CONTRASTE.sal
│   ├── ENCENDER.sal
│   ├── ENVIAR RAW.sal
│   ├── FRECUENCIA.sal
│   ├── INVERTIR 0.sal
│   ├── INVERTIR 1.sal
│   ├── LIMPIAR.sal
│   ├── PUNTO 1.sal
│   ├── PUNTO 2.sal
│   ├── PUNTO 3.sal
│   └── TEXTO DEMO.sal
└── documentacion/
    ├── I2C_lab.docx
    └── I2C_Informe.docx
```

## Tecnologías y herramientas

- **Python:** desarrollo del programa de control de la pantalla OLED.
- **Protocolo I2C:** comunicación serial entre el sistema de control y el dispositivo.
- **Saleae Logic:** captura y análisis de señales digitales.
- **Git y GitHub:** control de versiones y almacenamiento del proyecto.

## Integrantes

- **Ediem Valero**
- **Paula Quintero**

## Documentación

En la carpeta `documentacion/` se encuentran la guía del laboratorio y el informe desarrollado. En `capturas_saleae/` se almacenan las sesiones de análisis lógico, mientras que el código de Python se encuentra en `codigo/`.

## Resultados

Los archivos de captura permiten consultar las señales obtenidas durante las distintas operaciones realizadas sobre la pantalla OLED. El informe del laboratorio contiene el desarrollo de la práctica y el análisis de los resultados.

## Licencia

Este proyecto se publica con fines académicos. El código y los documentos se comparten como parte del desarrollo del laboratorio.
