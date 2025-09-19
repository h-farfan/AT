---
layout: default
title: Aplicaciones
permalink: /aplicaciones.html
---

# Aplicaciones

Este módulo presenta las principales aplicaciones prácticas de la teoría de turbulencia óptica, tanto en investigación como en tecnología. Se incluyen comunicaciones ópticas, óptica adaptativa, diagnóstico atmosférico y aplicaciones de *Andrews & Phillips* como aperture averaging y enlaces satelitales.

---

## 1. Comunicaciones ópticas en espacio libre (FSO)

Las comunicaciones FSO usan láseres para transmitir información entre dos puntos.  
La turbulencia introduce fluctuaciones de intensidad (**scintilación**) que afectan la tasa de error de bit.

- La **relación señal/ruido (SNR)** depende de la varianza de scintilación:

$$
\sigma_I^2 = \frac{\langle I^2\rangle - \langle I\rangle^2}{\langle I\rangle^2}.
$$

- Mitigaciones:
  - Diversidad espacial (múltiples aperturas receptoras).  
  - Codificación robusta y protocolos adaptativos.  
  - Uso de aperturas grandes para suavizar fluctuaciones.

---

## 2. Óptica adaptativa

La **óptica adaptativa (AO)** corrige aberraciones de fase en tiempo real.

- Elementos principales:
  - **Sensor de frente de onda** (ej. Shack–Hartmann).  
  - **Controlador** que calcula la corrección.  
  - **Espejo deformable** que aplica la corrección.  

La AO es fundamental en astronomía, telescopios de gran apertura y sistemas de imagen de alta resolución.

---

## 3. Diagnóstico y monitoreo de turbulencia

La turbulencia atmosférica se cuantifica mediante:

- **Parámetro $C_n^2$**: derivado de mediciones de scintilación o desplazamiento de centroides.  
- **Rayo láser retrodispersado (LIDAR)**: mide perfiles de $C_n^2(h)$.  
- **Variación angular de estrellas** (tilt anisoplanático): usado en astronomía.

Estos métodos permiten caracterizar condiciones atmosféricas en tiempo real.

---

## 4. Aplicaciones en imagen e ingeniería

- **Sistemas de vigilancia óptica**: reducción de distorsión por turbulencia.  
- **Microscopía de campo amplio**: corrección de aberraciones en medios biológicos.  
- **Láseres de alta energía**: evaluación de propagación y seguridad en entornos turbulentos.

---

## 5. Aportes de *Andrews & Phillips*

El texto de *Andrews & Phillips* desarrolla aplicaciones específicas:

- **Aperture averaging:**  
  Para un diámetro de apertura $D$, la varianza de scintilación disminuye aproximadamente como:

  $$
  \sigma_I^2(D) \propto D^{-7/3},
  $$

  en turbulencia Kolmogórov, reduciendo el impacto de fluctuaciones.

- **Fuentes parcialmente coherentes:**  
  Estrategia para mitigar scintilación reduciendo la coherencia espacial inicial del haz.

- **Enlaces satélite–tierra:**  
  Modelos detallados de propagación vertical, donde $C_n^2(h)$ decrece con la altura.  
  Estos enlaces son críticos para comunicaciones espaciales y redes cuánticas.

- **Sistemas de imagen (imaging y Ladar):**  
  Predicciones de resolución y pérdida de contraste en función de $C_n^2$, $\sigma_R^2$ y el perfil atmosférico.

---

## 6. Resumen operativo

- La turbulencia limita el rendimiento de enlaces FSO, telescopios y sistemas de imagen.  
- **Óptica adaptativa** y **aperture averaging** son técnicas clave de mitigación.  
- El parámetro $C_n^2(h)$ conecta la teoría con el diseño de sistemas prácticos.  
- *Andrews & Phillips* aportan modelos predictivos para aplicaciones reales (FSO, AO, satélite-tierra, imaging).

---

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
