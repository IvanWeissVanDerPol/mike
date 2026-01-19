# 📏 Convención de Nombres - Repositorio Mike

**Versión:** 2.0  
**Fecha:** 18 Enero 2026  
**Estado:** Estándar oficial del proyecto

---

## 🎯 Estándar: español-kebab-case

**Todos los archivos y carpetas siguen este formato:**

✅ **Todo en español** (idioma del cliente Mike)  
✅ **Todo en minúsculas** (sin MAYÚSCULAS)  
✅ **Palabras separadas con guiones** (-)  
✅ **Sin espacios, sin guiones bajos** (_, no permitidos)  
✅ **Números al inicio permitidos** (01-, 02-, etc.)

---

## ✅ EJEMPLOS CORRECTOS

### **Archivos:**
```
✅ empieza-aqui.md
✅ analisis-financiero.md
✅ 01-analisis-mercado.md
✅ datos-paraguay-2025.md
✅ investigacion-nichos-resumen.md
```

### **Carpetas:**
```
✅ 01-investigacion/
✅ 02-plan-negocio/
✅ 03-bases-datos/
✅ implementation/
✅ docs/
✅ archivo-viejo/
```

---

## ❌ EJEMPLOS INCORRECTOS

```
❌ README.md                          (inglés)
❌ ANALISIS-MERCADO.md                (MAYÚSCULAS)
❌ Analisis-Mercado.md                (camelCase)
❌ analisis_mercado.md                (guiones bajos)
❌ analisis mercado.md                (espacios)
❌ 01-ANALISIS-MERCADO-DRAFT.md       (MAYÚSCULAS + -DRAFT)
```

---

## 🔢 REGLAS DE NUMERACIÓN

### **Cuándo numerar archivos/carpetas:**

✅ **SÍ - Numerar estos:**
1. **Documentos de lectura secuencial** (plan de negocio, guías)
2. **Pasos de proceso ordenado** (fases, etapas, procedimientos)
3. **Listas priorizadas** (prioridad 1, 2, 3...)
4. **Carpetas de flujo de trabajo** (investigación → plan → implementación)

❌ **NO - No numerar estos:**
1. **Documentos de referencia** (se consultan según necesidad)
2. **Archivos de acción** (usuario elige orden)
3. **Archivos históricos/archive** (orden cronológico, no secuencial)
4. **Herramientas standalone** (sin secuencia lógica)

---

### **Formato de numeración:**

**Archivos secuenciales:**
```
00-indice.md                  (índice/resumen - siempre 00)
01-primer-documento.md
02-segundo-documento.md
03-tercer-documento.md
...
```

**Carpetas de workflow:**
```
01-investigacion/             (etapa 1)
02-planificacion/             (etapa 2)
03-implementacion/            (etapa 3)
```

**Brechas intencionales (opcional):**
```
10-fase-inicial/              (espacio para 11-19)
20-fase-intermedia/           (espacio para 21-29)
30-fase-final/                (espacio para 31-39)
90-archivo/                   (claramente separado)
```

---

### **Reglas específicas:**

1. **Usar 2 dígitos** para mejor ordenamiento:
   - ✅ `01-archivo.md` (se ordena correctamente)
   - ❌ `1-archivo.md` (se ordena mal: 1, 10, 2, 3...)

2. **Índices siempre 00**:
   - ✅ `00-indice.md` (aparece primero)
   - ❌ `indice.md` (se ordena alfabéticamente, no primero)

3. **Sin brechas a menos que sean intencionales**:
   - ✅ `01, 02, 03, 04` (secuencial)
   - ✅ `10, 20, 30, 40` (brechas intencionales para expansión)
   - ❌ `01, 03, 05, 09` (brechas accidentales - confunde)

4. **No usar rangos en nombres**:
   - ❌ `02-05-plantillas.md` (confuso: ¿es rango? ¿es versión?)
   - ✅ `02-plantillas.md` (claro)

---

## 📁 ESTRUCTURA ACTUAL DEL REPOSITORIO

### **Carpetas Raíz (Numeradas):**

```
01-investigacion/             (datos, investigación mercado)
02-plan-negocio/              (business plan 8 documentos)
03-bases-datos/               (guías Google Sheets)
04-plantillas/                (formularios pacientes)
05-modelos-financieros/       (calculadoras escenarios)
06-archivo/                   (anexos, documentos extra)
```

**Nota:** Secuencia perfecta 01-06, sin brechas. ✅

### **Carpetas Raíz (Sin Numerar):**

```
docs/                         (documentación técnica)
implementation/               (planes acción)
archivo-viejo/                (versiones antiguas)
```

**Razón:** No son secuenciales - se acceden según necesidad.

---

### **Archivos Raíz:**

```
empieza-aqui.md               (punto entrada - no numerado porque es único)
leeme.md                      (README - no numerado porque es único)
cuestionario-mike.html        (cuestionario - no numerado porque es único)
convencion-nombres.md         (este archivo - no numerado porque es único)
```

---

## 📖 EJEMPLOS POR CARPETA

### **02-plan-negocio/ (PERFECTO - modelo a seguir):**

