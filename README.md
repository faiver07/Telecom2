# 📊 Análisis de Deserción de Clientes - TELECOM X

## 📋 Descripción del Proyecto

Este proyecto analiza la deserción de clientes (churn) de la empresa TELECOM X mediante técnicas de análisis de datos y machine learning. El objetivo es identificar los factores que influyen en la cancelación de servicios y desarrollar estrategias para mejorar la retención de clientes.

---

## 🎯 Objetivos

- **Objetivo Principal:** Analizar la evasión de clientes de TELECOM X mediante análisis de datos.
- **Objetivos Específicos:**
    - Realizar procesos de ETL (Extracción, Transformación y Carga).
    - Ejecutar un Análisis Exploratorio de Datos (EDA) completo.
    - Desarrollar modelos predictivos para identificar clientes en riesgo de deserción.

---

## 📊 Dataset

**Fuente:** [TelecomX_Data.json](https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/main/TelecomX_Data.json)

- **Registros:** 7,267 clientes
- **Variables:** 21 columnas
- **Tasa de Churn:** 26.5%

### 📝 Diccionario de Variables

**Información del Cliente**
- `customerID`: Identificador único del cliente
- `gender`: Género (masculino/femenino)
- `SeniorCitizen`: Cliente mayor de 65 años (Sí/No)
- `Partner`: Tiene pareja (Sí/No)
- `Dependents`: Tiene dependientes (Sí/No)
- `tenure`: Meses de contrato

**Servicios de Telefonía**
- `PhoneService`: Suscripción al servicio telefónico
- `MultipleLines`: Múltiples líneas telefónicas

**Servicios de Internet**
- `InternetService`: Tipo de proveedor (DSL, Fibra óptica, No)
- `OnlineSecurity`: Seguridad en línea
- `OnlineBackup`: Respaldo en línea
- `DeviceProtection`: Protección de dispositivos
- `TechSupport`: Soporte técnico
- `StreamingTV`: Televisión por streaming
- `StreamingMovies`: Películas por streaming

**Información de Cuenta**
- `Contract`: Tipo de contrato (Mes a mes, 1 año, 2 años)
- `PaperlessBilling`: Facturación sin papel
- `PaymentMethod`: Método de pago
- `Charges.Monthly`: Cargos mensuales
- `Charges.Total`: Cargos totales

---

## 🔧 Metodología

1. **ETL (Extract, Transform, Load)**
    - Extracción de datos desde URL JSON
    - Limpieza y transformación de tipos de datos
    - Manejo de valores nulos y duplicados
    - Creación de variables derivadas

2. **Análisis Exploratorio de Datos (EDA)**
    - Análisis univariado y bivariado
    - Segmentación por tipo de servicio (solo teléfono, solo internet, ambos)

3. **Modelado Predictivo**
    - Random Forest (modelo principal, optimización de hiperparámetros)
    - Regresión Logística (modelo complementario con SMOTE)
    - Validación cruzada y métricas de evaluación

---

## 📈 Resultados Principales

### 🎯 Hallazgos Importantes

- **El 26.5% de los clientes desertan de la empresa**, siendo la tasa de churn un reto relevante para la sostenibilidad del negocio.
- **El segmento más crítico** son los clientes que tienen ambos servicios (teléfono e internet), representando el 22.6% de la deserción total.
- **La mayoría de los clientes** tiene contratos mes a mes, lo que implica menor lealtad y mayor riesgo de churn.
- **Los clientes con cargos mensuales altos y menor antigüedad** presentan mayor probabilidad de cancelar los servicios.
- **La ausencia de servicios adicionales de internet** (seguridad, soporte técnico, respaldo, protección de dispositivos) incrementa significativamente la probabilidad de churn.
- **El método de pago electrónico y la facturación sin papel** están asociados a una mayor tasa de deserción.
- **Factores demográficos** como no tener pareja, no tener dependientes y ser menor de 65 años aumentan el riesgo de churn.
- **El género no es un factor determinante** en la deserción de clientes.

### 🎯 Factores de Riesgo Identificados

**Demográficos**
- Sin pareja: 14% vs 8% con pareja
- Sin dependientes: 18% vs 3.9% con dependientes
- Menores de 65 años: 16.5% vs 6.1% mayores de 65

**Servicios**
- Sin seguridad online: 18.8% de deserción
- Sin soporte técnico: 18.5% de deserción
- Sin respaldo online: 15% de deserción
- Sin protección de dispositivos: 15.5% de deserción

**Contractuales**
- Contratos mes a mes: Mayor riesgo de deserción
- Pago electrónico: Factor de riesgo
- Facturación sin papel: 17.6% vs 4.9% con papel

**Económicos**
- Menor antigüedad: Correlación con mayor deserción
- Cargos totales bajos: Indicador de riesgo

### 🤖 Rendimiento del Modelo

- **Random Forest (Modelo Principal):**
    - AUC-ROC: 0.85+ (excelente capacidad predictiva)
    - Precisión: Balanceada entre clases
    - Variables más importantes: Antigüedad, cargos mensuales, tipo de contrato

---

## 🛠️ Tecnologías Utilizadas

- pandas, numpy, matplotlib, seaborn
- scikit-learn, tensorflow, imblearn
- requests, json

---

## 🚀 Cómo Ejecutar

1. **Instalar dependencias**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn tensorflow imblearn requests
    ```

2. **Ejecutar el análisis**
    ```bash
    python aluratelecom.py
    ```

---

## 📊 Visualizaciones Incluidas

- Distribuciones de variables por churn
- Análisis de correlaciones
- Gráficos de importancia de características
- Curvas ROC y Precision-Recall
- Análisis por segmentos de servicio

---

## 🎯 Recomendaciones Estratégicas

1. Focalizar en clientes con ambos servicios (22.6% de deserción)
2. Promover servicios adicionales de internet (seguridad, soporte, respaldo)
3. Incentivar contratos a largo plazo vs mes a mes
4. Programa de retención para clientes nuevos (< 12 meses)
5. Revisar estrategia de precios para cargos altos

---

## 👨‍💻 Autor

- [Tu nombre]
- GitHub: [tu-github]
- LinkedIn: [tu-linkedin]

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo LICENSE para más detalles.

---

⭐ Si este proyecto te fue útil, ¡no olvides darle una estrella!
