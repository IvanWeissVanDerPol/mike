# 💾 BASES DE DATOS - CSVs y Guías

**Propósito:** Datos estructurados listos para importar a Google Sheets o Excel

**Cuándo usar:** Cuando necesites comparar opciones lado a lado (ubicaciones, escenarios, competidores)

---

## 📊 CONTENIDO (9 archivos)

### **CRÍTICOS PARA DECISIÓN:**

#### **01-escenarios-comparacion.csv** ⭐
**Para qué:** Comparar 5 escenarios de inversión lado a lado  
**Cuándo usar:** Antes de decidir cuánto invertir  
**Columnas:** Escenario, Inversión, Break-even, ROI, Ganancia Mes 12, Riesgo

#### **02-proyecciones-5-escenarios.csv** ⭐
**Para qué:** Ver proyecciones mes a mes de cada escenario  
**Cuándo usar:** Después de elegir escenario preliminar, para ver flujo caja  
**Columnas:** Mes, Sesiones, Ingresos, Costos, Ganancia (x5 escenarios)

---

### **DATOS DE REFERENCIA:**

#### **03-datos-demograficos-ine.csv**
**Para qué:** Datos población Asunción por edad y zona  
**Fuente:** INE Paraguay 2025 (oficial)  
**Columnas:** Zona, Población Total, 20-39 años, 40-59 años, 60+ años

#### **04-tarifas-oficiales-akyfpy.csv**
**Para qué:** Tarifas oficiales sugeridas por asociación profesional  
**Fuente:** AKYFPY 2025  
**Columnas:** Servicio, Tarifa Particular, Tarifa Asegurado, Observaciones

---

### **LISTAS DE COMPRAS:**

#### **05-equipamiento-precios.csv**
**Para qué:** Lista equipamiento con precios reales verificados  
**Fuente:** Seakit Paraguay, proveedores locales  
**Columnas:** Equipo, Proveedor, Precio Gs., Precio USD, Prioridad

#### **06-ubicaciones-propiedades.csv**
**Para qué:** Propiedades en alquiler con datos reales  
**Fuente:** InfoCasas.com.py (enero 2026)  
**Columnas:** Dirección, Zona, Área m², Precio Gs., Precio USD, Características

---

### **PARA EJECUCIÓN:**

#### **07-marketing-alianzas.csv**
**Para qué:** Lista gimnasios y partners potenciales  
**Columnas:** Nombre, Ubicación, Contacto, Socios Estimados, Prioridad

#### **08-competidores-mystery-shopping.csv** (VACÍO - pendiente ejecutar)
**Para qué:** Registrar precios y servicios de competidores  
**Cuándo usar:** Semana de mystery shopping (llamar 5-9 competidores)  
**Columnas:** Nombre, Teléfono, Precio Sesión, Servicios, Horarios, Observaciones

---

### **GUÍA:**

#### **09-estructura-base-datos.md**
**Para qué:** Especificaciones técnicas de la base de datos  
**Cuándo leer:** Si vas a crear software personalizado (probablemente NO necesario)

---

## 🎯 CÓMO USAR ESTOS CSVs

### **OPCIÓN A: Google Sheets (RECOMENDADO)**

**Ventaja:** Interactivo, comparaciones lado a lado, fórmulas, gráficos

**Paso a paso:**
1. Abre `00-guia-setup-google-sheets.md` (instrucciones completas)
2. Crea Google Sheet nuevo
3. Importa CSVs (File → Import → Upload → cada CSV es una pestaña)
4. Agrega fórmulas y gráficos según guía
5. Comparte con familia/socios si necesario

**Tiempo:** 30 minutos setup inicial

---

### **OPCIÓN B: Excel (Alternativa)**

**Ventaja:** Offline, no necesita Google account

**Paso a paso:**
1. Abre Excel
2. Data → From Text/CSV → selecciona CSV
3. Importa cada CSV como hoja nueva
4. Agrega tablas dinámicas y gráficos

**Tiempo:** 20 minutos

---

### **OPCIÓN C: Leer Directo (Rápido pero limitado)**

**Ventaja:** Inmediato, no setup

**Desventaja:** No puedes comparar lado a lado fácilmente

**Cuándo usar:** Solo para consultas rápidas puntuales

---

## 📋 ORDEN DE USO RECOMENDADO

**Si estás decidiendo inversión:**
1. **Primero:** `01-escenarios-comparacion.csv` (ver 5 opciones)
2. **Luego:** `02-proyecciones-5-escenarios.csv` (detalle opción elegida)
3. **Después:** `referencias/matriz-decision-escenarios.md` (confirmar decisión)

**Si estás buscando ubicación:**
1. **Primero:** `06-ubicaciones-propiedades.csv` (opciones reales)
2. **Visita:** 3-5 propiedades en persona
3. **Decide:** Basado en zona, precio, accesibilidad

**Si estás comprando equipamiento:**
1. **Primero:** `05-equipamiento-precios.csv` (lista priorizada)
2. **Cotiza:** 2-3 proveedores adicionales
3. **Compra:** Según `implementation/lista-compras.md`

**Si estás validando precios:**
1. **Primero:** `04-tarifas-oficiales-akyfpy.csv` (referencia oficial)
2. **Ejecuta:** Mystery shopping (llama competidores)
3. **Completa:** `08-competidores-mystery-shopping.csv` con hallazgos
4. **Ajusta:** Tu precio según mercado real

---

## ⚠️ IMPORTANTE: DATOS VERIFICADOS

Todos los CSVs contienen **datos REALES**, no estimaciones:

- ✅ Demografía: INE Paraguay 2025 (oficial)
- ✅ Tarifas: AKYFPY 2025 (oficial)
- ✅ Equipamiento: Seakit + proveedores (cotizaciones reales enero 2026)
- ✅ Propiedades: InfoCasas.com.py (anuncios activos enero 2026)
- ✅ Proyecciones: Calculadas con datos verificados

**NO son:**
- ❌ Promedios de internet
- ❌ Datos de otros países
- ❌ Estimaciones genéricas

---

## 🔧 TROUBLESHOOTING

**Problema:** CSV se abre mal en Excel (caracteres raros)  
**Solución:** Data → From Text/CSV → Encoding: UTF-8

**Problema:** Números con comas se importan como texto  
**Solución:** Find & Replace "," por "" → Convert to Number

**Problema:** Fechas no se reconocen  
**Solución:** Formato celdas → Date → DD/MM/YYYY

---

## 🔗 ARCHIVOS RELACIONADOS

**Guía setup Google Sheets:** `00-guia-setup-google-sheets.md`  
**Resumen ejecutivo:** `../referencias/00-resumen-ejecutivo.md`  
**Escenarios detallados:** `../05-modelos-financieros/escenarios-financieros.md`  
**Plan financiero:** `../02-plan-negocio/03-plan-financiero.md`

---

**Última actualización:** 19 Enero 2026  
**Archivos CSV:** 8 (1 vacío pendiente mystery shopping)  
**Formato:** UTF-8, comma-separated
