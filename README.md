# 📊 Fase 1 – Comprensión del Negocio (CRISP-DM)

**Proyecto:** Análisis de datos NNA_TI  
**Equipo:** Yeimy Alarcón, Ricardo Vargas, María José Galindo  
**Fecha:** Octubre 2025  

---

# Análisis Exploratorio de la Base de Datos NNA-TI

**Proyecto:** Relación de niños, niñas y adolescentes con el mercado laboral  
**Metodología:** CRISP-DM (fases de Entendimiento y Preparación de Datos)  
**Base:** `base_datos_completa_NNA_TI_anon`  
**Autoría:** Universidad Santo Tomás – Facultad de Estadística  

---

## 📘 Contexto general

Este proyecto se enmarca dentro del análisis de datos de **niños, niñas y adolescentes (NNA)** con posibles situaciones de **trabajo infantil o adolescente**, aplicando de manera parcial la metodología **CRISP-DM**.  
El propósito central es comprender, limpiar y estructurar la base de datos para realizar un **análisis exploratorio descriptivo** que permita identificar patrones demográficos, socioeconómicos y laborales asociados al estado del resultado de la intervención.

---

## 🎯 Objetivo general

Realizar un **análisis exploratorio** de la base `base_datos_completa_NNA_TI_anon` para **limpiar, organizar y describir** la información de niños, niñas y adolescentes con posibles situaciones de trabajo infantil o adolescente, **resumiendo patrones básicos** por **demografía, ubicación, afiliación al SGSSS y lugar principal de trabajo**, mediante **tablas y visualizaciones descriptivas**, **aplicando las fases de entendimiento y preparación de datos** de la metodología **CRISP-DM**.

---

## 🧮 Objetivos específicos

1. **Comprender la estructura y contenido del conjunto de datos `base_datos_completa_NNA_TI_anon`**, identificando las variables relevantes, sus tipos y su relación con el fenómeno del trabajo infantil/adolescente.  
2. **Evaluar la calidad de la información**, detectando valores faltantes, inconsistencias y categorías no especificadas que puedan afectar la interpretación estadística de los resultados.  
3. **Aplicar procesos de limpieza, estandarización y creación de variables derivadas**, con el fin de mejorar la organización, trazabilidad y coherencia del conjunto de datos para el análisis posterior.  
4. **Organizar las variables en grupos temáticos lógicos** (demografía, ubicación, trabajo, salud y resultado), facilitando la interpretación y visualización de la información.  
5. **Desarrollar un análisis exploratorio descriptivo**, utilizando medidas estadísticas, tablas y visualizaciones que permitan identificar patrones generales y relaciones entre las variables demográficas, socioeconómicas y laborales con el estado del resultado de la intervención.

---

## 🧩 Momentos del análisis

- **Configuración y carga de datos.**  
- **Estandarización de nombres de columna.**  
- **Eliminación de información personal (PII).**  
- **Limpieza de inconsistencias.**  
- **Identificación de valores faltantes.**  
- **Creación de variables derivadas.**  
- **Estructuración por grupos temáticos.**  
- **Exportación de resultados y generación de visualizaciones.**

---

## 📊 Variables derivadas

Se crearon **9 variables nuevas** basadas en la lógica del negocio y la necesidad de análisis, manteniendo etiquetas claras y canónicas, tales como:

- `RANGO_EDAD`  
- `ZONA_LABEL`  
- `SEXO_LABEL`  
- `ESTRATO_SOCIOECONOMICO_LABEL`  
- `LUGAR_TRABAJO_LABEL`  
- `AFILIACION_AL_SGSSS_LABEL`  
- `FLAG_AFILIACION_SGSSS`  
- `ESTADO_RESULTADO`  
- `UPZ_UPR_ALIAS`

Estas variables facilitan el análisis y las visualizaciones relacionadas con el fenómeno de estudio.

---

## 🗂️ Estructuración del dataset final

Las columnas del dataset final (`df_final`) se reordenaron en **grupos temáticos lógicos**:

- **Metadata**  
- **Ubicación**  
- **Demografía**  
- **Trabajo**  
- **Salud**  
- **Resultado**

---

