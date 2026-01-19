# 📊 GUÍA SETUP GOOGLE SHEETS - BASE DE DATOS PROYECTO MIKE

**Objetivo:** Centralizar todos los datos en una sola hoja de cálculo interactiva  
**Tiempo setup:** 30 minutos  
**Costo:** GRATIS  
**Resultado:** Dashboard decisional con 5 hojas interconectadas

---

## 🎯 POR QUÉ GOOGLE SHEETS

**Problemas actuales:**
- Datos en 48 archivos markdown diferentes
- Difícil comparar zonas side-by-side
- Difícil actualizar precios (hay que editar 5 archivos)
- No exportable a Excel para banco/inversores

**Con Google Sheets:**
- ✅ Todo en un solo lugar
- ✅ Filtros y ordenamiento dinámico
- ✅ Comparaciones automáticas
- ✅ Gráficos generados automáticamente
- ✅ Exportable a Excel/PDF
- ✅ Accesible desde celular

---

## 📋 ESTRUCTURA: 5 HOJAS (TABS)

### **HOJA 1: Competidores**
Datos de mystery shopping + investigación

**Columnas:**
| A | B | C | D | E | F | G | H | I | J | K |
|---|---|---|---|---|---|---|---|---|---|---|
| ID | Nombre | Zona | Dirección | Teléfono | Web | Precio Sesión | Precio Evaluación | Duración | Paquetes | Equipamiento | Años Mercado | Observaciones |

**Ejemplo fila:**
```
1 | Fisiocenter | Centro | Av. Perú 568 | 021 444 555 | fisiocenter.com.py | Gs. 160,000 | Gs. 200,000 | 45 min | 10 ses: Gs. 1.5M | Completo | 5+ | Presencia digital fuerte
```

---

### **HOJA 2: Ubicaciones-Alquileres**
Propiedades para alquilar consultorio

**Columnas:**
| A | B | C | D | E | F | G | H | I | J | K |
|---|---|---|---|---|---|---|---|---|---|---|
| ID | Dirección | Zona | m² | Precio/mes | Garantía | Parking | Baño | Observaciones | Link InfoCasas | Estado | Calificación (1-5) |

**Ejemplo fila:**
```
1 | Av. Venezuela 123 | Villa Aurelia | 80 | Gs. 2,800,000 | 2 meses | Sí (2 espacios) | Privado | Primer piso, ventanas grandes | https://infocasas.com.py/... | Disponible | 4/5
```

---

### **HOJA 3: Equipamiento-Precios**
Cotizaciones proveedores, precios verificados

**Columnas:**
| A | B | C | D | E | F | G | H |
|---|---|---|---|---|---|---|---|
| Categoría | Item | Marca | Proveedor | Precio | Link/Contacto | Fecha Cotización | Observaciones |

**Ejemplo fila:**
```
Electroterapia | Ultrasonido profesional | Enraf-Nonius | Seakit | Gs. 895,000 | seakit.com.ar | 15-Ene-2026 | 1 año garantía
```

---

### **HOJA 4: Escenarios-Financieros**
Los 5 escenarios comparados side-by-side

**Columnas:**
| A | B | C | D | E | F |
|---|---|---|---|---|---|
| Concepto | Domicilio Puro | Mixto Básico (SL) | Consultorio Mínimo | Mixto Completo (ASU) | Consultorio Óptimo |

**Filas (conceptos):**
```
Inversión Inicial
Costos Fijos Mensuales
Costo Variable por Sesión
Precio Sesión Promedio
Break-even (sesiones/mes)
Ganancia Mes 1
Ganancia Año 1
ROI Año 1
Payback (meses)
Riesgo
```

---

### **HOJA 5: Marketing-Alianzas**
Gimnasios, médicos, canales de captación

**Columnas:**
| A | B | C | D | E | F | G | H | I |
|---|---|---|---|---|---|---|---|---|
| ID | Tipo | Nombre | Contacto | Teléfono | Email | Dirección | Fecha Contacto | Estado | Acuerdo | Observaciones |

**Tipos:** Gimnasio, Traumatólogo, Geriatra, Empresa (corporativo), Clínica

**Estados:** No contactado, Contactado, Interesado, Acuerdo firmado, Rechazado

**Ejemplo fila:**
```
1 | Gimnasio | Smart Fit Villa Morra | Juan Pérez | 0981-123-456 | contacto@smartfit.com.py | Av. Mariscal López 123 | 20-Ene-2026 | Acuerdo firmado | Poster en recepción + 10% dto socios | 2000 socios, alto potencial
```

---

## 🚀 PASO A PASO: CREAR GOOGLE SHEETS

