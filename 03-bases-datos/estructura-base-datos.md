# GUÍA: ESTRUCTURA DE DATABASE GOOGLE SHEETS

**Archivo:** Database-Investigacion-Mike  
**Formato:** Google Sheets (online)  
**Hojas:** 8 tabs  
**Estado:** Estructura definida, listo para crear

---

## 📋 INSTRUCCIONES DE CREACIÓN

### **Paso 1: Crear Google Sheet**
1. Ir a Google Drive
2. Nuevo → Google Sheets
3. Nombrar: "Database-Investigacion-Mike"
4. Compartir con Mike (edición)

### **Paso 2: Crear 8 Hojas (Tabs)**

Renombrar Sheet1 → "Dashboard"  
Crear Sheet2 → "Competidores"  
Crear Sheet3 → "Ubicaciones"  
Crear Sheet4 → "Contactos-Medicos"  
Crear Sheet5 → "Gimnasios"  
Crear Sheet6 → "Equipamiento"  
Crear Sheet7 → "Proyecciones"  
Crear Sheet8 → "Seguimiento"

---

## 📊 HOJA 1: DASHBOARD

### **Estructura:**

**Sección A: Estado del Proyecto**
```
| Métrica | Valor | Estado |
|---------|-------|--------|
| Fase actual | FASE-XX | [Color] |
| % Completitud | XX% | [Barra progreso] |
| Datos verificados | XXX/200 | [Color] |
| Competidores investigados | XX/15 | [Color] |
| Locales visitados | X/5 | [Color] |
```

**Sección B: Próximas Tareas (Top 5)**
```
| Tarea | Prioridad | Fecha Límite | Estado |
|-------|-----------|--------------|--------|
| Mystery shopping | Alta | DD/MM | Pendiente |
| ... | ... | ... | ... |
```

**Sección C: Alertas**
```
| Alerta | Tipo | Acción Requerida |
|--------|------|------------------|
| FASE-00 sin completar | Crítico | Entrevistar a Mike |
| ... | ... | ... |
```

**Formato:**
- Header: Negrita, fondo azul oscuro, texto blanco
- Usar formato condicional para colores de estado
- Gráficos: Gauge chart para % completitud

---

## 📊 HOJA 2: COMPETIDORES

### **Columnas (A-R):**

```
A: ID (1, 2, 3...)
B: Nombre
C: Dirección
D: Zona
E: Teléfono
F: Website
G: Email
H: Especialidad
I: Precio Evaluación (Gs.)
J: Precio Sesión (Gs.)
K: Precio Paquete 10 (Gs.)
L: Acepta Seguros (Sí/No)
M: Horario
N: Rating Google (1-5)
O: Reviews Cantidad
P: Observaciones
Q: Fecha Investigación
R: Estado (Verificado/Pendiente)
```

### **Datos Iniciales (Poblar):**

**Fila 2:**
```
1 | Fisiocenter | Av. Perú 568 | Centro | (021) 204-600 | fisiocenter.com.py | - | Deportivo, ATM | 200,000 | 170,000 | - | Sí | 7AM-7PM | 4.5 | 50+ | AKYFPY compliant | 18/01/2026 | Verificado
```

**Fila 3:**
```
2 | CEMEFIR | Av. Venezuela 664 | Centro | - | cemefir.com.py | - | Neurológico | - | - | - | Sí | - | 4.7 | 30+ | Centro especializado | 18/01/2026 | Parcial
```

**Fila 4:**
```
3 | Kinesio Gold | Barrio Mburucuyá | Mburucuyá | - | Facebook | - | Técnicas avanzadas | - | - | - | - | - | 4.3 | 15 | Presencia solo FB | 18/01/2026 | Parcial
```

Continuar con filas 5-20 (dejar vacías para completar durante mystery shopping).

### **Formato:**
- Congelar fila 1 (headers)
- Columna I, J, K: Formato moneda (Gs.)
- Columna N: Formato número con 1 decimal
- Columna R: Formato condicional:
  - "Verificado" = Verde
  - "Parcial" = Amarillo
  - "Pendiente" = Rojo
- Habilitar filtros en todas las columnas

### **Fórmulas útiles:**
```
Celda I21: =AVERAGE(I2:I20) → Precio promedio evaluación
Celda J21: =AVERAGE(J2:J20) → Precio promedio sesión
Celda K21: =AVERAGE(K2:K20) → Precio promedio paquete
```

---

## 📊 HOJA 3: UBICACIONES

### **Columnas (A-N):**

