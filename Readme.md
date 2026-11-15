# 📦 Optimización de Cadena de Suministro y Riesgo Logístico

Análisis exploratorio de **180,519 registros transaccionales** (65,752 órdenes únicas) para entender por qué se están retrasando las entregas, medir el impacto financiero y proponer mejoras operativas usando Python y Excel.

---

## 📌 1. Contexto del Proyecto

La compañía mueve un volumen importante de negocio con **$36.78M USD** en ventas y **$3.97M USD** en beneficios, pero enfrenta un problema operativo pesado: **el 54.83% de los envíos llegan tarde**.

En este proyecto armé un flujo de trabajo para atacar este problema: limpié los datos crudos en Python, calculé métricas clave de negocio en Excel y diseñé un dashboard ejecutivo para visualizar dónde está el verdadero cuello de botella.

### 🛠️ Herramientas Utilizadas
* **Python (`pandas`, `numpy`):** Limpieza de datos (ETL), eliminación de información sensible (PII como correos y contraseñas), tratamiento de nulos y estandarización de fechas.
* **Microsoft Excel:** Creación de campos calculados (*Shipping gap*, *Risk Category*, *Fraud Prevention*), tablas dinámicas y diseño del tablero final.

---

## ❓ 2. Preguntas Clave que quise resolver

1. ¿Cuál es el retraso real en las entregas y cuántos días de diferencia hay entre lo prometido y lo real?
2. ¿Qué tipo de envío (*Shipping Mode*) es el que está fallando más y rompiendo la promesa con el cliente?
3. ¿Cuáles son los países o regiones que dejan más dinero y dónde deberíamos poner atención?
4. ¿Cómo podemos controlar las cancelaciones y el fraude detectado (**2.25%**) sin afectar la operación?

---

## 📂 3. Estructura del Repositorio

```text
supply-chain-optimization/
│
├── data/
│   └── clean_supply.csv                      # Dataset limpio y listo para análisis (44 columnas)
│
├── notebooks/
│   └── 01_data_cleaning.ipynb                # Script de Python con la limpieza y auditoría inicial
│
├── dashboards/
│   └── Supply_analysis.xlsx                  # Archivo de Excel con el modelo de datos y el Dashboard
│
├── reports/
│   └── Informe_SupplyChain_PedroVargas.pdf   # Reporte ejecutivo listo para descargar
│
├── images/
│   └── executive_dashboard.png               # Captura general del tablero en Excel
│
└── README.md                                 # Documentación del proyecto
