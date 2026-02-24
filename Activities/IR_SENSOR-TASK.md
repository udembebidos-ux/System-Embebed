# ACTIVITY IR SENSOR

## FLOWCHART

# StWo Signal: Representación de Secuencia 0110 (Protocolo NEC)

En esta tarea se analiza la forma de onda física necesaria para transmitir la secuencia de bits `0110` utilizando el protocolo de infrarrojos NEC.

## 1. Especificaciones de Tiempos
El protocolo NEC utiliza codificación por distancia de pulsos basándose en una unidad de tiempo $T = 562.5\mu s$:

| Elemento | Duración Pulso (Mark) | Duración Espacio (Space) | Tiempo Total |
| :--- | :--- | :--- | :--- |
| **Header** | $9ms$ | $4.5ms$ | $13.5ms$ |
| **Lógico '0'** | $562.5\mu s$ ($1T$) | $562.5\mu s$ ($1T$) | $1.125ms$ |
| **Lógico '1'** | $562.5\mu s$ ($1T$) | $1.6875ms$ ($3T$) | $2.25ms$ |

## 2. Diagrama de la Señal (Visualización en GitHub)
A continuación se muestra la representación lógica de la ráfaga para los bits `0, 1, 1, 0`. Los bloques altos representan el envío de la portadora de 38kHz.

```mermaid
gantt
    title Señal IR NEC - Secuencia 0110
    dateFormat X
    axisFormat %s
    section Header
    Pulso 9ms (Mark)           :active, h1, 0, 90
    Espacio 4.5ms (Space)      :h2, 90, 135
    section Bits 0110
    Bit 0 - Mark               :active, b0m, 135, 141
    Bit 0 - Space              :b0s, 141, 147
    Bit 1 - Mark               :active, b1m, 147, 153
    Bit 1 - Space              :b1s, 153, 170
    Bit 1 - Mark               :active, b2m, 170, 176
    Bit 1 - Space              :b2s, 176, 193
    Bit 0 - Mark               :active, b3m, 193, 199
    Bit 0 - Space              :b3s, 199, 205
    Stop Bit                   :active, st, 205, 211
