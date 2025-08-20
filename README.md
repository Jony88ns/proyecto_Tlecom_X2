# proyecto_Tlecom_X2
Proyecto Telecom X2

---

# 📊 Predicción de Churn en Telecom X2

## 📝 Descripción

Este proyecto busca analizar y predecir la cancelación de clientes (**churn**) en la empresa de telecomunicaciones **Telecom X**, que enfrenta una alta tasa de bajas de clientes.
El objetivo es **identificar qué clientes tienen mayor probabilidad de abandonar** la empresa, permitiendo diseñar **estrategias de retención proactivas**.

El trabajo sigue la metodología **CRISP-DM**, pasando por las etapas de comprensión del negocio, exploración de datos, preparación, modelado y evaluación.

---

## 📂 Estructura del Proyecto

* `TELCOMX2Alura.ipynb`: Notebook con todo el flujo de análisis y modelado.
* `README.md`: Documentación del proyecto.

---

## 📊 Datos

Los datos fueron obtenidos desde una API y contienen información de:

* **Customer**: datos demográficos del cliente.
* **Account**: información de cuentas y métodos de pago.
* **Services**: servicios contratados, como:

  * Telefonía fija y múltiples líneas.
  * Internet y servicios adicionales (seguridad online, respaldo, protección de dispositivos, soporte técnico).
  * Televisión por cable y streaming de películas.

La variable objetivo es **Churn** (1 = el cliente se da de baja, 0 = el cliente se mantiene).

---

## 🔎 Análisis Exploratorio

Durante la exploración de los datos se identificaron:

* Mayor propensión al churn en clientes con **contratos mensuales** frente a contratos anuales.
* Relación entre churn y **métodos de pago automáticos** (mayor retención).
* Servicios adicionales como **seguridad online o respaldo** se asocian con menor churn.
* Los clientes con **cargos mensuales altos y menor antigüedad** tienden a cancelar más.

---

## 🤖 Modelos Implementados

Se probaron distintos algoritmos de clasificación binaria:

* **Random Forest**
* **XGBoost**
* **LightGBM**
* **Support Vector Machine (SVM)**

Las métricas utilizadas incluyeron:

* Accuracy
* F1-Score
* ROC-AUC
* Matriz de confusión

El mejor rendimiento se obtuvo con **LightGBM**, logrando una buena capacidad de discriminación entre clientes que permanecen y los que se dan de baja.

---

## ✅ Conclusiones

* El churn está fuertemente relacionado con el **tipo de contrato**: los contratos más cortos implican mayor riesgo de baja.
* Los clientes con **muchos servicios adicionales** suelen mostrar mayor fidelidad.
* Los **métodos de pago electrónicos** (como domiciliación bancaria) reducen la tasa de cancelación.
* Existe una relación clara entre **costo mensual alto y abandono**, especialmente en clientes con poca antigüedad.

---

## 💡 Recomendaciones

* Incentivar a clientes de contratos mensuales a migrar hacia **planes anuales** con beneficios adicionales.
* Fomentar la contratación de **servicios complementarios** que aumentan el valor percibido.
* Promover métodos de **pago automático** para reducir fricciones en el proceso de facturación.
* Diseñar campañas de retención personalizadas para clientes con **cargos altos y poca antigüedad**, ya que son los más propensos a desertar.
* Implementar un **modelo de predicción en producción**, que marque en tiempo real a los clientes con riesgo de churn para que el área comercial actúe de inmediato.

---

## 🚀 Tecnologías utilizadas

* Python 3
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* TensorFlow / Keras
* XGBoost, LightGBM
* Jupyter Notebook

---
