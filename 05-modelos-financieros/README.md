# 💰 MODELOS FINANCIEROS - Escenarios de Inversión

**Propósito:** Comparar 5 escenarios de inversión con proyecciones detalladas

**Cuándo usar:** Antes de decidir cuánto capital invertir en el negocio

---

## 📊 CONTENIDO (1 archivo principal)

### **escenarios-financieros.md** ⭐ (29KB, ~850 líneas)

**Para qué:** Análisis exhaustivo de 5 opciones de inversión para abrir el consultorio

**Lo que contiene:**
- **Escenario 1:** Domicilio Puro (Gs. 4.75M) - ROI 857%, riesgo muy bajo
- **Escenario 2:** Mixto San Lorenzo (Gs. 38.5M) - ROI 69%, riesgo bajo
- **Escenario 3:** Consultorio Mínimo (Gs. 35M) - ROI 84%, riesgo medio
- **Escenario 4:** Mixto Asunción (Gs. 55.4M) - ROI 37-61%, riesgo medio
- **Escenario 5:** Consultorio Premium (Gs. 75M) - ROI 24%, riesgo alto

**Nivel de detalle:**
- ✅ Inversión inicial desglosada (equipamiento, alquiler, mobiliario, etc.)
- ✅ Costos fijos mensuales
- ✅ Proyecciones mes a mes año 1
- ✅ Análisis sensibilidad (best case, worst case, conservative, optimistic)
- ✅ Break-even analysis
- ✅ ROI y payback period

---

## 🎯 CÓMO USAR ESTE DOCUMENTO

### **PASO 1: Lee el resumen ejecutivo primero**

Antes de sumergirte en 850 líneas, lee:
- `../referencias/00-resumen-ejecutivo.md` (5 páginas, 10 min)
- `../referencias/matriz-decision-escenarios.md` (1 página, 3 min)

Esos documentos te dan la **decisión** sin el detalle técnico.

---

### **PASO 2: Identifica tu rango de capital**

**¿Cuánto capital tienes disponible HOY?**

| Capital Disponible | Escenarios Viables | Recomendación |
|-------------------|-------------------|---------------|
| **< Gs. 10M** | Solo Escenario 1 | Domicilio Puro → Luego escala con ganancias |
| **Gs. 10-35M** | Escenarios 1, 2 | Mixto SL si vives en San Lorenzo |
| **Gs. 35-50M** | Escenarios 1, 2, 3 | Consultorio Mínimo viable |
| **Gs. 50-70M** | Escenarios 1-4 | **Mixto Asunción (4)** ⭐ Mejor relación riesgo/retorno |
| **> Gs. 70M** | Todos | Premium solo si tienes experiencia 2+ años |

---

### **PASO 3: Lee tu escenario en detalle**

Abre `escenarios-financieros.md` y navega a:
- **Escenario 1:** Línea 50
- **Escenario 2:** Línea 250
- **Escenario 3:** Línea 380
- **Escenario 4:** Línea 500
- **Escenario 5:** Línea 650

Lee solo TU escenario (no necesitas leer los 5).

---

### **PASO 4: Verifica los supuestos**

Cada escenario tiene supuestos clave:
- Precio por sesión (Gs. 150-170K)
- Sesiones/mes (crecimiento mes a mes)
- Tasa ocupación (% capacidad utilizada)
- Costos fijos (alquiler, servicios)

**Pregúntate:**
- ¿Estos números son realistas para MI caso?
- ¿Puedo conseguir 35-50 sesiones/mes en 6 meses?
- ¿El alquiler es correcto para la zona que quiero?

---

### **PASO 5: Compara con CSVs**

Para ver los números lado a lado:
1. Abre `../03-bases-datos/01-escenarios-comparacion.csv`
2. Importa a Google Sheets o Excel
3. Compara métricas clave (ROI, break-even, payback)

**Ventaja:** Ver 5 escenarios en una tabla comparativa.

---

## 📋 MÉTRICAS CLAVE EXPLICADAS

### **ROI (Return on Investment)**
**Qué es:** Ganancia año 1 / Inversión inicial × 100%

**Ejemplo:**
- Inversión: Gs. 54M
- Ganancia año 1: Gs. 33M
- ROI: 33/54 = 61%

**Qué significa:**
- ROI > 50% = Excelente
- ROI 30-50% = Bueno
- ROI < 30% = Aceptable pero lento