## 📈 Visualizaciones principales

El análisis descriptivo se centró en la variable **ESTADO_RESULTADO**, explorando las siguientes dimensiones:

- **RANGO_EDAD:** Diferencias notables en el porcentaje de desvinculación según edad.  
- **ESTRATO_SOCIOECONÓMICO:** Los estratos bajos y “No especificado” muestran mayor desvinculación.  
- **LOCALIDAD:** Variaciones significativas entre localidades; Usme, Suba y Engativá presentan valores más altos.  
- **SEXO:** Similitud entre hombres y mujeres, pero mayor desvinculación en la categoría “No especificado”.  
- **AFILIACIÓN_AL_SGSSS:** El régimen contributivo muestra un porcentaje mayor de desvinculación.  
- **LUGAR_TRABAJO:** Espacios como “UTI” o “calle” presentan los niveles más altos de desvinculación.

**Conclusión general:**  
Las variables demográficas y geográficas presentan patrones diferenciados en el estado de resultado, con categorías “No especificado” que sugieren problemas de calidad o de registro en los datos.

---

## ✅ Criterios de éxito

1. **Documentación estructurada del conjunto de datos:**  
   Diccionario de variables y descripción clara de la base `base_datos_completa_NNA_TI_anon`.  

2. **Evaluación de calidad de datos completada:**  
   Reporte con tasas de valores faltantes, registros inconsistentes y categorías no especificadas.  

3. **Base depurada y estandarizada:**  
   Dataset limpio, con variables derivadas correctamente creadas y nombres homogéneos.  

4. **Estructura temática validada:**  
   Variables agrupadas coherentemente por categorías (Demografía, Ubicación, Trabajo, Salud, Resultado).  

5. **Análisis exploratorio reproducible:**  
   Gráficos, tablas y estadísticas descriptivas reproducibles mediante scripts en Python o R.  

6. **Comunicación clara de resultados:**  
   Presentación final con interpretación descriptiva, hallazgos principales y visualizaciones interpretadas.

---

## 📚 Referencia metodológica

Metodología **CRISP-DM (Cross-Industry Standard Process for Data Mining)** – se implementaron las fases de:
- **Entendimiento de los datos**
- **Preparación de los datos**

*(No se incluyen modelado ni despliegue, dado el carácter exploratorio y descriptivo del análisis.)*

---

# 📊 Momentos del Análisis

En esta sección se describen los principales pasos desarrollados durante el proceso de **entendimiento y preparación de datos**, aplicando las fases iniciales de la metodología **CRISP-DM**.

---

## 1. Configuración y carga de datos

Se realizó la configuración del entorno de trabajo y la carga de la base principal:

**Base:** `NNA Trabajo Infantil/Adolescente`  
**Registros:** 56,473  
**Columnas:** 115  

<img width="565" height="186" alt="image" src="https://github.com/user-attachments/assets/ecdb0a04-a743-4723-b93c-9f07f5acb210" />

---

## 2. Estandarización de nombres de columna

Se aplicó un proceso de **normalización de los nombres de las variables**, ajustándolos a un formato canónico (`snake_case`) y removiendo acentos, espacios y caracteres especiales.  
Esto asegura la compatibilidad del dataset con las herramientas de análisis y programación.

---

## 3. Eliminación de información personal

Se identificaron y **eliminaron 10 columnas** con información personal identificable (PII), con el fin de proteger la privacidad de los NNA y cumplir con principios de anonimización de datos.

**Columnas eliminadas:**
- `ID_FIC`
- `FICHA_FIC`
- `NUMERO_DE_FICHA_ANTERIOR`
- `USUARIO`
- `DIRECCION_DE_LA_VIVIENDA`
- `DIRECCION_DEL_TRABAJO`
- `TELEFONO_1`
- `TELEFONO_2`
- `CORREO_1`
- `CORREO_2`

**Resultado:**  
`Dataset seguro: 56,473 registros × 105 columnas`

<img width="563" height="271" alt="image" src="https://github.com/user-attachments/assets/e0831429-1138-4ffc-93e5-fe5984d6a4ba" />

---

## 4. Limpieza de inconsistencias

