# Caso Aplicado: Empresa Colombiana (DCF Completo)

## 1. Descripción de la Empresa

Empresa: Alimentos Andinos S.A.S.  
Sector: Consumo masivo  
Ubicación: Bogotá, Colombia  
Ingresos actuales: $15.000 millones COP  
Crecimiento histórico promedio: 6%

La empresa busca determinar su valor empresarial para una posible venta parcial a un inversionista estratégico.

---

## 2. Supuestos del Modelo

- Crecimiento anual proyectado: 6%
- Margen EBITDA: 18%
- CAPEX: 5% de ventas
- Tasa de impuesto: 35%
- WACC estimado: 14%
- Crecimiento perpetuo (g): 4%
- Horizonte de proyección: 5 años

---

## 3. Proyección de Flujo de Caja Libre

Se proyectan los siguientes flujos (millones COP):

Año 1: 1.200  
Año 2: 1.350  
Año 3: 1.500  
Año 4: 1.650  
Año 5: 1.800  

---

## 4. Aplicación del Modelo DCF en Python

```python
import numpy as np

flujos = np.array([1200, 1350, 1500, 1650, 1800])
wacc = 0.14
g = 0.04

años = np.arange(1, len(flujos) + 1)
valor_presente_flujos = flujos / (1 + wacc) ** años
valor_total_flujos = np.sum(valor_presente_flujos)

valor_terminal = (flujos[-1] * (1 + g)) / (wacc - g)
valor_presente_terminal = valor_terminal / (1 + wacc) ** len(flujos)

valor_empresa = valor_total_flujos + valor_presente_terminal

print("Valor estimado de la empresa:", round(valor_empresa, 2))

