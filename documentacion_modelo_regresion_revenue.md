
# 📈 Modelo de Regresión Lineal – Predicción de Revenue

Este archivo documenta el modelo de regresión lineal entrenado para predecir el **revenue mensual** en la categoría *Electronics*, como parte del análisis para MELI.

---

## 🎯 Objetivo del Modelo

Predecir el `revenue` mensual en función de variables clave de comportamiento comercial, con fines de forecasting y simulación de estrategias de pricing.

---

## 🧾 Variables del Modelo

**Variables independientes (features):**

- `avg_price`: Precio promedio mensual
- `quantity`: Volumen total vendido
- `month_num`: Mes del año (1-12)
- `year`: Año (2022, 2023, etc.)

**Variable dependiente (target):**

- `revenue`: Ingresos mensuales totales

---

## ⚙️ Detalles del Modelo

- Tipo: `LinearRegression` de `sklearn`
- Entrenado sobre datos de Electronics agregados mensualmente
- R² en test (últimos 6 meses): **0.98**
- MAPE: **< 1%**

---

## 📦 Archivo del Modelo

El modelo entrenado está guardado como archivo `.pkl` y puede cargarse con:

```python
import pickle
with open("regresion_lineal_revenue_model.pkl", "rb") as f:
    model = pickle.load(f)
```

---

## ✅ Uso esperado

- Forecast de revenue mensual
- Simulaciones de impacto por cambio en `avg_price` o `quantity`
- Soporte a decisiones de pricing o planificación comercial

