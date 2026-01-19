# 📊 GUÍA COMPLETA: GOOGLE SHEETS DATABASE - PROYECTO MIKE

**Fecha:** 18 Enero 2026  
**Versión:** 1.0  
**Tiempo estimado creación:** 1.5-2 horas  
**Nivel dificultad:** Intermedio (requiere conocimientos básicos Google Sheets)

---

## 🎯 OBJETIVO

Crear un **Google Sheets interactivo** que centralice TODOS los datos del proyecto Mike en un solo lugar, con:
- 8 hojas de datos
- Dashboard con métricas clave
- Fórmulas automáticas
- Gráficos visuales
- Acceso compartido con Mike

---

## 📁 ARCHIVOS CSV PREPARADOS

Ya tienes 7 archivos CSV listos para importar en `04-bases-datos/`:

1. ✅ `01-Competidores-Data.csv` (9 competidores + slots mystery shopping)
2. ✅ `02-Ubicaciones-Propiedades.csv` (10 propiedades reales)
3. ✅ `03-Equipamiento-Precios.csv` (25 equipos con precios verificados)
4. ✅ `04-Proyecciones-5-Escenarios.csv` (5 escenarios financieros)
5. ✅ `05-Marketing-Alianzas.csv` (20 contactos potenciales)
6. ✅ `06-Datos-Demograficos-INE.csv` (datos población INE)
7. ✅ `07-Tarifas-Oficiales-AKYFPY.csv` (tarifas profesionales)

---

## 🔧 PASO A PASO: CREAR EL GOOGLE SHEETS

### **PASO 1: Crear Google Sheet Base**

1. Ir a https://sheets.google.com
2. Clic en **+ Blank** (nueva hoja en blanco)
3. Renombrar el archivo: **"Plan Negocio Mike - Database Master"**
4. Configurar acceso: **Share** → Agregar email de Mike → **Editor**

---

### **PASO 2: Crear Estructura de Hojas**

Crear 9 hojas (tabs) en este orden:

| N° | Nombre Hoja | Color Tab | Propósito |
|----|-------------|-----------|-----------|
| 1 | **📊 DASHBOARD** | Azul oscuro | Resumen ejecutivo con métricas clave |
| 2 | **🏥 Competidores** | Rojo | Base de datos competencia |
| 3 | **📍 Ubicaciones** | Verde | Propiedades alquiler |
| 4 | **🛠️ Equipamiento** | Naranja | Precios equipos |
| 5 | **💰 Proyecciones** | Morado | 5 escenarios financieros |
| 6 | **📢 Marketing** | Amarillo | Alianzas y canales |
| 7 | **👥 Demografía** | Gris | Datos INE población |
| 8 | **💵 Tarifas AKYFPY** | Verde oscuro | Aranceles oficiales |
| 9 | **📝 Notas** | Blanco | Espacio libre |

**Cómo crear hojas:**
- Clic derecho en tab inferior → **Insert sheet**
- O clic en **+** al final de los tabs
- Renombrar: doble clic en nombre tab
- Cambiar color: clic derecho en tab → **Change color**

---

### **PASO 3: Importar CSVs a Cada Hoja**

Para cada hoja (2-8), importar el CSV correspondiente:

#### **Hoja 2: 🏥 Competidores**

1. Ir a hoja **🏥 Competidores**
2. Menú **File** → **Import**
3. Tab **Upload** → Seleccionar `01-Competidores-Data.csv`
4. **Import location:** Replace current sheet
5. **Separator type:** Comma
6. **Convert text to numbers:** ✅ Yes
7. Clic **Import data**

#### **Repetir para las otras 6 hojas:**

| Hoja | Archivo CSV |
|------|-------------|
| 📍 Ubicaciones | `02-Ubicaciones-Propiedades.csv` |
| 🛠️ Equipamiento | `03-Equipamiento-Precios.csv` |
| 💰 Proyecciones | `04-Proyecciones-5-Escenarios.csv` |
| 📢 Marketing | `05-Marketing-Alianzas.csv` |
| 👥 Demografía | `06-Datos-Demograficos-INE.csv` |
| 💵 Tarifas AKYFPY | `07-Tarifas-Oficiales-AKYFPY.csv` |

---

### **PASO 4: Formatear Hojas Importadas**

