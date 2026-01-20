# 📊 TEMPLATE: CONTABILIDAD SIMPLE (Registro Ingresos/Gastos)

**Para:** Mike González - Control financiero mes a mes  
**Propósito:** Trackear ingresos, gastos y métricas clave SIN contador  
**Tiempo:** 10-15 min/semana  
**Cuándo usar:** Desde Día 1 del negocio

---

## ⚡ POR QUÉ NECESITAS ESTO

**Sin tracking financiero:**
- ❌ No sabes si llegaste a break-even
- ❌ No puedes calcular ROI real vs proyectado
- ❌ Declaración impuestos anual = caos
- ❌ No detectas problemas hasta que es tarde

**Con este template:**
- ✅ Sabes exactamente cuánto ganas/gastas
- ✅ Ves si vas camino a break-even
- ✅ Puedes ajustar precios/gastos basado en datos
- ✅ Declaración impuestos = copy/paste de tu registro

---

## 📋 MÉTODO SIMPLE (Recomendado Año 1)

### **Opción A: Cuaderno Físico** (Más simple)

**Qué necesitas:**
- Cuaderno rayado (1 página = 1 semana)
- Bolígrafo
- 10 minutos cada viernes

**Formato por semana:**

```
SEMANA 1 - Feb 1-7, 2026
--------------------------------
INGRESOS:
Lunes 3:   Paciente Juan P.     Gs. 150,000  (Sesión #1)
Miércoles 5: Paciente Ana G.     Gs. 150,000  (Sesión #2)
Jueves 6:  Paciente Carlos M.   Gs. 150,000  (Sesión #3)
           TOTAL INGRESOS:       Gs. 450,000

GASTOS:
Lunes 3:   Gel conductor         Gs. 45,000
Martes 4:  Nafta (traslados)     Gs. 80,000
Viernes 7: Internet mes Feb      Gs. 150,000
           TOTAL GASTOS:         Gs. 275,000

GANANCIA SEMANAL:                Gs. 175,000
SESIONES REALIZADAS:             3
PACIENTES NUEVOS:                3
PACIENTES RECURRENTES:           0
```

**Fin de mes:** Sumas todas las semanas = Ingreso/Gasto mensual

---

### **Opción B: Google Sheets** (Más profesional)

**Ventajas:**
- Cálculos automáticos
- Gráficos
- Acceso desde celular

**Cómo crear:**

#### **HOJA 1: Registro Diario**

| Fecha | Tipo | Categoría | Descripción | Paciente | Ingreso | Gasto | Saldo |
|-------|------|-----------|-------------|----------|---------|-------|-------|
| 01/02 | Ingreso | Sesión | Evaluación inicial | Juan P. | 150.000 | | 150.000 |
| 01/02 | Gasto | Insumos | Gel ultrasonido | | | 45.000 | 105.000 |
| 03/02 | Ingreso | Sesión | Terapia manual | Ana G. | 150.000 | | 255.000 |
| 04/02 | Gasto | Transporte | Nafta domicilio | | | 80.000 | 175.000 |

**Fórmula columna Saldo:**  
`=F2-G2+H1` (donde F=Ingreso, G=Gasto, H=Saldo anterior)

---

#### **HOJA 2: Resumen Mensual**

| Mes | Ingresos | Gastos | Ganancia | Sesiones | Break-even? | ROI Acumulado |
|-----|----------|--------|----------|----------|-------------|---------------|
| Enero | 0 | 54.449.850 | -54.449.850 | 0 | NO | -100% |
| Febrero | 2.100.000 | 950.000 | 1.150.000 | 14 | NO | -98% |
| Marzo | 3.750.000 | 1.200.000 | 2.550.000 | 25 | NO | -93% |
| Abril | 5.250.000 | 1.350.000 | 3.900.000 | 35 | **SÍ** ✅ | -89% |

**Fórmulas:**
- Ganancia: `=B2-C2`
- Break-even: `=IF(B2>C2+costos_fijos,"SÍ","NO")`
- ROI Acumulado: `=SUM(D:D)/inversión_inicial`

---

#### **HOJA 3: Categorías de Gastos**