Se detectaron y corrigieron errores tipográficos, duplicados y valores no válidos en variables clave (edad, sexo, estrato, localidad, entre otras).  
Además, se verificó la coherencia entre variables categóricas relacionadas.

---

## 5. Identificación de valores faltantes

Se evaluó la **proporción de datos faltantes** en todas las variables.  
El gráfico siguiente muestra las **15 variables con mayor porcentaje de valores faltantes**.

<img width="577" height="369" alt="image" src="https://github.com/user-attachments/assets/e18c372d-f268-4a6e-b56e-3d4fa1e06016" />


📝 **Interpretación:**
Las variables con mayor porcentaje de faltantes corresponden principalmente a secciones relacionadas con la intervención, acompañamiento y características del acudiente, lo cual sugiere posibles vacíos de registro o diferencias entre fuentes.

---

## 6. Variables derivadas

Se crearon **9 variables nuevas** basadas en la lógica del negocio y la necesidad de análisis, manteniendo etiquetas claras y canónicas.

| Variable | Descripción |
|-----------|-------------|
| `RANGO_EDAD` | Agrupa edades en rangos (0–5, 6–11, etc.) |
| `ZONA_LABEL` | Etiquetas de zona (Urbana, Rural, Periurbana) |
| `SEXO_LABEL` | Etiquetas para sexo (Hombre, Mujer, Intersexual) |
| `ESTRATO_SOCIOECONOMICO_LABEL` | Nivel socioeconómico |
| `LUGAR_TRABAJO_LABEL` | Lugar donde trabaja la persona |
| `AFILIACION_AL_SGSSS_LABEL` + `FLAG_AFILIACION_SGSSS` | Afiliación a salud con indicador binario |
| `ESTADO_RESULTADO` | Estado laboral (Desvinculado / Trabajo protegido / En proceso) |
| `UPZ_UPR_ALIAS` | Copia de variable geográfica |

Estas variables facilitan la organización, visualización y análisis de patrones dentro del dataset.

---

## 7. Estructuración del dataset final

Las columnas del dataset final (`df_final`) se reorganizaron en **grupos temáticos lógicos** para mejorar la interpretación y trazabilidad del análisis.

| Grupo | Descripción |
|--------|-------------|
| `METADATA` | Información de origen y contexto |
| `UBICACION` | Datos geográficos y espaciales |
| `DEMOGRAFIA` | Características personales |
| `TRABAJO` | Información laboral |
| `SALUD` | Datos de afiliación al sistema de salud |
| `RESULTADO` | Estado final del caso |

---

---

## 9. Visualizaciones

Se realizaron diversas visualizaciones descriptivas orientadas al **Estado del Resultado**, con enfoque en variables como:

- Rango de edad  
- Estrato socioeconómico  
- Localidad  
- Sexo  
- Afiliación al SGSSS  
- Lugar principal de trabajo  

# 📊 Visualizaciones generales  
### Relacionado con segmentación demográfica y geográfica

### 🖼️ Distribuciones básicas

<img width="898" height="557" alt="image" src="https://github.com/user-attachments/assets/a182aa50-d443-4805-af69-bd3d7016e3d9" />

---

### Distribución: Rango de Edad
La mayor parte de los registros se concentra en los grupos **6–11 años** y **0–5 años**.  
El grupo **12–14 años** y **15–17 años** representan una proporción menor, mientras que la categoría *no especificada* es considerablemente alta, lo que indica la necesidad de revisar la completitud de esta variable.

---

### Distribución: Sexo
El **40,6 %** de los casos corresponde a **hombres**, el **30,6 %** a **mujeres**, y el **19,8 %** se encuentra *no especificado*.  
Este porcentaje elevado de “No especificado” puede reflejar problemas de registro o falta de estandarización en la variable de sexo.

---

### Distribución: Estrato Socioeconómico
Predominan los estratos **2 (Bajo)** y **3 (Medio-bajo)**, mientras que el **estrato 1 (Bajo-bajo)** y las categorías *No especificado* también presentan un número considerable de registros.  
Esta distribución sugiere que la mayoría de los NNA pertenecen a hogares de niveles socioeconómicos bajos.

