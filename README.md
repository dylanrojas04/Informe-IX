# 📡 Análisis de Modulación Digital y Codificación de Canal usando Simulink

### Universidad Militar Nueva Granada  
**Facultad de Ingeniería – Ingeniería en Telecomunicaciones**

---

## 🧠 Descripción del Proyecto

Este proyecto tiene como objetivo analizar y comparar el desempeño de distintas técnicas de **modulación digital** y **codificación de canal** utilizando **Simulink (MATLAB)** como entorno de simulación.  
Se implementaron las modulaciones **BPSK** y **16-QAM**, evaluando sus **tasas de error de bit (BER)** bajo un canal **AWGN** y aplicando **códigos de Hamming** y **codificación convolucional** con **decodificación Viterbi**.

El trabajo forma parte del laboratorio de **Comunicaciones Digitales**, en el marco del estudio de los efectos del ruido y las técnicas de corrección de errores sobre sistemas digitales.

---

## ⚙️ Contenido del Repositorio

| Archivo | Descripción |
|----------|--------------|
| `Simulink.xlsx` | Resultados experimentales obtenidos de las simulaciones (SNR, BER, Errores, Símbolos). |
| `Guia_simulink_comdigital.pdf` | Documento guía original con la metodología y parámetros de simulación. |
| `BPSK_model.png` | Diagrama de Simulink del sistema BPSK con y sin codificación Hamming. |
| `README.md` | Este archivo, con la descripción y documentación del proyecto. |

---

## 🧩 Metodología

El desarrollo se realizó en **Simulink**, empleando los siguientes bloques principales:

- **Bernoulli Binary Generator** – Genera secuencias binarias aleatorias.  
- **Moduladores BPSK / 16-QAM** – Convierte los datos digitales en señales moduladas.  
- **AWGN Channel** – Simula el canal con ruido blanco gaussiano aditivo.  
- **Codificadores Hamming / Convolucional** – Aplican redundancia para corrección de errores.  
- **Demoduladores y Decodificadores** – Recuperan la información transmitida.  
- **Error Rate Calculation** – Calcula la tasa de error de bit (**BER**) y los errores totales.  

Se ejecutaron simulaciones variando el **SNR (dB)** desde –40 hasta +10, analizando el comportamiento de la **BER** para cada esquema de modulación con y sin codificación.

---

## 📊 Resultados

### 🔹 Modulación BPSK
- Sin codificación: mayor BER en bajos SNR.  
- Con codificación Hamming: reducción significativa de errores y mejora promedio de **2 dB** en ganancia de codificación.

### 🔹 Modulación 16-QAM
- Sin codificación: alta sensibilidad al ruido debido a la complejidad de la constelación.  
- Con codificación convolucional: notable reducción de BER a SNR bajos, con ganancia promedio de **3 dB**.

Las curvas **BER vs SNR** demostraron el impacto positivo de las técnicas de codificación sobre la confiabilidad de la transmisión.

---

## 🧮 Ganancia de Codificación

La ganancia de codificación (**Gc**) se calculó como:

\[
G_c = SNR_{sin\_cod} - SNR_{con\_cod}

