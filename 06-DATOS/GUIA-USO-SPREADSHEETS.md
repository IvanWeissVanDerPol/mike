# 📊 GUÍA DE USO - Spreadsheets

**Propósito:** Cómo usar las plantillas CSV para tracking  
**Tiempo setup:** 15 minutos  
**Herramientas:** Google Sheets (gratis) o Excel

---

## 🎯 ARCHIVOS INCLUIDOS

### **1. tracking-clientes-sesiones.csv**
- **Qué es:** Lista maestra de todos tus clientes
- **Actualizar:** Cuando tengas cliente nuevo
- **Campos clave:**
  - `ID_Cliente`: C001, C002, C003... (único por cliente)
  - `Nivel_Precio`: 1=VIP (100K), 2=Estándar (80K), 3=Descuento (60K)
  - `Estado`: Activo, Inactivo, Pausado

### **2. registro-sesiones.csv**
- **Qué es:** Registro de CADA sesión realizada
- **Actualizar:** Después de CADA sesión (mismo día)
- **Campos clave:**
  - `ID_Sesion`: S001, S002, S003... (único por sesión)
  - `Pagado`: Si/No/Pendiente
  - `Notas_Sesion`: Qué trabajaste, cómo se sintió cliente

### **3. finanzas-mensuales.csv**
- **Qué es:** Resumen semanal de ingresos/gastos
- **Actualizar:** Fin de cada semana (domingo)
- **Campos clave:**
  - `Ingreso_Neto_Gs`: Ingreso bruto - todos los gastos
  - `Ahorros_Acumulados_Gs`: Suma acumulativa (objetivo: Gs. 15-20M)

---

## 🚀 CÓMO IMPORTAR A GOOGLE SHEETS

### **Opción A: Importar CSV (Recomendado)**

1. **Ir a Google Sheets:** https://sheets.google.com
2. **Crear hoja nueva** → Clic en "+ Blank"
3. **Importar archivo:**
   - Menú: File → Import
   - Tab: Upload → "Select a file from your device"
   - Buscar: `tracking-clientes-sesiones.csv`
   - Import location: "Replace spreadsheet"
   - Separator type: "Comma"
   - Clic: "Import data"
4. **Repetir para otros 2 archivos** (crear hoja nueva cada vez)
5. **Opcional:** Combinar las 3 hojas en 1 archivo (copiar/pegar entre tabs)

**Tiempo:** 5 minutos

---

### **Opción B: Copiar y Pegar Manual**

1. Abrir archivo CSV con Notepad (clic derecho → "Abrir con" → Notepad)
2. Copiar todo el contenido
3. Crear Google Sheet nuevo
4. Pegar en celda A1
5. Menú: Data → "Split text to columns"
6. Ajustar anchos de columna

**Tiempo:** 3 minutos por archivo

---

## 📝 CÓMO USAR - WORKFLOW DIARIO

### **Después de CADA sesión:**

1. **Abrir:** `registro-sesiones.csv` (o tu Google Sheet)
2. **Agregar fila nueva:**
   ```
   S006, 2026-02-10, C001, Ana García, Masaje relajante, 60, 100000, Si, Efectivo, Mi domicilio, Trabajó espalda alta
   ```
3. **Guardar** (Google Sheets auto-guarda)
4. **Tiempo:** 2 minutos

---

### **Fin de cada semana (Domingo):**

1. **Abrir:** `finanzas-mensuales.csv`
2. **Sumar sesiones de la semana:**
   - Contar cuántas sesiones (ej: 5)
   - Sumar todos los ingresos (ej: Gs. 420K)
   - Sumar gastos (aceite, transporte, etc.)
3. **Calcular:**
   ```
   Ingreso_Neto = Ingreso_Bruto - Gastos
   Ahorros_Acumulados = Ahorros_Anteriores + Ingreso_Neto
   ```
4. **Agregar fila nueva**
5. **Tiempo:** 10 minutos

---

### **Cuando cliente nuevo:**

1. **Abrir:** `tracking-clientes-sesiones.csv`
2. **Agregar fila:**
   ```
   C004, Pedro Gómez, 0971-555666, pedro@email.com, Referido gimnasio, 2026-02-12, 0, Prospecto, 2, Contactó por Instagram
   ```
3. **Nota:** Total_Sesiones empieza en 0, se actualiza después de primera sesión
4. **Tiempo:** 1 minuto

---

## 📊 FÓRMULAS ÚTILES (Google Sheets)

### **En hoja "Resumen" (crear nueva tab):**

**Total sesiones realizadas:**
```
=COUNTA(registro-sesiones!A:A)-1
```
(Cuenta filas en registro-sesiones, menos header)

**Ingreso total mes actual:**
```
=SUMIF(finanzas-mensuales!A:A, "1", finanzas-mensuales!F:F)
```
(Suma ingresos donde Mes = 1)

**Cliente con más sesiones:**
```
=SORT(tracking-clientes-sesiones!A:G, 7, FALSE)
```
(Ordena por columna 7 = Total_Sesiones, descendente)

**Promedio precio por sesión:**
```
=AVERAGE(registro-sesiones!G:G)
```

---

## 🎨 FORMATEO RECOMENDADO

### **Colores para Estado (tracking-clientes-sesiones):**