---

### Distribución: Afiliación al SGSSS
El régimen **Subsidiado** es el más frecuente, seguido del **Contributivo**, mientras que las categorías *No especificado* y *No asegurado* también tienen una presencia notable.  
Esto refleja la cobertura mixta del sistema de salud entre los NNA y evidencia posibles brechas en el acceso o registro.

---

### Distribución: Estado de Resultado
La categoría **Desvinculado** concentra la mayor proporción de casos, seguida de **En proceso/Sin cambio**, y en menor medida **Trabajo protegido**.  
Esta tendencia muestra que la mayoría de los NNA han sido desvinculados del trabajo infantil, aunque aún existe un grupo relevante en seguimiento o sin cambios reportados.

---
## 📊 Visualizaciones generales: relacionado con segmentación demográfica y geográfica

En esta sección se presentan las principales **visualizaciones descriptivas** relacionadas con la segmentación **demográfica y geográfica** del conjunto de datos `base_datos_completa_NNA_TI_anon`.  
Estas permiten comprender cómo se distribuyen las intervenciones y características de los NNA en el territorio y en distintas dimensiones socioeconómicas.

---

### Gráfico 1: UPZ/UPR (Top 12 por frecuencia)

<img width="817" height="408" alt="image" src="https://github.com/user-attachments/assets/cbc57177-6cfb-43ed-a5fc-36db24668b9a" />


**Descripción:**  
El gráfico muestra las **12 UPZ o UPR con mayor número de registros** en la base de datos.  
Las zonas con más frecuencia indican **mayor concentración de NNA vinculados o atendidos**, lo que sugiere territorios con mayor presencia de casos o focalización de intervenciones.

---

### Gráfico 2: Lugar principal de trabajo

<img width="687" height="407" alt="image" src="https://github.com/user-attachments/assets/03b89437-cf91-4954-8d7a-44ae7b4c75b2" />


**Descripción:**  
Se observa que la mayoría de los NNA reportan trabajar **“en una UTI”** o **“en la calle, estacionario o ambulante”**.  
La categoría *No especificado* también es elevada, lo que indica vacíos de información.  
Estos resultados permiten identificar los contextos laborales más comunes y su potencial vulnerabilidad.

---

### Gráfico 3: Afiliación al SGSSS (%) por Localidad

<img width="757" height="412" alt="image" src="https://github.com/user-attachments/assets/e26ef0a6-bf00-425b-8735-e18377554f9b" />


**Descripción:**  
El mapa de calor muestra la **proporción de afiliaciones al SGSSS** por localidad.  
Predominan los regímenes **Subsidiado** y **Contributivo**, aunque hay variaciones significativas entre localidades.  
Algunas zonas (como Engativá o Suba) tienen mayor cobertura, mientras que otras presentan valores altos de *No especificado* o *No asegurado*.

---

### Gráfico 4: Lugar de trabajo (%) por Localidad

<img width="758" height="410" alt="image" src="https://github.com/user-attachments/assets/321137d4-7269-4b3e-8df3-d3ea900685cd" />


**Descripción:**  
Este gráfico relaciona el **lugar principal de trabajo** con la **localidad** de residencia.  
Se identifican diferencias marcadas: algunas localidades concentran más trabajo en UTI o en vía pública, mientras que otras presentan mayor registro de actividades en vivienda.  
Esto sugiere que el tipo de entorno laboral varía según el territorio y su contexto socioeconómico.

---

## 📈 Visualizaciones relacionadas con el Estado de Resultado

En esta sección se presentan las relaciones entre el **Estado de Resultado** y diferentes variables demográficas, socioeconómicas y contextuales.  
Cada visualización permite identificar patrones en el porcentaje de desvinculación y otras categorías del estado final del caso.

---

### RANGO_EDAD

<img width="645" height="408" alt="image" src="https://github.com/user-attachments/assets/7ea323c7-0206-4aab-b115-19534e2b17db" />


