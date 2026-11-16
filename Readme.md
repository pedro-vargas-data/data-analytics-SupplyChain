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

* **`Data/sample_clean_supply.csv`** — Dataset limpio y listo para análisis (44 columnas)
* **`Notebooks/supply-chain-optimization_notebooks_01_data_cleaning.ipynb`** — Script de Python con la limpieza y auditoría inicial
* **`Reports/Informe_SupplyChain_PedroVargas.pdf`** — Reporte ejecutivo listo para descargar
* **`Outputs/Executive_dashboard.png`** — Captura general del tablero en Excel
* **`Readme.md`** — Documentación principal del proyecto

---

## 🔍 4. Principales Hallazgos

### 📊 El problema real con los envíos
Al cruzar los datos por tipo de envío, descubrí que el problema no es general, sino de servicios específicos con expectativas irreales:
* **First Class:** `95.32%` de retrasos (27,814 ítems). Prácticamente todo llega tarde.
* **Second Class:** `76.63%` de retrasos (35,216 ítems). Una brecha de tiempo muy alta.
* **Same Day:** `45.74%` de retrasos (9,737 ítems).
* **Standard Class:** `38.07%` de retrasos (107,752 ítems). Es la base más estable de la operación.

### 🌍 ¿Dónde se concentra el negocio?
* **Mercados principales:** **Europa** ($10.87M USD) y **LATAM** ($10.28M USD) suman el **57.5%** de las ventas totales.
* **Categorías fuertes:** **Fan Shop** ($17.11M USD) y **Apparel** ($7.98M USD) lideran la facturación.

---

## 📊 5. Vista Previa del Dashboard
![Executive Dashboard](images/executive_dashboard.png)

---

## 💡 6. Recomendaciones Operativas

1. **Ajustar los tiempos de entrega (SLAs):** Las promesas en *First* y *Second Class* están rotas frente a la realidad logística. Hay que ajustar los días estimados en el sistema para no darle falsas expectativas al cliente.
2. **Revisar socios logísticos (3PL):** Poner la lupa en Europa y LATAM, ya que concentran la mayor parte de los ingresos y las demoras.
3. **Control antifraude:** Automatizar validaciones básicas en las órdenes para mantener controlado el **2.25%** de riesgo de fraude detectado sin bloquear ventas legítimas.

---

## 🚀 7. Cómo clonar y revisar el proyecto

```bash
git clone https://github.com/pedro-vargas-data/data-analytics-SupplyChain.git
cd data-analytics-SupplyChain
```
## Desarrollado por Pedro Vargas Salgado | www.linkedin.com/in/pedrovargas-data-mba

