# **README: Análisis Predictivo para Telecom X 2**  

## **📌 Descripción del Proyecto**  
Este proyecto tiene como objetivo **predecir la evasión de clientes (Churn)** en una empresa de telecomunicaciones utilizando técnicas de machine learning. A través de un análisis exhaustivo de los datos, identificamos los factores clave que influyen en la cancelación de servicios y generamos estrategias de retención basadas en insights accionables.  

---

## **🎯 Objetivos**  
1. **Identificar** a los clientes con mayor riesgo de cancelación.  
2. **Determinar** las variables más influyentes en el comportamiento de Churn.  
3. **Proponer** estrategias de retención personalizadas.  
4. **Entregar** un modelo predictivo con métricas evaluadas.  

---

## **📊 Estructura del Repositorio**  
```bash
├── data/  
│   └── TelecomX_Data.json              # Dataset original  
├── notebooks/  
│   └── TelecomX_Churn_Analysis.ipynb   # Análisis y modelado  
├── outputs/  
│   ├── churn_high_risk_customers.csv   # Clientes de alto riesgo  
│   └── feature_importance.png          # Gráfico de importancia  
├── README.md                           # Este archivo  
└── requirements.txt                    # Dependencias  
```

---

## **🔍 Análisis Realizado**  

### **1. Preparación de Datos**  
- Eliminación de columnas irrelevantes (`customerID`).  
- Codificación de variables categóricas (`One-Hot Encoding`).  
- Estandarización de variables numéricas (`StandardScaler`).  

### **2. Exploración de Datos (EDA)**  
- **Proporción de Churn**: 26% "Sí" vs 74% "No" (dataset desbalanceado).  
- **Correlaciones clave**:  
  - `MonthlyCharges` (+) y `tenure` (-) son los predictores más fuertes.  
- **Visualizaciones**:  
  - Matriz de correlación.  
  - Distribución de Churn por tipo de contrato e Internet.  

### **3. Modelado Predictivo**  
- **Algoritmos utilizados**:  
  - `Random Forest` (Precisión: 82%, Recall: 70%).  
  - `Regresión Logística` (para comparación).  
- **Balanceo de clases**: SMOTE aplicado para mejorar la detección de Churn.  

### **4. Resultados Clave**  
- **Top 3 variables importantes**:  
  1. `MonthlyCharges` (25%).  
  2. `tenure` (20%).  
  3. `InternetService_Fiber optic` (15%).  
- **Perfil de alto riesgo**:  
  - Contrato mensual + Fibra óptica + Pago electrónico.  

---

## **🚀 Cómo Ejecutar el Proyecto**  

### **1. Instalación de Dependencias**  
```bash
pip install -r requirements.txt
```

### **2. Ejecución del Notebook**  
Abrir `TelecomX_Churn_Analysis.ipynb` en Google Colab o Jupyter Notebook.  

### **3. Pasos Clave en el Notebook**  
1. Cargar datos desde `data/TelecomX_Data.json`.  
2. Ejecutar todas las celdas para reproducir el análisis.  
3. Generar salvas en `outputs/` (ej: lista de clientes de alto riesgo).  

---

## **📈 Estrategias de Retención Propuestas**  
1. **Ofertas personalizadas**: Descuentos para clientes con fibra óptica y contrato mensual.  
2. **Programa de fidelización**: Beneficios por antigüedad (ej: mes gratis al cumplir 1 año).  
3. **Mejora en soporte técnico**: Asignar agentes dedicados a clientes con reclamos frecuentes.  

---

## **🛠️ Tecnologías Utilizadas**  
- **Lenguaje**: Python 3.9+.  
- **Librerías**:  
  - `Pandas` (manipulación de datos).  
  - `Scikit-learn` (modelos de ML).  
  - `Matplotlib/Seaborn` (visualizaciones).  
  - `imblearn` (SMOTE para balanceo).  

---

## **📂 Datos y Resultados**  
- **Dataset**: `TelecomX_Data.json` (incluye variables como `tenure`, `MonthlyCharges`, `Churn`, etc.).  
- **Salidas**:  
  - `outputs/churn_high_risk_customers.csv`: Lista de clientes prioritarios para retención.  
  - Gráficos de importancia y correlación.  

---

## **📝 Conclusiones**  
El modelo identifica con un **82% de precisión** a los clientes propensos a cancelar, permitiendo a Telecom X enfocar esfuerzos en:  
- Reducir el costo percibido (`MonthlyCharges`).  
- Incentivar contratos anuales.  
- Mejorar la experiencia en fibra óptica.  

---

## **✉️ Contacto**  
¿Preguntas o colaboraciones?  
- **Email**:  (carlosvillatobon@gmail.com)  
- **LinkedIn**: [Mi Perfil](www.linkedin.com/in/carlos-alberto-villa-tobon-4a336366).  

--- 

¡Contribuciones y feedback son bienvenidos! 🌟