Para cada hoja (2-8), aplicar formato profesional:

#### **A) Formatear Encabezados:**

1. Seleccionar fila 1 (encabezados)
2. **Format** → **Text** → **Bold**
3. **Background color:** Color del tab (ej: rojo para Competidores)
4. **Text color:** Blanco
5. **Alignment:** Center
6. **Text wrapping:** Wrap

#### **B) Congelar Primera Fila:**

1. Seleccionar fila 1
2. **View** → **Freeze** → **1 row**

#### **C) Ajustar Anchos de Columna:**

1. Doble clic en borde entre letras de columnas (A|B) → Auto-ajusta
2. O seleccionar todas las columnas → Clic derecho → **Resize columns** → **Fit to data**

#### **D) Formatear Números (solo columnas de montos):**

Columnas con **Gs.** o **USD**:
1. Seleccionar columna (ej: columna "Precio_Alquiler_Gs")
2. **Format** → **Number** → **Custom number format**
3. Escribir: `#,##0` (para Guaraníes sin decimales)
4. Para USD: `$#,##0.00`

#### **E) Agregar Filtros:**

1. Seleccionar toda la tabla (Ctrl+A o clic en esquina superior izquierda)
2. **Data** → **Create a filter**
3. Aparecen iconos de filtro en encabezados

---

### **PASO 5: Crear DASHBOARD (Hoja 1)**

Esta es la hoja MÁS IMPORTANTE. Centraliza métricas clave.

#### **Estructura del Dashboard:**

```
┌────────────────────────────────────────────────────────────┐
│  📊 PLAN DE NEGOCIO MIKE - DASHBOARD EJECUTIVO            │
│  Última actualización: [FECHA AUTO]                        │
└────────────────────────────────────────────────────────────┘

┌─────────────────────┐  ┌─────────────────────┐  ┌─────────────────────┐
│ 🎯 MERCADO          │  │ 💰 FINANCIERO       │  │ 🏥 COMPETENCIA      │
│                     │  │                     │  │                     │
│ Población ASU:      │  │ Inversión:          │  │ Competidores:       │
│ 464,185             │  │ Gs. 54,449,850      │  │ 9 identificados     │
│                     │  │                     │  │                     │
│ Target 20-65+:      │  │ Break-even:         │  │ Promedio precio:    │
│ 316,631 (68%)       │  │ 35 sesiones/mes     │  │ Gs. 170,000         │
│                     │  │                     │  │                     │
│ ABC1+C2:            │  │ ROI Año 1:          │  │ Mystery shopping:   │
│ 208,000-255,000     │  │ 36.5% - 56.0%       │  │ 6 pendientes        │
└─────────────────────┘  └─────────────────────┘  └─────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│ 📊 COMPARACIÓN 5 ESCENARIOS                                │
│ [TABLA DINÁMICA DESDE HOJA PROYECCIONES]                   │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────┐  ┌─────────────────────┐
│ 📍 UBICACIONES      │  │ 🛠️ EQUIPAMIENTO     │
│                     │  │                     │
│ Propiedades:        │  │ Total items:        │
│ 10 analizadas       │  │ 25 equipos          │
│                     │  │                     │
│ Rango alquiler:     │  │ Inversión equipo:   │
│ Gs. 1.8M - 6.5M     │  │ Gs. 7,200,000       │
└─────────────────────┘  └─────────────────────┘
```

#### **Implementación Dashboard - Paso a Paso:**

##### **A) Título y Fecha:**

**Celda A1:**
```
📊 PLAN DE NEGOCIO MIKE - DASHBOARD EJECUTIVO
```
- **Font size:** 18
- **Bold:** Sí
- **Background:** #4A86E8 (azul)
- **Text color:** Blanco
- **Merge cells:** A1:H1

**Celda A2:**
```
=CONCATENATE("Última actualización: ", TEXT(TODAY(), "DD/MM/YYYY"))
```
- **Font size:** 10
- **Italic:** Sí
- **Merge cells:** A2:H2

---

##### **B) Cuadro 1: 🎯 MERCADO** (Celdas A4:C12)

**Celda A4:** (Título cuadro)
```
🎯 DATOS DE MERCADO
```
- **Font size:** 14, **Bold**
- **Background:** #93C47D (verde claro)
- **Merge:** A4:C4

**Celda A6:**
```
Población Asunción:
```