### **PASO 1: Crear hoja nueva (5 minutos)**

1. Ir a: https://sheets.google.com
2. Click "Blank" (hoja en blanco)
3. Renombrar archivo: "Base Datos - Plan Negocio Mike Fisioterapia"
4. Crear 5 hojas (tabs en la parte inferior):
   - Renombrar "Sheet1" → "Competidores"
   - Click "+" → Crear "Ubicaciones-Alquileres"
   - Click "+" → Crear "Equipamiento-Precios"
   - Click "+" → Crear "Escenarios-Financieros"
   - Click "+" → Crear "Marketing-Alianzas"

---

### **PASO 2: Importar datos existentes (10 minutos)**

**Opción A: Copiar-pegar desde CSV**

1. Abrir `Competidores-Data.csv` (en esta carpeta)
2. Seleccionar todo (Ctrl+A)
3. Copiar (Ctrl+C)
4. En Google Sheets, pestaña "Competidores", celda A1
5. Pegar (Ctrl+V)
6. Repetir para las otras 4 hojas

**Opción B: Importar archivo**

1. En Google Sheets: File → Import
2. Upload → Seleccionar `Competidores-Data.csv`
3. Import location: "Replace current sheet"
4. Click "Import data"

---

### **PASO 3: Formato y estilo (10 minutos)**

**Para cada hoja:**

1. **Fila de encabezados:**
   - Seleccionar fila 1
   - Format → Text → Bold
   - Format → Fill color → Gris claro
   - View → Freeze → 1 row (para scroll con encabezados visibles)

2. **Columnas de precio:**
   - Seleccionar columnas con precios (ej: columna G en Competidores)
   - Format → Number → Custom number format
   - Formato: `"Gs. "#,##0` (para que muestre: Gs. 160,000)

3. **Columnas de porcentaje:**
   - Format → Number → Percent

4. **Ajustar ancho columnas:**
   - Doble click en borde entre columnas (autoajusta)

---

### **PASO 4: Agregar fórmulas útiles (5 minutos)**

**HOJA "Competidores" - Calcular promedio precio:**

En celda vacía (ej: M2):
```
=AVERAGE(G2:G10)
```
→ Calcula promedio precio sesión de todos los competidores

Agregar label en celda L2: `Promedio Mercado:`

---

**HOJA "Ubicaciones-Alquileres" - Ranking por precio:**

En columna L (después de Calificación):
Agregar encabezado: `Ranking Precio`

En L2:
```
=RANK(E2,E:E,1)
```
→ 1 = más barato, aumenta según más caro

---

**HOJA "Escenarios-Financieros" - Mejor ROI:**

En celda destacada (ej: G2):
```
=MAX(B10:F10)
```
Donde fila 10 es "ROI Año 1"

Label: `Mejor ROI:`

---

### **PASO 5: Crear gráficos (opcionales, 5 minutos)**

**Gráfico 1: Comparación precios competencia**

1. En hoja "Competidores", seleccionar columnas: Nombre (B) y Precio Sesión (G)
2. Insert → Chart
3. Chart type: Column chart
4. Título: "Precios Competencia Asunción 2026"
5. Mover gráfico al lado derecho de la tabla

**Gráfico 2: Comparación escenarios inversión**

1. En hoja "Escenarios-Financieros", seleccionar:
   - Fila "Inversión Inicial"
   - Fila "Ganancia Año 1"
2. Insert → Chart
3. Chart type: Grouped bar chart
4. Título: "Inversión vs Ganancia - 5 Escenarios"

---

## 📊 FUNCIONES AVANZADAS (OPCIONAL)

### **Filtros dinámicos**

Ejemplo: Filtrar competidores por zona

1. Seleccionar toda la tabla (A1:M20)
2. Data → Create a filter
3. Click icono filtro en columna "Zona"
4. Seleccionar solo "Villa Aurelia" → Ver solo competidores en esa zona

---

### **Validación de datos (listas desplegables)**

Ejemplo: Columna "Estado" en Marketing-Alianzas

1. Seleccionar columna "Estado" (I2:I100)
2. Data → Data validation
3. Criteria: List of items
4. Items: `No contactado, Contactado, Interesado, Acuerdo firmado, Rechazado`
5. Save

Ahora al hacer click en celda de "Estado", aparece dropdown con opciones.

---

### **Formato condicional (colores automáticos)**

Ejemplo: Resaltar precios bajos en verde, altos en rojo

1. Seleccionar columna "Precio Sesión" (G2:G20)
2. Format → Conditional formatting
3. Format rules: Color scale
   - Minpoint: Verde
   - Midpoint: Amarillo
   - Maxpoint: Rojo
