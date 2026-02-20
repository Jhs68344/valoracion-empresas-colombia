# Modelos de Valoración en Python

## 1. Introducción

Python se ha convertido en una herramienta clave en análisis financiero y valoración empresarial, especialmente en:

- Banca de inversión
- Fondos de capital privado
- Consultoría financiera avanzada
- Modelos cuantitativos

A diferencia de Excel, Python permite:

- Automatizar cálculos
- Ejecutar simulaciones masivas
- Integrar análisis estadístico
- Trabajar con grandes volúmenes de datos

Este documento muestra una estructura básica para construir un modelo DCF en Python.

---

## 2. Librerías necesarias

Para valoración financiera se pueden utilizar:

- numpy → Cálculos numéricos
- pandas → Manejo de datos
- matplotlib → Visualización
- scipy → Métodos numéricos

Instalación:

pip install numpy pandas matplotlib scipy

---

## 3. Cálculo básico del DCF en Python

### 3.1 Definir flujos proyectados

```python
import numpy as np

# Flujos de caja proyectados (millones COP)
flujos = np.array([200, 220, 250, 280, 300])

wacc = 0.12
g = 0.04