```
00-indice.md                          ✅ Índice primero
01-analisis-mercado.md                ✅ Secuencial
02-modelo-negocio.md                  ✅ Secuencial
03-plan-financiero.md                 ✅ Secuencial
04-plan-operaciones.md                ✅ Secuencial
05-marco-legal-regulatorio.md         ✅ Secuencial
06-plan-marketing.md                  ✅ Secuencial
07-analisis-riesgos.md                ✅ Secuencial
08-cronograma-implementacion.md       ✅ Secuencial
modelo-negocio-resumen.md             ✅ Resumen sin número (consulta)
estructuras-docs.md                   ✅ Estructura sin número (referencia)
```

**Razón:** Es lectura secuencial - números guían el orden.

---

### **implementation/ (CORRECTO - sin números):**

```
inicio-rapido.md                      ✅ Sin número (usuario elige orden)
semana-1-plan.md                      ✅ Sin número (acción específica)
lista-compras.md                      ✅ Sin número (herramienta)
leeme.md                              ✅ Sin número (índice)
```

**Razón:** Son archivos de acción - no hay secuencia obligatoria.

---

### **01-investigacion/financiero/ (CORRECTO - numerados):**

```
01-tarifas-profesionales-akyfpy-2025.md    ✅ Prioridad 1
02-equipamiento-precios-seakit.md          ✅ Prioridad 2
```

**Razón:** Orden de consulta recomendado.

---

## 🔄 MANTENIMIENTO

### **Al agregar archivos nuevos:**

1. **Pregúntate:** ¿Este archivo tiene secuencia lógica con otros?
   - **SÍ** → Numerar (01-, 02-, 03-...)
   - **NO** → No numerar

2. **Si numeras:**
   - Usa 2 dígitos: `01-`, no `1-`
   - Manténlo secuencial: sin brechas
   - Índice siempre `00-`

3. **Si no numeras:**
   - Nombre descriptivo
   - español-kebab-case
   - Sin prefijo numérico

---

### **Al reorganizar:**

1. **Si eliminas archivo numerado:**
   - Renumerar los siguientes para cerrar brecha
   - O documentar la brecha como intencional

2. **Si cambias orden:**
   - Renumerar todos los afectados
   - Verificar referencias en otros archivos

---

## ❓ PREGUNTAS FRECUENTES

### **P: ¿Por qué español y no inglés?**
R: Mike es paraguayo, el negocio es en Paraguay, los clientes hablan español. El idioma debe reflejar el contexto.

### **P: ¿Por qué guiones (-) y no guiones bajos (_)?**
R: Los guiones son más legibles y son el estándar web (URLs). Los guiones bajos se ven como una sola palabra en algunos editores.

### **P: ¿Por qué minúsculas y no MAYÚSCULAS?**
R: Más fácil de escribir (sin Shift), mejor para URLs, estándar moderno. MAYÚSCULAS parecen gritar.

### **P: ¿Está bien tener brechas en la numeración?**
R: Funcionalmente sí, visualmente no ideal. Si son pocas (1-2) déjalas. Si son muchas (5+) considera renumerar.

### **P: ¿Puedo usar números en medio del nombre?**
R: Sí, si son parte del contenido: `datos-paraguay-2025.md`, `sesion-18-ene-2026.md`

### **P: ¿Cómo nombrar versiones?**
R: No uses sufijos -v1, -v2. Usa control de versiones (git) o fechas: `plan-2026-01-15.md`

### **P: ¿README.md está permitido?**
R: Preferimos `leeme.md` (español), pero `README.md` es aceptable en carpetas técnicas (convención universal).

---

## ✅ CHECKLIST DE VERIFICACIÓN

Antes de crear/renombrar archivo, verifica:

```
□ ¿Está todo en minúsculas?
□ ¿Está en español (o es término técnico universal)?
□ ¿Usa guiones (-) y no guiones bajos (_)?
□ ¿No tiene espacios?
□ ¿Si tiene número, usa 2 dígitos (01-, no 1-)?
□ ¿El número refleja secuencia real, no arbitrario?
□ ¿El nombre es descriptivo (no genérico)?
```

Si respondes SÍ a todo → ✅ Nombre correcto

---

## 📞 REFERENCIA RÁPIDA

### **Formato Estándar:**
```
[número opcional]-[descripción-en-español].md

Ejemplos:
✅ 01-analisis-mercado.md
✅ datos-paraguay-2025.md
✅ investigacion-nichos-resumen.md
```

### **Carpetas:**
```
[número opcional]-[descripción-en-español]/

Ejemplos:
✅ 01-investigacion/
✅ implementation/
✅ archivo-viejo/
```

---

## 🎯 RESUMEN EJECUTIVO

**3 reglas de oro:**

1. **español-kebab-case** (español, minúsculas, guiones)
2. **Numerar solo lo secuencial** (lectura ordenada, fases)
3. **Descriptivo > genérico** (analisis-mercado.md > documento1.md)

**Sigue estas reglas → 100% consistencia → fácil mantener**

---

**Creado:** 18 Enero 2026  
**Versión:** 2.0 (incluye reglas de numeración)  
**Estado:** Estándar oficial activo  
**Compliance actual:** 100% ✅

---

**Este documento es la fuente de verdad para naming en este proyecto.**
