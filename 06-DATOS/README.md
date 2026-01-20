# 📊 DATOS - Hojas de Cálculo Google Sheets

Esta carpeta contiene enlaces a todas las hojas de cálculo de datos utilizadas en el plan de negocios de Mikie Moyano Nakamura.

---

## 🔗 Hojas de Cálculo Activas

### **1. Rastreador de Clientes y Sesiones**
**Propósito:** Rastrear todos los clientes, sesiones, pagos y referencias

**Archivos CSV listos para usar:**
- [`tracking-clientes-sesiones.csv`](./tracking-clientes-sesiones.csv) - Lista maestra de clientes
- [`registro-sesiones.csv`](./registro-sesiones.csv) - Registro de cada sesión
- [`finanzas-mensuales.csv`](./finanzas-mensuales.csv) - Resumen financiero semanal

**📖 Guía completa:** [`GUIA-USO-SPREADSHEETS.md`](./GUIA-USO-SPREADSHEETS.md)

**Enlace a tu Google Sheets:** [Crear tu copia aquí - importar CSV](https://sheets.google.com)

**Hojas incluidas:**
- Lista Maestra de Clientes
- Registro de Sesiones
- Rastreador de Ingresos Semanal
- Rastreador de Gastos
- Rastreador de Referencias
- Calendario de Disponibilidad

**Frecuencia actualización:** Después de cada sesión

---

### **2. Proyecciones Financieras**
**Propósito:** Modelos financieros para tres escenarios (Pesimista, Realista, Optimista)

**Enlace:** [Insertar enlace Google Sheets aquí]

**Hojas incluidas:**
- Escenario 1: Pesimista (30% probabilidad)
- Escenario 2: Realista (50% probabilidad)
- Escenario 3: Optimista (20% probabilidad)
- Valor Esperado Ponderado
- Análisis de Sensibilidad

**Frecuencia actualización:** Revisión mensual

---

### **3. Inventario de Equipo y Suministros**
**Propósito:** Rastrear equipo, suministros y compras necesarias

**Enlace:** [Insertar enlace Google Sheets aquí]

**Hojas incluidas:**
- Inventario Actual
- Lista de Compras Pendientes
- Calendario de Reabastecimiento
- Costos por Sesión

**Frecuencia actualización:** Semanal

---

### **4. Análisis Mercado - Competidores**
**Propósito:** Datos de investigación de mercado sobre competidores en Asunción

**Enlace:** [Insertar enlace Google Sheets aquí]

**Hojas incluidas:**
- Competidores Identificados
- Análisis de Precios
- Servicios Ofrecidos
- Ubicaciones y Horarios

**Frecuencia actualización:** Trimestral

---

## 📁 Archivos CSV (Datos Históricos)

Los siguientes datos fueron exportados originalmente como CSV y ahora están en Google Sheets:

### **Datos Demográficos INE 2025**
- Población por barrio en Asunción
- Distribución por edad y género
- Niveles socioeconómicos

**Fuente de datos:** Instituto Nacional de Estadística (INE)  
**Ahora en Google Sheets:** [Insertar enlace]

---

### **Datos Legales DNIT 2025**
- Requisitos legales para fisioterapeutas
- Proceso de matriculación MSPBS
- Requisitos RUC/SET

**Fuente de datos:** DNIT - SET (Gobierno Paraguay)  
**Ahora en Google Sheets:** [Insertar enlace]

---

## 🔧 Cómo Usar Estas Hojas

### **Para Mikie (Usuario Principal):**

1. **Hacer una copia de cada hoja:**
   - Hacer clic en "Archivo" → "Hacer una copia"
   - Nombrar: "Mikie - [Nombre Hoja] - [Fecha]"
   - Guardar en tu propio Google Drive

2. **Actualizar regularmente:**
   - Rastreador Clientes: Después de cada sesión
   - Proyecciones Financieras: Final de cada mes
   - Inventario: Cada semana
   - Análisis Mercado: Cada trimestre

3. **Permisos:**
   - Mantener estas hojas PRIVADAS
   - No compartir con clientes
   - Solo compartir con asesores de confianza si es necesario

---

## 📊 Estructura de Datos Recomendada

### **Rastreador de Clientes:**
```
ID_Cliente | Nombre | Nivel | Teléfono | Fuente | Fecha_Primera_Sesión | Total_Sesiones | Estado
C001 | Ana García | 1 (VIP) | 0981-XXX | Amigo directo | 2026-01-25 | 5 | Activo
```

### **Registro de Sesiones:**
```
ID_Sesión | Fecha | ID_Cliente | Servicio | Duración | Precio | Pagado | Notas
S001 | 2026-01-25 | C001 | Masaje + Pistola | 60min | Gs.60K | ✅ | Tensión espalda baja
```

### **Rastreador de Ingresos:**
```
Semana | Fechas | Sesiones | Ingreso_Bruto | Costos | Ingreso_Neto | Acumulado
1 | Ene 20-26 | 3 | Gs.200K | Gs.420K | -Gs.220K | -Gs.220K
```

---

## 🔐 Privacidad y Seguridad

**CRÍTICO - Proteger Estos Datos:**

✅ **HACER:**
- Mantener hojas protegidas con contraseña
- Usar autenticación de dos factores en Google
- Hacer copias de respaldo semanalmente
- Solo acceder desde dispositivos seguros

❌ **NO HACER:**
- Compartir enlaces públicamente
- Incluir información médica sensible
- Publicar nombres de clientes en redes sociales
- Acceder desde computadoras públicas

---

## 📞 Soporte

**¿Problemas con las hojas?**
- Verificar permisos de acceso (debe ser "Editor" o "Propietario")
- Refrescar página del navegador
- Intentar desde navegador diferente
- Verificar conexión a internet

**¿Necesitás ayuda con fórmulas?**
- Todas las fórmulas están pre-configuradas
- No editar celdas con fondo gris (son calculadas)
- Solo ingresar datos en celdas blancas

---

## 🔄 Actualizaciones

**Última actualización:** Enero 21, 2026  
**Versión:** 4.0 (Reorganización Española)  
**Próxima revisión:** Febrero 2026 (después Mes 1 completo)

---

**NOTA:** Los datos originalmente estaban en archivos CSV pero ahora se mantienen en Google Sheets para facilitar el acceso y la actualización en tiempo real. Ver `03-INVESTIGACION/` para datos de investigación de mercado.