**Celda C6:** (Fórmula que trae dato de hoja Demografía)
```
=VLOOKUP("Población Total Asunción", '👥 Demografía'!A:B, 2, FALSE)
```
- **Format number:** `#,###` (sin decimales)

**Celda A7:**
```
Target 20-65+ años:
```

**Celda C7:**
```
=VLOOKUP("Mercado Objetivo 20-65+", '👥 Demografía'!A:B, 2, FALSE)
```
- **Format number:** `#,###`

**Celda A8:**
```
ABC1 + C2 (target principal):
```

**Celda C8:**
```
=VLOOKUP("Mercado Objetivo ABC1+C2", '👥 Demografía'!A:B, 2, FALSE)
```
- Mostrar como rango: **"208,000 - 255,000"** (editar manualmente o usar fórmula compleja)

**Celda A10:**
```
% Población económicamente activa:
```

**Celda C10:**
```
=VLOOKUP("Población 15-64 años", '👥 Demografía'!A:B, 2, FALSE) / VLOOKUP("Población Total Asunción", '👥 Demografía'!A:B, 2, FALSE)
```
- **Format number:** Percentage (`67.2%`)

**Celda A11:**
```
Edad mediana:
```

**Celda C11:**
```
=VLOOKUP("Edad Mediana", '👥 Demografía'!A:B, 2, FALSE)
```
- Agregar texto: **"33.1 años"**

**Aplicar bordes:**
- Seleccionar A4:C12
- **Borders:** All borders, color gris claro

---

##### **C) Cuadro 2: 💰 FINANCIERO** (Celdas E4:G12)

**Celda E4:** (Título cuadro)
```
💰 DATOS FINANCIEROS
```
- **Font size:** 14, **Bold**
- **Background:** #FFD966 (amarillo)
- **Merge:** E4:G4

**Celda E6:**
```
Escenario Recomendado:
```

**Celda G6:**
```
Mixto Completo ASU
```
- **Bold**

**Celda E7:**
```
Inversión Inicial:
```

**Celda G7:**
```
=VLOOKUP("4. Mixto Completo ASU", '💰 Proyecciones'!A:B, 2, FALSE)
```
- **Format:** `"Gs. "#,##0`

**Celda E8:**
```
Break-even:
```

**Celda G8:**
```
=VLOOKUP("4. Mixto Completo ASU", '💰 Proyecciones'!A:I, 9, FALSE) & " sesiones/mes"
```

**Celda E9:**
```
ROI Año 1:
```

**Celda G9:**
```
=VLOOKUP("4. Mixto Completo ASU", '💰 Proyecciones'!A:P, 16, FALSE) & "%"
```

**Celda E10:**
```
Payback:
```

**Celda G10:**
```
=VLOOKUP("4. Mixto Completo ASU", '💰 Proyecciones'!A:Q, 17, FALSE) & " meses"
```

**Celda E11:**
```
Ganancia Año 1:
```

**Celda G11:**
```
=VLOOKUP("4. Mixto Completo ASU", '💰 Proyecciones'!A:O, 15, FALSE)
```
- **Format:** `"Gs. "#,##0`

**Aplicar bordes:**
- Seleccionar E4:G12
- **Borders:** All borders, color gris claro

---

##### **D) Cuadro 3: 🏥 COMPETENCIA** (Celdas A14:C22)

**Celda A14:**
```
🏥 COMPETENCIA
```
- **Font size:** 14, **Bold**
- **Background:** #E06666 (rojo claro)
- **Merge:** A14:C14

**Celda A16:**
```
Competidores identificados:
```

**Celda C16:**
```
=COUNTA('🏥 Competidores'!B2:B10)
```

**Celda A17:**
```
Con precios verificados:
```

**Celda C17:**
```
=COUNTIF('🏥 Competidores'!I2:I100, "<>")
```

**Celda A18:**
```
Precio promedio sesión:
```

**Celda C18:**
```
=AVERAGE(FILTER('🏥 Competidores'!J2:J100, '🏥 Competidores'!J2:J100<>""))
```
- **Format:** `"Gs. "#,##0`

**Celda A19:**
```
Rango precios:
```