---

### **Break-even (Punto de Equilibrio)**
**Qué es:** Sesiones/mes necesarias para cubrir costos fijos

**Ejemplo:**
- Costos fijos: Gs. 4.76M/mes
- Precio sesión: Gs. 150K
- Costo variable: Gs. 10K/sesión
- Break-even: 4.76M / (150K - 10K) = **34 sesiones/mes**

**Qué significa:**
- < 30 sesiones/mes = MUY alcanzable
- 30-50 sesiones/mes = Alcanzable
- > 50 sesiones/mes = Difícil año 1

---

### **Payback Period**
**Qué es:** Meses para recuperar inversión inicial

**Ejemplo:**
- Inversión: Gs. 54M
- Ganancia promedio: Gs. 2.8M/mes
- Payback: 54M / 2.8M = **19 meses**

**Qué significa:**
- < 12 meses = Excelente
- 12-24 meses = Bueno
- > 24 meses = Lento

---

## ⚠️ IMPORTANTE: SUPUESTOS vs REALIDAD

**Este modelo financiero usa:**
- ✅ Datos reales: Alquileres (InfoCasas 2026), equipamiento (Seakit), tarifas (AKYFPY)
- ⚠️ Supuestos: Crecimiento sesiones/mes, retención pacientes, precio final

**LO QUE NO PUEDE PREDECIR:**
- Cuántos pacientes conseguirás mes 1 (depende de marketing y boca a boca)
- Si los pacientes volverán (depende de tu calidad clínica)
- Competencia futura (nuevos centros abriendo)

**POR ESO:**
1. Usa escenarios **conservadores** (worst case) para decisión
2. Valida con **mystery shopping** (precios reales competencia)
3. Ejecuta **plan 30 días** y ajusta con datos reales

---

## 🔗 ARCHIVOS RELACIONADOS

**Antes de leer este archivo:**
- `../referencias/00-resumen-ejecutivo.md` - Decisión en 5 páginas
- `../referencias/matriz-decision-escenarios.md` - Matriz decisión 1 página

**Después de elegir escenario:**
- `../02-plan-negocio/03-plan-financiero.md` - Plan detallado personalizado
- `../03-bases-datos/01-escenarios-comparacion.csv` - Tabla comparativa

**Para ejecutar:**
- `../implementation/plan-accion-30-dias.md` - Roadmap día por día

---

## 🎯 DECISIÓN RÁPIDA (Si no tienes tiempo)

**Si solo tienes 5 minutos:**

1. ¿Cuánto capital tienes? → Ve a PASO 2 arriba
2. Lee SOLO tu escenario recomendado
3. Verifica break-even (¿puedo conseguir esas sesiones/mes?)
4. Si sí → Decide. Si no → Lee escenario anterior (menos inversión)

**Si tienes 30 minutos:**
- Lee `escenarios-financieros.md` completo
- Compara 2-3 escenarios viables
- Usa `matriz-decision-escenarios.md` para decidir

**Si tienes dudas:**
- Completa `00-CUESTIONARIO-MIKE-CRITICO.html`
- Recibirás plan personalizado con 1 escenario recomendado

---

## 📊 ESCENARIOS EN 1 LÍNEA CADA UNO

| # | Nombre | Para Quién | Por Qué |
|---|--------|-----------|---------|
| **1** | Domicilio Puro | Sin capital, necesita validar mercado YA | ROI 857%, riesgo cero, lanza en 1 semana |
| **2** | Mixto SL | Capital moderado, vive en San Lorenzo | Balance perfecto, ROI 69%, cerca de casa |
| **3** | Consultorio Mín | Capital medio, quiere consultorio sin lujos | Viable, pero Escenario 2 o 4 son mejores opciones |
| **4** | Mixto ASU | Capital sólido, quiere ubicación premium | **RECOMENDADO** - Mejor relación riesgo/retorno |
| **5** | Premium | Capital alto, experiencia 2+ años | Solo para fisios con reputación establecida |

---

**Última actualización:** 19 Enero 2026, 02:40  
**Archivo principal:** escenarios-financieros.md (850 líneas)  
**Escenarios:** 5 (desde Gs. 4.75M hasta Gs. 75M)  
**Recomendación default:** Escenario 4 (Mixto Asunción) si tienes Gs. 50-60M