| Categoría | Febrero | Marzo | Abril | Total | % del Total |
|-----------|---------|-------|-------|-------|-------------|
| **Fijos** |
| Alquiler | 2.800.000 | 2.800.000 | 2.800.000 | 8.400.000 | 65% |
| Servicios | 350.000 | 350.000 | 350.000 | 1.050.000 | 8% |
| Impuestos | 40.000 | 40.000 | 40.000 | 120.000 | 1% |
| **Variables** |
| Insumos | 180.000 | 240.000 | 350.000 | 770.000 | 6% |
| Transporte | 120.000 | 150.000 | 180.000 | 450.000 | 4% |
| **TOTAL** | 3.490.000 | 3.580.000 | 3.720.000 | 10.790.000 | 100% |

---

## 📊 MÉTRICAS CLAVE A TRACKEAR

### **MÉTRICAS SEMANALES:**

1. **Sesiones realizadas (#)**
   - Meta semana 1-4: 2-3 sesiones/semana
   - Meta mes 2-3: 5-7 sesiones/semana
   - Meta mes 4+: 8-10 sesiones/semana

2. **Ingresos brutos (Gs.)**
   - Meta: Incremento 10-15% semana a semana

3. **Gastos variables (Gs.)**
   - Ojo: Si > 20% ingresos = estás gastando mucho en insumos

4. **Pacientes nuevos vs recurrentes (#)**
   - Ideal: 70% recurrentes, 30% nuevos (después mes 2)

---

### **MÉTRICAS MENSUALES:**

1. **Ganancia neta (Gs.)**
   - Meta mes 4: Positiva (> Gs. 0)
   - Meta mes 6: > Gs. 2M/mes
   - Meta mes 12: > Gs. 4M/mes

2. **Break-even alcanzado? (Sí/No)**
   - Fórmula: Ingresos > (Costos fijos + Costos variables)
   - Meta: Mes 4 (escenario conservador)

3. **ROI Acumulado (%)**
   - Fórmula: (Ganancia acumulada / Inversión inicial) × 100%
   - Meta año 1: > 30% (recuperaste Gs. 16M de Gs. 54M)

4. **Costo por sesión (Gs.)**
   - Fórmula: Gastos variables / Sesiones realizadas
   - Meta: < Gs. 15,000/sesión

5. **Precio promedio sesión (Gs.)**
   - Fórmula: Ingresos / Sesiones
   - Meta inicial: Gs. 150,000
   - Ajustar según mercado

---

### **MÉTRICAS TRIMESTRALES (Cada 3 meses):**

1. **Tasa retención pacientes (%)**
   - Fórmula: (Pacientes que volvieron / Total pacientes atendidos) × 100%
   - Meta: > 60%

2. **Sesiones por paciente (promedio)**
   - Fórmula: Total sesiones / Total pacientes únicos
   - Meta: > 6 sesiones/paciente (tratamiento completo)

3. **Costo adquisición cliente (CAC) (Gs.)**
   - Fórmula: Gastos marketing / Pacientes nuevos
   - Meta: < Gs. 150,000 (recuperas en 1 sesión)

---

## 🗓️ RUTINA SEMANAL (10-15 min cada viernes)

**VIERNES - Cierre de semana:**

1. **Registra sesiones faltantes** (5 min)
   - ¿Olvidaste anotar alguna sesión esta semana?
   - Revisa agenda y completa

2. **Anota gastos pendientes** (3 min)
   - Revisión de tickets/facturas
   - ¿Compraste algo y no anotaste?

3. **Calcula totales semanales** (2 min)
   - Suma ingresos semana
   - Suma gastos semana
   - Calcula ganancia semanal

4. **Actualiza métricas** (5 min)
   - Sesiones realizadas: X
   - Pacientes nuevos: X
   - Pacientes recurrentes: X
   - Break-even esta semana? (Sí/No)

5. **Compara con proyección** (5 min)
   - ¿Vas según el plan financiero?
   - ¿Necesitas ajustar algo próxima semana?

**Total tiempo:** 15 minutos máximo

---

## 📅 RUTINA MENSUAL (30 min último día del mes)

**ÚLTIMO DÍA DEL MES:**

1. **Cierra mes en registro** (10 min)
   - Verifica todas las transacciones estén anotadas
   - Suma totales mensuales

2. **Calcula métricas clave** (10 min)
   - Ganancia neta mes
   - ROI acumulado
   - Break-even alcanzado?
   - Sesiones totales vs meta

3. **Compara con proyección** (10 min)
   - Abre `02-plan-negocio/03-plan-financiero.md`
   - Compara tus números reales vs proyectados
   - ¿Vas mejor o peor? ¿Por qué?

4. **Ajustes para próximo mes** (10 min)
   - Si gastos muy altos → ¿Dónde recortar?
   - Si ingresos bajos → ¿Más marketing?
   - Si break-even no alcanzado → ¿Subir precio? ¿Más sesiones?

**Total tiempo:** 30-40 minutos

---

## 💡 EJEMPLO REAL - MES 1 (Febrero 2026)

### **Registro Diario (primeras semanas):**

```
SEMANA 1 (Feb 1-7):
Lunes 3:    Sesión Juan P.         +Gs. 150,000
Miércoles 5: Sesión Ana G.         +Gs. 150,000
Jueves 6:   Gel conductor          -Gs. 45,000
Viernes 7:  Internet (fijo)        -Gs. 150,000
TOTAL:      Ingresos Gs. 300K, Gastos Gs. 195K, Ganancia Gs. 105K

SEMANA 2 (Feb 8-14):
Lunes 10:   Sesión Carlos M.       +Gs. 150,000
Lunes 10:   Sesión Ana G. (2da)    +Gs. 150,000
Martes 11:  Sesión Juan P. (2da)   +Gs. 150,000
Jueves 13:  Nafta domicilios       -Gs. 80,000
Viernes 14: Toallas nuevas         -Gs. 65,000
TOTAL:      Ingresos Gs. 450K, Gastos Gs. 145K, Ganancia Gs. 305K

[...continúa semanas 3-4...]
```

### **Resumen Mes 1 (Febrero):**

| Métrica | Real | Proyectado | Diferencia |
|---------|------|------------|------------|
| **Sesiones** | 14 | 15 | -1 ✅ Casi perfecto |
| **Ingresos** | Gs. 2,100,000 | Gs. 2,250,000 | -Gs. 150K ⚠️ Ligeramente bajo |
| **Gastos fijos** | Gs. 3,190,000 | Gs. 3,190,000 | Gs. 0 ✅ |
| **Gastos variables** | Gs. 180,000 | Gs. 150,000 | +Gs. 30K ⚠️ Gastaste más insumos |
| **Ganancia neta** | -Gs. 1,270,000 | -Gs. 1,090,000 | -Gs. 180K ❌ Pérdida mayor |
| **Break-even?** | NO | NO | Esperado |

**Análisis:**
- ⚠️ Faltó 1 sesión (14 vs 15 proyectadas) → Más marketing semana 1
- ⚠️ Gastos insumos +20% → Comprar en mayor cantidad (descuentos)
- ✅ Pérdida mes 1 esperada (inversión inicial no se recupera mes 1)

**Acción próximo mes:**
- Objetivo: 25 sesiones (vs 14 este mes)
- Marketing: 2 gimnasios nuevos
- Insumos: Compra pack 6 meses (descuento 15%)

---

## 🚨 SEÑALES DE ALERTA (Actúa inmediato)

### **🔴 ALERTA ROJA (Crítico):**

1. **Mes 4 y no llegaste a break-even**
   - Problema: Modelo financiero no funciona
   - Acción: Sube precio Gs. 150K → Gs. 170K O reduce costos fijos

2. **Gastos variables > 25% ingresos**
   - Problema: Insumos muy caros o desperdicio
   - Acción: Cambia proveedores, compra bulk, reduce uso

3. **Caja negativa (no puedes pagar alquiler mes siguiente)**
   - Problema: Flujo de caja crítico
   - Acción: Préstamo familiar urgente O vende equipamiento no esencial

---

### **🟡 ALERTA AMARILLA (Monitorear):**

1. **Sesiones/mes estancadas 2+ meses**
   - Problema: Marketing no funciona
   - Acción: Cambia estrategia (más gimnasios, Google Ads, referidos médicos)

2. **Tasa retención < 50%**
   - Problema: Pacientes no vuelven
   - Acción: Mejora calidad atención, follow-up post-sesión, precios paquetes

3. **ROI mes 6 < 0% (aún no recuperaste nada)**
   - Problema: Muy lento crecimiento
   - Acción: Acelera marketing, sube precios, reduce costos

---

## ✅ CHECKLIST SETUP INICIAL

**Antes de primer paciente:**

- [ ] Método de registro elegido (cuaderno físico O Google Sheets)
- [ ] Categorías de gastos definidas (fijos, variables, marketing)
- [ ] Carpeta física O digital para guardar facturas/recibos
- [ ] Alarma viernes "Actualizar contabilidad" (15 min)
- [ ] Alarma último día mes "Cierre mensual" (30 min)

**Si TODOS ✅ → Listo para trackear desde Día 1**

---

## 📂 ORGANIZACIÓN DE DOCUMENTOS

### **Carpeta física (si usas cuaderno):**

```
📁 CONTABILIDAD 2026/
  ├── 📓 Cuaderno registro diario
  ├── 📂 Facturas Enero/
  ├── 📂 Facturas Febrero/
  ├── 📂 Facturas Marzo/
  ├── 📄 Resumen Trimestre 1
  └── 📄 Declaración RESIMPLE Año 1
```

### **Carpeta digital (si usas Google Sheets):**

```
Google Drive/Consultorio Mike/
  ├── Contabilidad 2026.xlsx
  ├── Facturas/
  │   ├── 2026-01-Enero/
  │   ├── 2026-02-Febrero/
  │   └── 2026-03-Marzo/
  ├── Declaraciones DNIT/
  └── Comprobantes RESIMPLE/
```

---

## 🎯 METAS FINANCIERAS AÑO 1

**Usa este tracking para verificar:**

| Mes | Meta Sesiones | Meta Ingresos | Meta Ganancia | Break-even? |
|-----|--------------|---------------|---------------|-------------|
| 1 | 15 | Gs. 2.25M | -Gs. 1.09M | NO |
| 2 | 20 | Gs. 3.00M | -Gs. 620K | NO |
| 3 | 25 | Gs. 3.75M | -Gs. 115K | NO |
| 4 | 35 | Gs. 5.25M | **+Gs. 820K** | **SÍ** ✅ |
| 5 | 40 | Gs. 6.00M | +Gs. 1.64M | Sí |
| 6 | 45 | Gs. 6.75M | +Gs. 2.41M | Sí |
| 12 | 77 | Gs. 11.55M | +Gs. 6.03M | Sí |

**Total Año 1:**
- Sesiones: 582
- Ingresos: Gs. 87.3M
- Ganancia neta: Gs. 33.5M
- ROI: **61.5%** 
- Payback: 19-20 meses

---

## 🔗 ARCHIVOS RELACIONADOS

**Plan financiero:** `../02-plan-negocio/03-plan-financiero.md`  
**Escenarios:** `../05-modelos-financieros/escenarios-financieros.md`  
**Impuestos:** `guia-dnit-resimple.md`  
**Plan 30 días:** `plan-accion-30-dias.md`

---

## 💡 TIPS PRO

1. **Foto de cada factura** (Google Drive automático)
   - App CamScanner o Google Drive scan
   - Backup si pierdes papel

2. **Anota MISMO DÍA** (no acumules)
   - 2 minutos post-sesión > 30 minutos viernes recordando

3. **Revisa métricas cada semana** (no solo fin de mes)
   - Detectas problemas temprano, ajustas rápido

4. **Compara con plan cada mes**
   - ¿Vas mejor/peor que proyección?
   - Celebra si vas mejor, ajusta si vas peor

5. **Guarda TODO 5 años**
   - DNIT puede auditar hasta 5 años atrás
   - Mejor prevenir

---

**Última actualización:** 19 Enero 2026, 03:45  
**Tiempo setup:** 30 minutos (crear template)  
**Tiempo semanal:** 10-15 minutos (actualizar)  
**Tiempo mensual:** 30-40 minutos (análisis)  
**Beneficio:** Control total de tu negocio, decisiones basadas en datos
