# 📊 Fase 1 – Comprensión del Negocio (CRISP-DM)

**Proyecto:** Análisis de datos NNA_TI  
**Equipo:** Yeimy Alarcón, Ricardo Vargas, María José Galindo  
**Fecha:** Octubre 2025  

---

## 1. Determinación de objetivos de negocio

### Contexto
La base de datos **NNA_TI** contiene información proveniente de fichas de intervención y seguimiento a niños, niñas y adolescentes en diferentes localidades de **Bogotá**.  
El propósito de este proyecto es **identificar patrones, riesgos y oportunidades de mejora en la atención**.

### Objetivo principal
Evaluar la calidad, cobertura y características de las intervenciones realizadas a niños, niñas y adolescentes de las localidades de Bogotá.

### Objetivos específicos
- Analizar la distribución de las variables demográficas y contextuales.  
- Identificar problemas de calidad en la recolección de datos (datos faltantes o inconsistencias).  
- Generar reportes visuales y tabulares para apoyar la toma de decisiones de las entidades responsables.  

### Criterios de éxito de negocio
- Disponer de un sistema de reportes claros y reproducibles que permitan:  
  - Detectar vacíos de información en variables críticas.  
  - Presentar indicadores descriptivos confiables.  
  - Facilitar comparaciones entre localidades, perfiles y tipos de intervención.  

---

## 2. Evaluación de la situación

### Inventario de recursos
- **Personal:** 3 analistas de datos (equipo del proyecto) + profesor guía.  
- **Datos:** Base Excel `base_datos_completa_NNA_TI_anon.xlsx` con 56.474 registros y 115 variables. Incluye un diccionario de variables en la hoja `variables`.  
- **Software:** Python (Pandas, Matplotlib, Seaborn), Visual Studio Code, Google Colab.  
- **Hardware:** Codespaces de GitHub y computadores personales.  

### Riesgos y contingencias
- **Riesgo:** Alta proporción de datos vacíos o mal diligenciados en variables clave.  
  - **Contingencia:** Documentar y excluir variables no confiables, aplicar análisis solo a variables con consistencia mínima.  
- **Riesgo:** Complejidad del diccionario (más de 100 variables).  
  - **Contingencia:** Priorización de grupos de variables (demografía, educación, intervención, riesgos).  

### Terminología
- **NNA:** Niños, Niñas y Adolescentes.  
- **TI:** Tipo de Intervención.  
- **Ficha_fic:** Identificador único de cada registro.  
- **PQR:** Peticiones, Quejas y Reclamos.  

---

## 3. Determinación de los objetivos de minería de datos

### Objetivos de minería de datos
Construir un proceso automatizado de comprensión de datos que genere:  
- Diccionario de variables (tipos, vacíos).  
- Reportes tabulares y gráficos de variables numéricas y categóricas.  
- Matriz de correlaciones y distribución de datos faltantes.  
- Resúmenes por grupos temáticos (demografía, educación, riesgos, intervención).  

### Criterios de éxito de minería de datos
- Reportes exportados en formato `.csv` y gráficos en `.png` dentro de la carpeta `reports/`.  
- Ejecución reproducible del script en cualquier entorno Python.  
- Identificación explícita de variables con:  
  - Alta proporción de datos faltantes.  
  - Duplicados.  

---

## 4. Plan del proyecto

### Etapas del proceso
1. **Comprensión del negocio** Incluye el contexto, los objetivos y los recursos que vamos a manejar en el proyecto..  
2. **Comprensión de los datos:** exploración inicial de la base de datos, diccionario, problemas de calidad.  
3. **Preparación de datos:** limpieza: selección de variables, tratamiento de valores faltantes .  
4. **Modelado:** técnicas estadísticas para describir y comparar los datos. 
5. **Evaluación:** validación de resultados frente a objetivos de negocio.  
6. **Despliegue:** entrega de reportes en GitHub: reportes en CSV y gráficos en PNG

### Evaluación inicial de herramientas y técnicas
- Para el análisis haremos uso de Python, ofrece librerías adecuadas para análisis exploratorio (**Pandas, Seaborn, Matplotlib**).  
- GitHub permite reproducibilidad y control de versiones.  

---
