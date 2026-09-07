# Plantify

## Maceta Inteligente — Monitor Ambiental de Salud

**Hunter Electronics · 2026**

---

## ¿Qué es Plantify?

Plantify es un dispositivo de **monitoreo ambiental preventivo** integrado en una maceta inteligente, desarrollado sobre la plataforma **ESP32**. El sistema monitorea de forma continua las condiciones del ambiente interior donde vive el usuario, utilizando sensores ambientales para detectar situaciones que pueden afectar el confort y el bienestar.

La planta no es el producto final, sino el elemento físico que integra el sistema dentro del hogar. Mientras contribuye al ambiente mediante su proceso natural de intercambio gaseoso, el **ESP32** procesa los datos obtenidos por los sensores y genera alertas mediante un **semáforo LED RGB, una pantalla OLED, un buzzer y notificaciones push a través de la aplicación Blynk**.

El sistema busca facilitar la identificación de condiciones ambientales desfavorables y permitir que el usuario pueda tomar medidas preventivas, como ventilar el ambiente o corregir condiciones de humedad y temperatura.

> **"Tu planta cuida tu salud"**

---

## 🏥 Relación con la salud

La calidad del ambiente interior puede influir en el confort, el descanso y el bienestar de las personas. Factores como la **temperatura, la humedad y la calidad del aire** deben mantenerse dentro de niveles adecuados para evitar condiciones ambientales desfavorables.

Plantify utiliza el **BME680**, un sensor ambiental integrado capaz de medir **temperatura, humedad relativa, presión atmosférica y resistencia del gas**, permitiendo obtener información relacionada con la calidad del aire. Además, incorpora un **LDR** para medir la iluminación ambiental y un sensor de humedad del suelo para controlar las condiciones del sustrato de la planta.

| Sensor              | Variable                   | Rango/condición objetivo                 | Efecto o acción preventiva                                                          |
| ------------------- | -------------------------- | ---------------------------------------- | ----------------------------------------------------------------------------------- |
| **BME680**          | Temperatura                | 18 – 26 °C                               | Detectar condiciones térmicas desfavorables                                         |
| **BME680**          | Humedad relativa           | 40 – 60 %                                | Reducir condiciones que favorezcan sequedad, condensación o proliferación de hongos |
| **BME680**          | Calidad del aire (VOC/gas) | Según medición y línea base del ambiente | Detectar cambios en la calidad del aire y recomendar ventilación                    |
| **BME680**          | Presión atmosférica        | Monitoreo continuo                       | Registrar cambios en las condiciones ambientales                                    |
| **LDR**             | Luz ambiental              | Nivel adecuado durante el día            | Controlar las condiciones de iluminación de la planta                               |
| **Sensor de suelo** | Humedad del sustrato       | 40 – 60 %                                | Evitar falta o exceso de agua en la planta                                          |

> **Nota:** El BME680 no mide directamente CO₂ en ppm. Su medición de gases se utiliza para estimar cambios en la calidad del aire mediante VOC y resistencia del gas. Por este motivo, Plantify no debe presentar la lectura del BME680 como una medición directa de CO₂.

---

## ⚙️ Funcionamiento del sistema

El funcionamiento general de Plantify se basa en la siguiente secuencia:

1. Los sensores recopilan información del ambiente y del sustrato.
2. El **ESP32** recibe y procesa los datos.
3. El sistema compara las mediciones con los valores de referencia establecidos.
4. El **LED RGB** indica visualmente el estado ambiental.
5. La **pantalla OLED** muestra los valores medidos.
6. El **buzzer** genera una alerta cuando se detecta una condición desfavorable.
7. La aplicación **Blynk** permite visualizar los datos y recibir notificaciones.
8. El sensor de humedad del suelo permite controlar el estado de la planta y determinar cuándo necesita riego.

---

## 🔧 Componentes principales

* **ESP32 DevKitC**
* **BME680**
* **LDR**
* **Sensor de humedad del suelo**
* **Pantalla OLED**
* **LED RGB**
* **Buzzer**
* **Bomba de agua**
* **Módulo relé**
* **Maceta y planta**
* Fuente de alimentación

---

## 📱 Aplicación Blynk

Plantify utiliza **Blynk** como interfaz de monitoreo remoto. Desde la aplicación, el usuario puede consultar los valores registrados por el sistema y recibir notificaciones cuando se detecten condiciones ambientales que requieran atención.

Entre los datos que pueden visualizarse se encuentran:

* Temperatura.
* Humedad relativa.
* Calidad relativa del aire mediante VOC/gas.
* Presión atmosférica.
* Nivel de iluminación.
* Humedad del suelo.
* Estado general del ambiente.

---

## 🌱 Objetivo

El objetivo principal de Plantify es desarrollar una solución tecnológica capaz de **monitorear las condiciones ambientales de un espacio interior y proporcionar información preventiva al usuario**, integrando electrónica, programación, sensores IoT y una interfaz móvil en un único dispositivo.

---

## 👥 Integrantes

**Jeronimo Capozzolo**
**Valentino Castaldo**
**Joaquin Bargach**
**Dylan Dragneff**

**7°6° · 2026**

**Hunter Electronics**