**Celda C19:**
```
=MIN(FILTER('🏥 Competidores'!J2:J100, '🏥 Competidores'!J2:J100<>"")) & " - " & MAX(FILTER('🏥 Competidores'!J2:J100, '🏥 Competidores'!J2:J100<>""))
```

**Celda A20:**
```
Mystery shopping pendiente:
```

**Celda C20:**
```
=COUNTIF('🏥 Competidores'!R2:R100, "Pendiente")
```

**Aplicar bordes:**
- Seleccionar A14:C22
- **Borders:** All borders

---

##### **E) Cuadro 4: 📍 UBICACIONES** (Celdas E14:G22)

**Celda E14:**
```
📍 UBICACIONES
```
- **Font size:** 14, **Bold**
- **Background:** #A4C2F4 (azul claro)
- **Merge:** E14:G14

**Celda E16:**
```
Propiedades analizadas:
```

**Celda G16:**
```
=COUNTA('📍 Ubicaciones'!B2:B15)
```

**Celda E17:**
```
Aptas consultorio:
```

**Celda G17:**
```
=COUNTIF('📍 Ubicaciones'!L2:L15, "Sí*")
```

**Celda E18:**
```
Alquiler promedio:
```

**Celda G18:**
```
=AVERAGE(FILTER('📍 Ubicaciones'!I2:I15, '📍 Ubicaciones'!I2:I15<>""))
```
- **Format:** `"Gs. "#,##0`

**Celda E19:**
```
Rango alquileres:
```

**Celda G19:**
```
=TEXT(MIN(FILTER('📍 Ubicaciones'!I2:I15, '📍 Ubicaciones'!I2:I15<>"")), "Gs. #,##0") & " - " & TEXT(MAX(FILTER('📍 Ubicaciones'!I2:I15, '📍 Ubicaciones'!I2:I15<>"")), "Gs. #,##0")
```

**Celda E20:**
```
Zona recomendada:
```

**Celda G20:**
```
Villa Aurelia
```
- **Bold**

**Aplicar bordes**

---

##### **F) Cuadro 5: 🛠️ EQUIPAMIENTO** (Celdas A24:C32)

**Celda A24:**
```
🛠️ EQUIPAMIENTO
```
- **Font size:** 14, **Bold**
- **Background:** #F9CB9C (naranja claro)
- **Merge:** A24:C24

**Celda A26:**
```
Total items catalogados:
```

**Celda C26:**
```
=COUNTA('🛠️ Equipamiento'!C2:C30)
```

**Celda A27:**
```
Precios verificados:
```

**Celda C27:**
```
=COUNTIF('🛠️ Equipamiento'!N2:N30, "Verificado")
```

**Celda A28:**
```
Inversión equipamiento (Escenario 4):
```

**Celda C28:**
```
Gs. 7,200,000
```
- (Valor fijo del escenario - puede calcularse sumando equipos del escenario)

**Celda A29:**
```
Equipo más caro:
```

**Celda C29:**
```
=INDEX('🛠️ Equipamiento'!C2:C30, MATCH(MAX('🛠️ Equipamiento'!F2:F30), '🛠️ Equipamiento'!F2:F30, 0))
```

**Celda A30:**
```
Proveedor principal:
```

**Celda C30:**
```
Seakit Paraguay
```

**Aplicar bordes**

---

##### **G) Tabla Comparativa 5 Escenarios** (Celdas A34:H45)

**Celda A34:**
```
📊 COMPARACIÓN 5 ESCENARIOS FINANCIEROS
```
- **Font size:** 14, **Bold**
- **Background:** #B4A7D6 (morado claro)
- **Merge:** A34:H34

**Celda A36:** (Encabezados tabla)
```
Escenario
```

**Celdas B36:H36:**
```
Inversión | ROI Año 1 | Payback (meses) | Break-even (ses/mes) | Ganancia Mes 12 | Riesgo | Recomendado Para
```
- **Bold**, **Background gris**, **Borders**

**Celdas A37:A41:** (Nombres escenarios)
```
=('💰 Proyecciones'!A2)
=('💰 Proyecciones'!A3)
=('💰 Proyecciones'!A4)
=('💰 Proyecciones'!A5)
=('💰 Proyecciones'!A6)
```

**Celdas B37:B41:** (Inversiones)
```
='💰 Proyecciones'!B2
='💰 Proyecciones'!B3
='💰 Proyecciones'!B4
='💰 Proyecciones'!B5
='💰 Proyecciones'!B6
```
- **Format:** `"Gs. "#,##0,,"M"` (muestra en millones: "Gs. 4.8M")

