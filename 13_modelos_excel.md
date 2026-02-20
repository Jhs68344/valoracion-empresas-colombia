# Modelos de Valoración en Excel (Plantilla Profesional)

## 1. Introducción

Excel es una de las herramientas más utilizadas en Colombia para construir modelos financieros y realizar valoraciones empresariales, especialmente en:

- Pymes
- Empresas familiares
- Consultoría financiera
- Banca y análisis corporativo

Este documento presenta una estructura estándar para construir un modelo de valoración por Flujo de Caja Descontado (DCF) en Excel.

---

## 2. Estructura recomendada del archivo Excel

Un modelo profesional debe tener hojas separadas y ordenadas:

1. **Inputs (Supuestos)**
2. **Estados Proyectados**
3. **Cálculo del Flujo de Caja Libre (FCL)**
4. **WACC (Tasa de descuento)**
5. **Valoración DCF**
6. **Sensibilidad**
7. **Resumen / Dashboard**

Esto mejora claridad, auditoría y presentación ante inversionistas.

---

## 3. Hoja 1: Inputs (Supuestos)

En esta hoja se deben ingresar los supuestos del modelo:

### Supuestos operativos
- Crecimiento de ventas (%)
- Margen bruto (%)
- Gastos operativos (%)
- Depreciación (% o valor)

### Supuestos de inversión
- CAPEX proyectado
- Variación de capital de trabajo

### Supuestos financieros
- Tasa de impuesto
- WACC o componentes del WACC
- Crecimiento perpetuo (g)

> Recomendación: colocar todos los supuestos en una zona clara y usar nombres definidos o celdas referenciadas.

---

## 4. Hoja 2: Estados proyectados

El modelo debe proyectar al menos 5 años:

- Ventas
- Costos
- EBITDA
- Depreciación
- EBIT
- Impuestos
- Utilidad operativa

La proyección debe estar conectada a los supuestos (inputs).

---

## 5. Hoja 3: Flujo de Caja Libre (FCFF)

Estructura estándar del FCFF:

FCFF = EBIT(1−T)  
+ Depreciación  
− CAPEX  
− Δ Capital de trabajo

En Excel se recomienda:

- Mostrar cada componente por separado
- Usar signos claros (+ / -)
- Mantener consistencia en unidades (COP, millones COP, etc.)

---

## 6. Hoja 4: WACC

El WACC debe construirse con transparencia.

Componentes:

- E/V (peso patrimonio)
- D/V (peso deuda)
- Costo patrimonio (Re)
- Costo deuda (Rd)
- Impuesto corporativo

Fórmula:

WACC = (E/V)*Re + (D/V)*Rd*(1−T)

En Colombia es recomendable justificar:

- Prima de riesgo país
- Tasa libre de riesgo usada (TES o referencia internacional)
- Supuestos de beta

---

## 7. Hoja 5: Valoración DCF

### 7.1 Descuento de flujos

Para cada año:

VP_FCL_t = FCL_t / (1 + WACC)^t

Se suman todos los valores presentes.

### 7.2 Valor terminal

Método de crecimiento perpetuo:

VT = FCL_(n+1) / (WACC − g)

Luego se descuenta:

VP_VT = VT / (1 + WACC)^n

### 7.3 Valor Empresa

Valor Empresa = Σ VP_FCL + VP_VT

---

## 8. Hoja 6: Sensibilidad

Se recomienda crear una tabla de doble entrada con:

- WACC (filas)
- g (columnas)

Ejemplo de rangos:

WACC: 10% a 16%  
g: 2% a 6%

Esto permite ver qué tan sensible es el valor ante cambios pequeños.

---

## 9. Hoja 7: Resumen / Dashboard

Debe mostrar:

- Valor empresa estimado
- Valor terminal
- Participación del valor terminal (%)
- Supuestos principales (WACC, g, años)
- Observaciones clave

El dashboard debe ser visualmente limpio y profesional.

---

## 10. Buenas prácticas en Excel

- Evitar escribir números “a mano” en fórmulas (usar inputs).
- Usar colores para diferenciar inputs vs cálculos.
- Documentar supuestos.
- Validar que el modelo sea consistente (auditoría).
- Mantener unidades claras (COP, millones, miles).

---

## 11. Conclusión

Un modelo DCF en Excel debe ser:

- Ordenado
- Auditable
- Transparente
- Con supuestos justificados (especialmente en Colombia)

Esta estructura es la base para construir valoraciones profesionales que puedan presentarse ante socios, bancos o inversionistas.

