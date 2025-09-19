---
layout: default
title:  Recursos Interactivos
permalink: /recursos-interactivos.html
---

# Recursos Interactivos

Este módulo reúne recursos prácticos para explorar la turbulencia óptica: simulaciones, visualizaciones, datos abiertos y guías de análisis. También se mencionan ejemplos extraídos de *Andrews & Phillips* que pueden adaptarse como ejercicios.

---

## 1. Simulaciones numéricas

### 1.1 Pantallas de fase
El método de **pantallas de fase** discretiza la atmósfera turbulenta en capas.  
Cada pantalla aplica una fase aleatoria con espectro $\Phi_n(\kappa)$:

$$
\Phi_n(\kappa) = 0.033 \, C_n^2 \, \kappa^{-11/3}.
$$

Este método permite:
- Simular propagación de haces gaussianos.  
- Visualizar distorsión de frente de onda.  
- Evaluar beam wander y scintilación.

### 1.2 Caminatas de centroides
Se pueden generar trayectorias de centroides mediante procesos estocásticos:

- Movimiento browniano fraccional (fBm) con exponente $H$.  
- Series sintéticas con DFA o PSD prescritos.  

Estas caminatas sirven para comparar con datos experimentales.

---

## 2. Visualizaciones interactivas

- **Mapas dinámicos de scintilación**: representar $I(x,y,t)$ en tiempo real.  
- **Diagramas de cascada**: mostrar cómo la energía se transfiere entre escalas.  
- **Animaciones de beams**: visualizar cómo un haz puntual se deforma al atravesar pantallas turbulentas.

Estas visualizaciones ayudan a estudiantes e investigadores a intuir conceptos abstractos.

---

## 3. Datos abiertos y análisis reproducible

Se recomienda incluir en la wiki:

- Archivos `.mat` o `.csv` con series de centroides, irradiancia y temperatura.  
- Scripts en MATLAB/Python para:
  - Calcular DFA y Hurst $H$.  
  - Estimar $C_n^2$ a partir de series.  
  - Ajustar distribuciones de irradiancia (log-normal, Gamma-Gamma).  

### Ejemplo: estimación de $C_n^2$
A partir de un registro de desplazamiento de centroides $\Delta x(t)$:

$$
C_n^2 \approx \frac{\langle (\Delta x)^2 \rangle}{k^{7/6} L^{11/6}}.
$$

---

## 4. Ejercicios inspirados en *Andrews & Phillips*

*Andrews & Phillips* ofrecen ejemplos teóricos que pueden adaptarse como prácticas interactivas:

- **Cálculo del índice de scintilación** para diferentes $C_n^2(h)$.  
- **Comparación de distribuciones** (log-normal vs Gamma-Gamma) para la irradiancia medida.  
- **Aperture averaging**: visualizar cómo crece la apertura $D$ y disminuye $\sigma_I^2$.  

---

## 5. Integración en la wiki

Cada recurso puede enlazarse desde la página principal con íconos o botones.  
Ejemplos:
- 🔗 [Simulación de pantallas de fase](/simulaciones/phase-screen.html)  
- 🔗 [Datos abiertos de centroides](/data/centroides.csv)  
- 🔗 [Notebook DFA en Python](/notebooks/dfa_demo.ipynb)

---

## 6. Resumen operativo

- Las **pantallas de fase** y las **series sintéticas** son métodos básicos de simulación.  
- Las **visualizaciones interactivas** facilitan el aprendizaje.  
- Los **datos abiertos** garantizan reproducibilidad y continuidad del proyecto.  
- *Andrews & Phillips* proveen ejemplos clásicos que pueden transformarse en ejercicios prácticos.

---

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