```
A: ID
B: Zona
C: Dirección
D: m²
E: Precio/mes (Gs.)
F: Precio USD (si aplica)
G: Link Anuncio
H: Visitado (Sí/No)
I: Fecha Visita
J: Estado (Disponible/Alquilado/Descartado)
K: Pros
L: Contras
M: Puntaje (1-10)
N: Notas
```

### **Datos Iniciales (de InfoCasas.com.py):**

**Fila 2:**
```
1 | Villa Aurelia | [Dirección exacta] | 60 | 5,000,000 | - | infocasas.com.py/... | No | - | Disponible | Zona media-alta, accesible | - | 8 | Buena opción
```

**Fila 3:**
```
2 | Villa Morra | Av. Aviadores del Chaco | 154 | - | 3,000 | infocasas.com.py/... | No | - | Disponible | Zona premium | Caro | 7 | Solo si presupuesto alto
```

Poblar con 15-20 propiedades reales de DATOS-REALES-PARAGUAY-CONSOLIDADO.md

### **Formato:**
- Columna E, F: Formato moneda
- Columna H: Dropdown (Sí, No)
- Columna J: Dropdown (Disponible, Alquilado, Descartado)
- Columna M: Formato condicional (>8 verde, 5-8 amarillo, <5 rojo)

### **Fórmulas:**
```
Celda E21: =AVERAGE(E2:E20) → Alquiler promedio
Celda M21: =AVERAGE(M2:M20) → Puntaje promedio
```

---

## 📊 HOJA 4: CONTACTOS-MEDICOS

### **Columnas (A-J):**

```
A: ID
B: Nombre Dr.
C: Especialidad
D: Clínica/Hospital
E: Teléfono
F: Email
G: Contactado (Sí/No)
H: Interés (1-5)
I: Próximo Paso
J: Notas
```

**Inicialmente vacío** (llenar durante FASE-06 marketing).

### **Formato:**
- Columna G: Dropdown (Sí, No)
- Columna H: Dropdown (1, 2, 3, 4, 5)
- Formato condicional columna H:
  - 5 = Verde oscuro
  - 4 = Verde claro
  - 3 = Amarillo
  - 1-2 = Rojo

---

## 📊 HOJA 5: GIMNASIOS

### **Columnas (A-K):**

```
A: ID
B: Nombre
C: Ubicaciones (cantidad sedes)
D: Contacto
E: Teléfono
F: Email
G: Website
H: Socios Aprox
I: Propuesta
J: Estado
K: Notas
```

### **Datos Iniciales:**

**Fila 2:**
```
1 | Smart Fit | 10 sedes Asunción | Marketing | - | marketing@smartfit.com.py | smartfit.com.py | 8,000+ | Descuentos mutuos socios | A contactar | Cadena grande, buen potencial
```

**Fila 3:**
```
2 | Exen Gym | 5 sedes | - | - | - | exengym.com.py | 3,000+ | Fisio in-house para lesiones | A contactar | Especializado CrossFit/funcional
```

**Fila 4:**
```
3 | Golden Gym | 1 sede | - | - | - | goldengym.com.py | 1,500+ | Charlas preventivas | A contactar | Gym tradicional
```

**Fila 5:**
```
4 | Catapumba Fit | 1 sede (nueva 2024) | - | - | - | - | 500+ | Alianza desde inicio | A contactar | Oportunidad temprana
```

Continuar con 6-10 gimnasios más.

### **Formato:**
- Columna J: Dropdown (A contactar, Contactado, En negociación, Acuerdo, Descartado)
- Formato condicional columna J

---

## 📊 HOJA 6: EQUIPAMIENTO

### **Columnas (A-J):**

```
A: ID
B: Equipo
C: Proveedor
D: Precio Gs
E: Precio USD
F: Link/Contacto
G: Cotizado (Sí/No)
H: Alternativas
I: Prioridad (Alta/Media/Baja)
J: Notas
```

### **Datos Iniciales (de Seakit Paraguay):**

**Fila 2:**
```
1 | Ultrasonido terapéutico | Seakit Paraguay | 895,000 | 119 | seakit.com.ar/paraguay | Sí | MercadoLibre | Alta | Excelente precio verificado
```

**Fila 3:**
```
2 | Láser IR terapéutico | Seakit Paraguay | 966,000 | 129 | seakit.com.ar/paraguay | Sí | - | Media | Ahora asequible año 1
```

**Fila 4:**
```
3 | Electroestimulador TENS/FES | Biosistemas Uruguay | 3,202,500 | 427 | biosistemas.com.uy | Sí | TENS económico USD 65 | Alta | Profesional completo
```