**Interpretación:**  
Observamos diferencias notables en el porcentaje de desvinculación según el rango de edad.  
Los rangos de edad más jóvenes (**0–5** y **6–11**) parecen tener un porcentaje de desvinculación ligeramente menor en comparación con los adolescentes (**12–14** y **15–17**).  
La categoría *No especificado* en edad presenta un porcentaje de desvinculación significativamente mayor, lo que podría indicar un sesgo en los datos o la necesidad de investigar más a fondo estos casos.

---

### ESTRATO_SOCIOECONÓMICO

<img width="712" height="436" alt="image" src="https://github.com/user-attachments/assets/fab9f5ff-d96b-4fac-8435-bde3804db24e" />


**Interpretación:**  
El estrato *No especificado* presenta el porcentaje más alto de desvinculación.  
Entre los estratos definidos, el estrato **2. Bajo** tiene un porcentaje de desvinculación ligeramente superior a los estratos **1. Bajo-bajo** y **3. Medio-bajo**.  
Esto sugiere que los hogares en niveles bajos concentran más casos atendidos o con seguimiento, posiblemente asociados a condiciones socioeconómicas más vulnerables.

---

### LOCALIDAD

<img width="676" height="426" alt="image" src="https://github.com/user-attachments/assets/dee0dda8-01f0-4756-9f17-fdcc44083ae7" />


**Interpretación:**  
El porcentaje de NNA desvinculados varía considerablemente entre localidades.  
Algunas localidades como **Usme, Suba y Engativá** muestran porcentajes de desvinculación más altos entre las top 15 localidades con más registros, mientras que otras como **Ciudad Bolívar** y **Antonio Nariño** tienen porcentajes más bajos.  
Esto sugiere que la ubicación geográfica es un factor importante y que las estrategias de intervención podrían ajustarse a las particularidades de cada zona.  
La categoría *99999* (localidad no especificada) presenta un porcentaje de desvinculación muy bajo, lo que refuerza la idea de que corresponde a datos atípicos o registros no georreferenciados.

---

### SEXO

<img width="631" height="373" alt="image" src="https://github.com/user-attachments/assets/5e357215-3872-4499-9f6d-aa23330d8bf3" />


**Interpretación:**  
Los porcentajes de desvinculación y *En proceso/Sin cambio* son similares entre hombres y mujeres.  
La categoría *No especificado* en sexo tiene un porcentaje de desvinculación notablemente más alto, similar a lo observado en la variable *Rango de Edad* en su categoría *No especificado*.  
Esto sugiere posibles inconsistencias en el registro que podrían afectar la interpretación del estado final.

---

### AFILIACIÓN_AL_SGSSS

<img width="633" height="375" alt="image" src="https://github.com/user-attachments/assets/2a568027-2bff-41bd-b7dd-6e877bf5a37b" />

**Interpretación:**  
Los NNA afiliados al régimen **Contributivo** muestran un porcentaje de desvinculación más alto en comparación con otros regímenes como el **Subsidiado** o **No asegurado**.  
Este hallazgo resulta interesante para explorar las razones detrás de esta diferencia, que podrían estar relacionadas con el acceso a servicios, condiciones laborales o características familiares.  
La categoría *No especificado* también presenta un porcentaje de desvinculación relativamente alto.

---

### LUGAR_TRABAJO

<img width="685" height="415" alt="image" src="https://github.com/user-attachments/assets/16279aa1-9271-441d-a789-87a3757f8005" />


**Interpretación:**  
El porcentaje de desvinculación varía según el lugar principal de trabajo.  
Lugares como **“En una UTI”** y **“En la calle, estacionario o ambulante”**, que concentran un alto número de casos, muestran porcentajes de desvinculación por encima del promedio general.  
Los casos con *No especificado* en el lugar de trabajo también presentan un alto porcentaje de desvinculación, lo cual podría reflejar problemas de registro o clasificación.

---

 **Conclusión general:**  
En resumen, los análisis sugieren que tanto las variables demográficas (edad, sexo - especialmente en categorías no especificadas) como las geográficas (localidad) y socioeconómicas (estrato, afiliación a salud, lugar de trabajo) están relacionadas con el estado del resultado de la intervención. Las categorías "No especificado" en varias variables presentan un comportamiento atípico con porcentajes de desvinculación más altos, lo que justifica una revisión de la calidad o el significado de estos datos.