4. Done

Ahora precios bajos se ven verdes automáticamente.

---

## 💾 EXPORTAR DATOS

### **Para presentar a banco/inversores:**

1. File → Download → Microsoft Excel (.xlsx)
   - O Download → PDF (si solo quieren ver, no editar)

2. Imprimir hoja específica:
   - Ir a hoja "Escenarios-Financieros"
   - File → Print
   - Settings: "Current sheet"
   - Click "Next" → Descargar PDF

---

## 🔄 MANTENIMIENTO

**Actualizar regularmente:**

| Dato | Frecuencia | Acción |
|------|------------|--------|
| Precios competencia | Cada 6 meses | Mystery shopping nuevo, actualizar columna G |
| Alquileres disponibles | Mensual | Agregar nuevas propiedades, marcar "No disponible" las antiguas |
| Equipamiento | Trimestral | Actualizar precios (pueden bajar/subir) |
| Marketing-Alianzas | Semanal | Agregar nuevos contactos, actualizar estados |
| Escenarios | Una vez (post FASE-00) | Personalizar con datos reales de Mike |

---

## ✅ CHECKLIST SETUP COMPLETO

- [ ] Google Sheets creado y nombrado
- [ ] 5 hojas (tabs) creadas con nombres correctos
- [ ] Datos CSV importados a cada hoja
- [ ] Encabezados formateados (negrita, fondo gris, fila congelada)
- [ ] Columnas de precios formateadas como "Gs. #,##0"
- [ ] Fórmulas agregadas (promedio, ranking, mejor ROI)
- [ ] 1-2 gráficos creados (opcional pero recomendado)
- [ ] Filtros activados en todas las hojas
- [ ] Compartido con Mike (si aplica)
- [ ] Exportado a Excel como backup

---

## 📞 USOS PRÁCTICOS

### **Uso 1: Decidir ubicación consultorio**

1. Ir a hoja "Ubicaciones-Alquileres"
2. Filtrar por: Zona = "Villa Aurelia"
3. Ordenar por: Precio/mes (menor a mayor)
4. Ver columna "Calificación"
5. **Decisión:** Propiedad con mejor relación precio/calidad (ej: 4/5 estrellas, precio Gs. 2.8M)

---

### **Uso 2: Ajustar precio sesión**

1. Ir a hoja "Competidores"
2. Ver celda "Promedio Mercado": Gs. XXX,XXX
3. Decidir: -10% (penetración), 0% (competitivo), +10% (premium)
4. Ir a hoja "Escenarios-Financieros"
5. Actualizar fila "Precio Sesión Promedio"
6. Ver automáticamente cómo cambia: Break-even, Ganancia Mes 1, ROI

---

### **Uso 3: Tracking alianzas marketing**

1. Ir a hoja "Marketing-Alianzas"
2. Agregar fila nueva cada vez que contactes gimnasio/médico
3. Actualizar columna "Estado" según avanza relación
4. Ver cuántos están en "Acuerdo firmado"
5. **Meta mes 1:** 3 acuerdos firmados

---

## 🚨 ERRORES COMUNES A EVITAR

❌ **No hacer backup**  
→ File → Make a copy (cada semana)

❌ **Borrar accidentalmente datos**  
→ Edit → Version history (puedes restaurar versión anterior)

❌ **Formato inconsistente**  
→ Seguir guía de formato en Paso 3

❌ **No actualizar datos**  
→ Hoja vieja = decisiones equivocadas

---

## 📱 ACCESO MÓVIL

1. Descargar app "Google Sheets" (Android/iOS)
2. Iniciar sesión con misma cuenta Google
3. Abrir "Base Datos - Plan Negocio Mike"
4. **Útil para:** Actualizar datos durante visitas (gimnasios, propiedades)

---

## 🎯 RESULTADO ESPERADO

**Antes:**
- Datos en 48 archivos markdown
- Difícil comparar, actualizar, compartir
- No visual, solo texto

**Después:**
- Todo en 1 Google Sheet (5 hojas)
- Comparaciones side-by-side
- Gráficos automáticos
- Exportable a Excel/PDF
- Actualizable desde celular
- Listo para presentar a banco

---

**ÚLTIMA ACTUALIZACIÓN:** 19 Enero 2026  
**VERSIÓN:** 1.0  
**PREREQUISITO:** Cuenta Google (gratis)  
**TIEMPO TOTAL SETUP:** 30-40 minutos  
**PRÓXIMO PASO:** Poblar hojas con datos de mystery shopping + FASE-00