1. Seleccionar columna "Estado"
2. Format → Conditional formatting
3. Reglas:
   - Si texto = "Activo" → Fondo verde claro
   - Si texto = "Inactivo" → Fondo rojo claro
   - Si texto = "Pausado" → Fondo amarillo

### **Colores para Pagado (registro-sesiones):**

- "Si" → Verde claro
- "No" → Rojo claro
- "Pendiente" → Amarillo

### **Formato moneda:**

1. Seleccionar columnas con precios (Precio_Gs, Ingreso_Bruto_Gs, etc.)
2. Format → Number → "Custom number format"
3. Escribir: `#,##0 "Gs."`
4. Ahora muestra: `100,000 Gs.` en vez de `100000`

---

## 📈 GRÁFICOS RECOMENDADOS

### **Gráfico 1: Sesiones por Semana**

1. Datos: finanzas-mensuales, columnas Semana + Sesiones_Realizadas
2. Insert → Chart
3. Tipo: Line chart
4. Uso: Ver si estás creciendo cada semana

### **Gráfico 2: Ahorros Acumulados**

1. Datos: finanzas-mensuales, columnas Semana + Ahorros_Acumulados_Gs
2. Tipo: Area chart
3. Uso: Ver progreso hacia meta Gs. 15-20M

### **Gráfico 3: Top 5 Clientes**

1. Datos: tracking-clientes-sesiones, columnas Nombre_Cliente + Total_Sesiones
2. Tipo: Bar chart (horizontal)
3. Uso: Identificar clientes más frecuentes (VIPs)

---

## 🔒 SEGURIDAD Y BACKUP

### **Proteger tus datos:**

✅ **HACER:**
- Activar 2FA en cuenta Google
- NO compartir enlace de Google Sheets públicamente
- Hacer backup semanal (File → Download → CSV)
- Guardar backups en carpeta local + USB

❌ **NO HACER:**
- Acceder desde computadora pública
- Compartir con "Anyone with link"
- Incluir diagnósticos médicos sensibles

### **Backup semanal:**

1. Abrir Google Sheet
2. File → Download → "Comma-separated values (.csv)"
3. Guardar en: `C:\Backups\Mikie-Sesiones-YYYY-MM-DD.csv`
4. Copiar a USB cada mes

---

## 📱 USO MÓVIL

### **Google Sheets app (iOS/Android):**

✅ **Ventajas:**
- Actualizar desde celular (después de sesión)
- Auto-sync (no necesitas "guardar")
- Offline mode (editar sin internet)

✅ **Recomendado para:**
- Registrar sesión rápidamente (2 min)
- Consultar horarios disponibles
- Verificar si cliente pagó

❌ **NO recomendado para:**
- Análisis financiero complejo (mejor en computadora)
- Crear gráficos

---

## ❓ PREGUNTAS FRECUENTES

**P: ¿Necesito pagar por Google Sheets?**  
R: NO. Google Sheets es gratis (solo necesitas cuenta Gmail).

**P: ¿Puedo usar Excel en vez de Google Sheets?**  
R: SÍ. Los archivos CSV funcionan en Excel también. Pero Google Sheets es mejor porque auto-guarda y puedes acceder desde celular.

**P: ¿Qué hago si borro algo por error?**  
R: Google Sheets: File → Version history → "See version history". Puedes restaurar versión anterior.

**P: ¿Cuánto espacio ocupan estos datos?**  
R: Muy poco. 1 año de datos (300 sesiones) = ~50KB. Google te da 15GB gratis.

**P: ¿Puedo compartir con contador/asesor?**  
R: SÍ. Share → "Share with people" → Email de tu contador → "Editor" o "Viewer"

**P: ¿Necesito actualizar TODOS los archivos?**  
R: Mínimo esencial: `registro-sesiones.csv` (después de CADA sesión). Los otros son opcionales pero recomendados.

---

## 🔄 MIGRAR A SISTEMA MÁS AVANZADO

### **Cuando crezcas (50+ sesiones/mes):**

Considera migrar a:
- **Software médico:** MediLink, DoctorPlus (Paraguay)
- **CRM:** HubSpot, Zoho CRM (gratis para empezar)
- **App especializada:** SimplePractice, Jane App

**Por ahora:** Google Sheets es perfecto (0-100 clientes)

---

## ✅ CHECKLIST SETUP INICIAL

**Antes de tu primera sesión:**

- [ ] Importar 3 archivos CSV a Google Sheets
- [ ] Crear tab "Resumen" con fórmulas básicas
- [ ] Agregar colores condicionales (Activo=verde, etc.)
- [ ] Hacer backup local de archivos
- [ ] Instalar Google Sheets app en celular
- [ ] Configurar acceso offline
- [ ] Agregar bookmark en navegador

**Tiempo total:** 20 minutos

---

## 📞 SI NECESITAS AYUDA

**Tutoriales Google Sheets:**
- YouTube: "Google Sheets tutorial español"
- Google: https://support.google.com/docs/answer/6000292

**Fórmulas útiles:**
- https://support.google.com/docs/table/25273

---

**Última actualización:** Enero 2026  
**Versión:** 1.0 (Básico - Fase 1)  
**Próxima versión:** Mes 6 (agregar análisis avanzado)