**Celdas C37:C41:** (ROI)
```
='💰 Proyecciones'!P2
='💰 Proyecciones'!P3
='💰 Proyecciones'!P4
='💰 Proyecciones'!P5
='💰 Proyecciones'!P6
```
- **Format:** `#,##0"%"`

**Repetir patrón para columnas D, E, F, G, H** referenciando columnas correspondientes de hoja Proyecciones.

**Aplicar formato condicional:**
- Seleccionar C37:C41 (ROI)
- **Format** → **Conditional formatting**
- **Format cells if:** Greater than `100%` → Background verde
- **Format cells if:** Between `50%` and `100%` → Background amarillo
- **Format cells if:** Less than `50%` → Background rojo claro

---

##### **H) Gráfico Comparativo** (Debajo de tabla)

1. Seleccionar tabla A36:D41
2. **Insert** → **Chart**
3. **Chart type:** Column chart (barras verticales)
4. **Chart title:** "Comparación ROI Año 1 - 5 Escenarios"
5. **Horizontal axis:** Nombres escenarios
6. **Vertical axis:** ROI %
7. **Position:** Debajo de tabla

---

### **PASO 6: Validaciones de Datos**

Agregar validaciones para evitar errores:

#### **Hoja Competidores - Columna "Estado":**
1. Seleccionar columna R (Estado) desde R2 hasta R100
2. **Data** → **Data validation**
3. **Criteria:** List from a range
4. **Range:** `Verificado, Parcial, Pendiente`
5. **On invalid data:** Reject input
6. **Appearance:** ✅ Show dropdown list

#### **Hoja Ubicaciones - Columna "Apto_Consultorio":**
1. Seleccionar columna L (Apto_Consultorio)
2. **Data validation**
3. **List:** `Sí, Sí - requiere adaptación, No`

#### **Hoja Equipamiento - Columna "Prioridad":**
1. Seleccionar columna J
2. **Data validation**
3. **List:** `Alta, Media, Baja, Recurrente`

#### **Hoja Equipamiento - Columna "Estado_Verificación":**
1. Seleccionar columna N
2. **Data validation**
3. **List:** `Verificado, Estimado, Pendiente`

---

### **PASO 7: Formato Condicional (Color Coding)**

