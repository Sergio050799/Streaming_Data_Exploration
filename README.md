# Streaming_Data_Exploration

---

## **Premisa Empresarial**
Una productora nos ha solicitado evaluar la viabilidad de asociarse con una plataforma de streaming para la distribución de su contenido audiovisual.  
Dado el extenso abanico de opciones disponibles en el mercado, tales como **Netflix**, **Prime Video**, **Disney+**, **Apple TV** y **HBO Max**, resulta crucial recopilar y analizar información relevante de estas plataformas.  
Este análisis será fundamental para tomar una decisión informada y estratégica que optimice los intereses de la productora.

---

## **1. Recopilación de Datos**

### **1.1 Fuentes de Datos**
- **Kaggle**: 
  - Datos obtenidos del usuario OctopusTeam, que contenían información actualizada de múltiples plataformas.  
  - Las columnas principales incluyeron:
    - `Title`, `Type`, `Genres`, `ReleaseYear`, `imdbId`, `imdbAverageRating`, `imdbNumVotes`, `Available Countries`.
- **Fuentes externas**:
  - Información adicional recopilada de **Huffington Post**, **El País**, **Xataka** y **El Diario**.  

### **1.2 Archivos CSV**
1. **Toda_Data**:
   - Información principal sobre títulos, géneros, calificaciones de IMDb, países disponibles, entre otros.
2. **Precios**:
   - Información sobre precios, características de los planes de suscripción y días de prueba.
3. **Suscriptores**:
   - Datos de suscriptores por región y continentes disponibles.

---

## **2. Limpieza de Datos**

### **2.1 Limpieza y Transformación de `Toda_Data`**
- **Añadimos columna**: `Plataforma`.
- **Eliminación de valores nulos** en columnas clave como calificaciones y votos.
- **Eliminación de títulos duplicados**.
- **Imputación de valores faltantes**:
  - Calificación promedio y número de votos se llenaron utilizando la mediana de la plataforma.
- **Concatenación de continentes** en función de los países disponibles.
- **Filtrado de años irrelevantes**: Eliminamos datos de años futuros a 2024 y anteriores a 2015.

### **2.2 Limpieza de `Precios` y `Suscriptores`**
- **Transformación de formato**: Estandarizamos las columnas y valores.
- **Asignación de valores faltantes**.
- **Filtrado por años**: Se aplicaron los mismos criterios de año que en `Toda_Data`.

---

## **3. Análisis Exploratorio y Visualizaciones**

### **3.1 Distribución de Títulos por Plataforma**
- **Gráfico**: Dona.
- **Propósito**: Identificar la proporción de títulos disponibles en cada plataforma.
- **Conclusión**: Amazon Prime Video tiene la mayor cantidad de títulos (66.2%), pero esto no necesariamente implica mayor calidad.

### **3.2 Porcentaje de Suscriptores por Plataforma en los Continentes**
- **Gráfico**: Barras agrupadas.
- **Propósito**: Mostrar cómo se distribuyen los suscriptores en diferentes regiones.
- **Conclusión**: América y Asia son los mercados más relevantes, con Netflix y Amazon Prime Video liderando en cobertura global.

### **3.3 Número de Títulos por Plataforma**
- **Gráfico**: Barras.
- **Propósito**: Comparar la cantidad total de títulos entre las plataformas.
- **Conclusión**: Amazon Prime Video lidera con más de 30,000 títulos, mientras que Apple TV+ tiene la biblioteca más pequeña pero curada.

### **3.4 Proporción de Contenido por Tipo**
- **Gráfico**: Circular.
- **Propósito**: Mostrar la proporción entre películas y series.
- **Conclusión**: Las películas constituyen el 79.7% del contenido total.

### **3.5 Top 5 Géneros Más Consumidos por Plataforma**
- **Gráfico**: Barras horizontales apiladas.
- **Propósito**: Analizar qué géneros dominan en cada plataforma.
- **Conclusión**: Documentales y Drama son los géneros más populares.

### **3.6 Mapa de Correlación entre Variables**
- **Gráfico**: Heatmap.
- **Propósito**: Identificar relaciones entre variables como calificaciones, votos y años.
- **Conclusión**: No se observaron correlaciones significativas entre las variables analizadas.

### **3.7 Calificaciones Promedio y Consistencia**
- **Gráfico**: Diagramas de caja.
- **Propósito**: Mostrar la consistencia y dispersión de las calificaciones en IMDb por plataforma.
- **Conclusión**:
  - Netflix y HBO Max tienen mayor consistencia.
  - Amazon Prime Video presenta mayor variabilidad en calidad.

### **3.8 Días de Prueba por Plataforma**
- **Gráfico**: Barras.
- **Propósito**: Identificar las plataformas que ofrecen días de prueba gratuita y cuántos días ofrecen.
- **Conclusión**: Amazon Prime Video y Apple TV+ lideran en esta estrategia.

### **3.9 Precios y Versiones de las Plataformas**
- **Gráfico**: Barras agrupadas.
- **Propósito**: Analizar las opciones de precios y planes de suscripción ofrecidos por cada plataforma.
- **Conclusión**:
  - Netflix tiene la mayor diversificación de planes.
  - Amazon Prime Video es la opción más económica.

---

## **4. Recomendaciones Estratégicas**

1. **Asociarse con plataformas de alta cobertura global**: Netflix y Amazon Prime Video son ideales para maximizar el alcance.
2. **Diversificar contenido en géneros populares**: Drama y Documentales tienen alta demanda en todas las plataformas.
3. **Posicionar contenido de calidad en plataformas consistentes**: Netflix y HBO Max ofrecen bibliotecas percibidas como consistentemente buenas.
4. **Aprovechar mercados clave**: América y Asia representan los mayores mercados, con HBO Max y Amazon Prime Video liderando en estas regiones, respectivamente.
5. **Alinear estrategias con precios y accesibilidad**: Amazon Prime Video destaca por su economía, mientras que Netflix tiene opciones diversificadas para diferentes usuarios.
6. **Enfocarse en contenido reciente**: La alta producción de contenido desde 2016 ofrece oportunidades para capitalizar la tendencia.

---

Este análisis proporciona una base sólida para decisiones estratégicas y asegura que las fortalezas de cada plataforma estén alineadas con los objetivos de la productora.