**Fila 5:**
```
4 | Camilla fisioterapia | MercadoLibre PY | 2,500,000-5,000,000 | - | mercadolibre.com.py | No | Seakit, proveedores locales | Alta | Cotizar 3 opciones
```

Continuar con 15-20 equipos.

### **Formato:**
- Columna D, E: Formato moneda
- Columna G: Dropdown (Sí, No)
- Columna I: Dropdown (Alta, Media, Baja)
- Formato condicional columna I

---

## 📊 HOJA 7: PROYECCIONES

### **Estructura:**

**Columnas (A-J):**
```
A: Mes
B: Pacientes/semana
C: Sesiones totales
D: Ingresos Particular (Gs.)
E: Ingresos Asegurado (Gs.)
F: Total Ingresos (Gs.)
G: Costos Fijos (Gs.)
H: Costos Variables (Gs.)
I: Utilidad Neta (Gs.)
J: Flujo Acumulado (Gs.)
```

### **Datos (de FASE-05):**

**Fila 2 (Mes 1):**
```
1 | 3 | 15 | =15*150000 | =0 | =D2+E2 | 4,760,000 | =15*6000 | =F2-G2-H2 | =I2
```

**Fila 3 (Mes 2):**
```
2 | 4 | 20 | =20*150000 | =0 | =D3+E3 | 4,760,000 | =20*6000 | =F3-G3-H3 | =J2+I3
```

Continuar hasta fila 37 (mes 36).

### **Fórmulas:**
- Columna D: `=B2*150000` (asumiendo 100% particular inicialmente)
- Columna E: Agregar cuando haya pacientes asegurados
- Columna F: `=D2+E2`
- Columna G: 4,760,000 (fijo, basado en FASE-05)
- Columna H: `=C2*6000` (costo variable por sesión)
- Columna I: `=F2-G2-H2`
- Columna J: `=J[anterior]+I[actual]`

### **Gráficos:**
- Gráfico línea: Ingresos vs Costos (meses 1-12)
- Gráfico línea: Flujo acumulado (meses 1-36)
- Gráfico columnas: Utilidad neta mensual

---

## 📊 HOJA 8: SEGUIMIENTO

### **Columnas (A-F):**

```
A: Fase
B: Nombre
C: Estado (Pendiente/En progreso/Completada)
D: % Completitud
E: Fecha Límite
F: Notas
```

### **Datos:**

```
Fila 2: FASE-00 | Información Base Mike | Completada | 100% | - | Cuestionario listo
Fila 3: FASE-01 | Setup Proyecto | Completada | 90% | - | Google Sheets pendiente
Fila 4: FASE-02 | Investigación Demográfica | Pendiente | 0% | Semana 2-3 | Iniciar próximamente
...
Fila 22: FASE-20 | Validación Final | Pendiente | 0% | Semana 21-23 | Al final
```

### **Formato:**
- Columna C: Dropdown (Pendiente, En progreso, Completada)
- Columna D: Formato porcentaje
- Formato condicional columna C

---

## ✅ CHECKLIST DE CREACIÓN

```
☐ Google Sheet creado y compartido
☐ 8 hojas creadas con nombres correctos
☐ HOJA 1 (Dashboard): Estructura + formato
☐ HOJA 2 (Competidores): 9 filas pobladas con datos reales
☐ HOJA 3 (Ubicaciones): 15+ filas pobladas con InfoCasas
☐ HOJA 4 (Contactos-Medicos): Headers listos
☐ HOJA 5 (Gimnasios): 4-10 filas pobladas
☐ HOJA 6 (Equipamiento): 15+ filas pobladas con Seakit + otros
☐ HOJA 7 (Proyecciones): Fórmulas configuradas meses 1-36
☐ HOJA 8 (Seguimiento): 21 fases listadas
☐ Formato condicional aplicado
☐ Filtros habilitados
☐ Gráficos creados en Dashboard y Proyecciones
```

---

## 📝 MANTENIMIENTO

**Actualizar SEMANALMENTE:**
- Dashboard: Estado actual, % completitud
- Competidores: Nuevos datos de mystery shopping
- Ubicaciones: Nuevas propiedades encontradas
- Seguimiento: Marcar fases completadas

**Backup:**
- Descargar como Excel cada 2 semanas
- Guardar en: `04-bases-datos/Database-Investigacion-Mike-[FECHA].xlsx`

---

**Tiempo estimado creación:** 1.5-2 horas  
**Última actualización:** 18 Enero 2026  
**Estado:** Guía completa, listo para ejecutar