#### **Hoja Competidores - Estado:**
1. Seleccionar columna R (Estado)
2. **Format** → **Conditional formatting**
3. **Rule 1:** Text is exactly `Verificado` → Background verde (#B7E1CD)
4. **Rule 2:** Text is exactly `Parcial` → Background amarillo (#FFE599)
5. **Rule 3:** Text is exactly `Pendiente` → Background rojo claro (#F4CCCC)

#### **Hoja Proyecciones - Riesgo:**
1. Seleccionar columna correspondiente a Riesgo
2. **Conditional formatting**
3. `MUY BAJO` / `BAJO` → Verde
4. `MEDIO` → Amarillo
5. `ALTO` / `MUY ALTO` → Rojo

#### **Hoja Equipamiento - Precio:**
1. Seleccionar columna F (Precio_Gs)
2. **Conditional formatting**
3. **Color scale:** Mínimo (verde) → Máximo (rojo)

---

### **PASO 8: Protección de Hojas**

Para evitar borrar fórmulas accidentalmente:

#### **Proteger Hoja Dashboard:**
1. Ir a hoja **📊 DASHBOARD**
2. **Data** → **Protect sheets and ranges**
3. **Sheet:** 📊 DASHBOARD
4. **Set permissions:** ✅ Restrict who can edit this range
5. **Show warning when editing** (permite editar pero advierte)
6. **Done**

#### **Repetir para hoja Proyecciones** (ya que tiene fórmulas complejas)

---

### **PASO 9: Crear Gráficos Adicionales**

#### **Gráfico 1: Distribución Población por Edad** (Hoja Demografía)

1. Ir a hoja **👥 Demografía**
2. Crear tabla manual:

| Grupo Edad | Población |
|------------|-----------|
| 0-14 años | 95,582 |
| 15-64 años | 311,932 |
| 65+ años | 56,631 |

3. Seleccionar tabla
4. **Insert** → **Chart**
5. **Chart type:** Pie chart
6. **Title:** "Distribución Poblacional Asunción 2025"

#### **Gráfico 2: Comparación Alquileres por Zona** (Hoja Ubicaciones)

1. Ir a hoja **📍 Ubicaciones**
2. Crear tabla dinámica:
   - **Rows:** Zona
   - **Values:** AVERAGE Precio_Alquiler_Gs
3. **Insert** → **Chart**
4. **Chart type:** Bar chart (horizontal)
5. **Title:** "Alquiler Promedio por Zona"

#### **Gráfico 3: Evolución Sesiones Año 1** (Hoja Proyecciones - crear nueva sub-hoja)

Crear tabla mes a mes para Escenario 4:

| Mes | Sesiones | Ingresos | Costos | Ganancia |
|-----|----------|----------|--------|----------|
| 1 | 25 | 3,900,000 | 4,670,000 | -770,000 |
| 2 | 30 | ... | ... | ... |
| ... | ... | ... | ... | ... |

1. Seleccionar columnas Mes, Ingresos, Costos
2. **Insert** → **Chart**
3. **Chart type:** Line chart
4. **Title:** "Evolución Financiera Año 1 - Escenario Mixto ASU"

---

### **PASO 10: Agregar Comentarios y Notas**

Para facilitar uso futuro:

#### **Agregar comentario a celda con fórmula compleja:**
1. Clic derecho en celda con fórmula
2. **Insert note** o **Insert comment**
3. Escribir: _"Esta fórmula calcula el promedio de precios de competidores verificados"_

#### **Celdas críticas con comentarios:**
- Dashboard C6 (Población): Nota fuente INE
- Dashboard G7 (Inversión): Nota escenario asumido
- Competidores J2 (Precio sesión): Nota "Verificar con mystery shopping"

---

### **PASO 11: Crear Enlaces entre Hojas**

Para navegación rápida:

#### **Dashboard - Agregar enlaces a otras hojas:**

**Celda A50:**
```
═══════════════════════════════════════
ACCESO RÁPIDO A HOJAS:
```

**Celdas A52:A58:** (Hipervínculos)
1. Escribir: `🏥 Ver Competidores`
2. Seleccionar celda
3. **Insert** → **Link**
4. **Link to:** Sheets in this document → **🏥 Competidores**
5. Repetir para todas las hojas

---

### **PASO 12: Configuraciones Finales**

#### **A) Configurar Zona Horaria:**
1. **File** → **Settings**
2. **Locale:** Paraguay
3. **Time zone:** (GMT-04:00) Atlantic Time (Paraguay)

#### **B) Habilitar Historial de Versiones:**
1. **File** → **Version history** → **See version history**
2. ✅ Activado por defecto
3. Útil para recuperar cambios

#### **C) Descargar Copia de Respaldo:**
1. **File** → **Download** → **Microsoft Excel (.xlsx)**
2. Guardar en `04-bases-datos/BACKUP-Google-Sheets.xlsx`

#### **D) Compartir con Mike:**
1. **Share** (botón superior derecha)
2. Agregar email Mike
3. **Role:** Editor (puede editar)
4. **Notify people:** ✅ Send email
5. Mensaje: _"Mike, acá está la base de datos completa del proyecto. Podés editar, agregar datos, y seguir el progreso. Cualquier duda, avisame."_

---

## 📊 FÓRMULAS ÚTILES ADICIONALES

### **Calcular Competidores por Zona:**
```
=COUNTIF('🏥 Competidores'!D:D, "Centro")
```

### **Promedio Alquiler Zona Específica:**
```
=AVERAGEIF('📍 Ubicaciones'!C:C, "Villa Aurelia", '📍 Ubicaciones'!I:I)
```

### **Contar Equipos Verificados vs Estimados:**
```
=COUNTIF('🛠️ Equipamiento'!N:N, "Verificado") / COUNTA('🛠️ Equipamiento'!N2:N30)
```
- **Format:** Percentage

### **Suma Total Inversión Equipamiento por Categoría:**
```
=SUMIF('🛠️ Equipamiento'!B:B, "Electroterapia", '🛠️ Equipamiento'!F:F)
```

### **Días hasta Fecha Objetivo Apertura:**
```
=DATEDIF(TODAY(), DATE(2026,6,1), "D") & " días"
```

---

## 🎨 PALETA DE COLORES RECOMENDADA

| Uso | Color Hex | Nombre |
|-----|-----------|--------|
| Encabezados principales | #4A86E8 | Azul Google |
| Positivo / Éxito | #B7E1CD | Verde claro |
| Advertencia | #FFE599 | Amarillo |
| Negativo / Pendiente | #F4CCCC | Rojo claro |
| Neutral | #D9D9D9 | Gris claro |
| Destacado | #F9CB9C | Naranja claro |

---

## 🔍 VERIFICACIÓN FINAL (Checklist)

Antes de dar por terminado:

- [ ] ✅ 9 hojas creadas y nombradas correctamente
- [ ] ✅ 7 CSVs importados sin errores
- [ ] ✅ Dashboard funcional con métricas actualizadas
- [ ] ✅ Todas las fórmulas calculan correctamente (sin #REF!, #VALUE!)
- [ ] ✅ Formato condicional aplicado (colores verde/amarillo/rojo)
- [ ] ✅ Filtros habilitados en todas las hojas de datos
- [ ] ✅ Primera fila congelada en todas las hojas
- [ ] ✅ Validaciones de datos en columnas críticas
- [ ] ✅ Gráficos visuales creados (mínimo 2)
- [ ] ✅ Compartido con Mike con permisos de Editor
- [ ] ✅ Copia de respaldo descargada (.xlsx)
- [ ] ✅ Zona horaria Paraguay configurada

---

## 🚀 PRÓXIMOS PASOS (Después de FASE-00)

Una vez Mike complete FASE-00:

1. **Actualizar Dashboard** con escenario elegido por Mike
2. **Poblar Mystery Shopping** con datos reales de llamadas
3. **Agregar hoja "Timeline"** con cronograma personalizado
4. **Crear hoja "Gastos Reales"** para tracking post-apertura
5. **Agregar hoja "Pacientes"** (cuando abra) para gestión

---

## 📱 ACCESO MÓVIL

Mike puede acceder desde celular:

1. Descargar app **Google Sheets** (Android/iOS)
2. Abrir con su cuenta Google
3. Buscar: "Plan Negocio Mike - Database Master"
4. Puede ver y editar desde el celular

---

## 💡 TIPS AVANZADOS

### **Tip 1: Usar QUERY para análisis complejos**

Crear hoja "Análisis Avanzado" con queries:

```
=QUERY('🏥 Competidores'!A:R, "SELECT D, AVG(J) WHERE J IS NOT NULL GROUP BY D ORDER BY AVG(J) DESC")
```
Resultado: Precio promedio sesión por zona

### **Tip 2: Importar datos de web automáticamente**

```
=IMPORTXML("https://www.infocasas.com.py/", "//span[@class='price']")
```
(Puede traer precios actualizados de inmobiliarias - requiere ajustes según estructura web)

### **Tip 3: Crear Alertas**

1. **Tools** → **Notification rules**
2. **When:** Any changes are made
3. **Email:** Mike's email
4. Mike recibe email cada vez que alguien edita el sheet

---

## ❓ TROUBLESHOOTING

### **Problema: Fórmulas muestran #REF!**
**Solución:** Nombre de hoja mal escrito. Verificar comillas simples alrededor del nombre.

### **Problema: Importación CSV con caracteres raros (Ã±)**
**Solución:** Al importar, seleccionar **UTF-8** encoding.

### **Problema: Números no se formatean correctamente**
**Solución:** Google Sheets puede detectar mal. Usar `=VALUE(A1)` para convertir texto a número.

### **Problema: Gráfico no actualiza automáticamente**
**Solución:** Clic derecho en gráfico → **Edit chart** → Verificar rango de datos.

---

## 📞 CONTACTO

Si tienes problemas creando el Google Sheets, documentar:
1. Captura de pantalla del error
2. Descripción paso que estabas haciendo
3. Hoja y celda donde ocurrió

---

**Tiempo estimado creación completa:** 1.5 - 2 horas  
**Resultado:** Base de datos profesional centralizada, actualizable, compartida

**Archivo:** GUIA-GOOGLE-SHEETS-COMPLETA.md  
**Fecha:** 18 Enero 2026  
**Versión:** 1.0

---

**FIN DE LA GUÍA**
