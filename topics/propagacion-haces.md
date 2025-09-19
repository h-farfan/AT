---
layout: default
title: Propagación de Haces en Medios Turbulentos
permalink: /propagacion-haces.html
---

# Propagación de Haces en Medios Turbulentos

Este módulo aborda la teoría de propagación de haces ópticos a través de la atmósfera turbulenta. Se presentan las aproximaciones físicas (Rytov, Born, ABCD), los efectos clásicos (desplazamiento de haz, fluctuaciones de ángulo de llegada, pérdida de coherencia) y los aportes de *Andrews & Phillips* (modelos de pantallas de fase, fluctuaciones de irradiancia y coherencia espacial/temporal).

---

## 1. Propagación libre de haces gaussianos

Un haz gaussiano en espacio libre (sin turbulencia) tiene distribución de campo:

$$
U(r,z) = U_0 \, \frac{w_0}{w(z)} \,
\exp\!\left(-\frac{r^2}{w^2(z)}\right)
\exp\!\left(-ikz - i\frac{kr^2}{2R(z)} + i\zeta(z)\right),
$$

donde:

- $w(z) = w_0 \sqrt{1+(z/z_R)^2}$ es el radio de haz,
- $R(z) = z\left[1+(z_R/z)^2\right]$ es el radio de curvatura,
- $\zeta(z)=\arctan(z/z_R)$ es la fase de Gouy,
- $z_R = \pi w_0^2/\lambda$ es la longitud de Rayleigh.

---

## 2. Aproximación de Rytov

En turbulencia débil, la fluctuación del campo $U$ puede modelarse como:

$$
U(\mathbf{r},z) = U_0(\mathbf{r},z)\,\exp[\psi(\mathbf{r},z)],
$$

donde $\psi = \chi + iS$ contiene fluctuaciones de amplitud $\chi$ y fase $S$.  

La **varianza de Rytov** cuantifica la intensidad de la turbulencia:

$$
\sigma_R^2 = 1.23 \, C_n^2 \, k^{7/6} \, L^{11/6},
$$

con $k=2\pi/\lambda$ y $L$ la distancia de propagación.

- $\sigma_R^2 \ll 1$: turbulencia débil.  
- $\sigma_R^2 \gg 1$: turbulencia fuerte.

---

## 3. Wander del haz y ángulo de llegada

La turbulencia provoca desplazamientos aleatorios del centroide del haz (**beam wander**).  
El ángulo de llegada fluctúa con varianza aproximada:

$$
\sigma_\theta^2 \approx 2.91\,k^2 \, L^{-1/3} \int_0^L C_n^2(z) \, (L-z)^{5/3}\, dz.
$$

Estas fluctuaciones afectan la resolución de sistemas de imagen y la estabilidad de enlaces ópticos.

---

## 4. Coherencia espacial y temporal

El campo óptico en turbulencia pierde coherencia.  
La función de coherencia mutua:

$$
\Gamma(\mathbf{r_1},\mathbf{r_2};z) =
\langle U(\mathbf{r_1},z)\,U^*(\mathbf{r_2},z)\rangle,
$$

se degrada con la separación $|\mathbf{r_1}-\mathbf{r_2}|$ debido a fluctuaciones de fase.  

En condiciones de turbulencia Kolmogórov, la longitud de coherencia transversal se aproxima como:

$$
\rho_0 = \left[ 0.423 \, k^2 \int_0^L C_n^2(z)\, dz \right]^{-3/5}.
$$

---

## 5. Modelos ABCD y óptica adaptativa

- **Matriz ABCD**: describe la propagación de haces gaussianos a través de sistemas ópticos lineales (lentes, espejos, espacio libre).  
- En turbulencia, se combina con **modelos estadísticos** para estimar la evolución de $w(z)$ y la calidad de haz.  
- La **óptica adaptativa** corrige en tiempo real las aberraciones de fase, usando sensores y espejos deformables.

---

## 6. Aportes de *Andrews & Phillips*

El libro *Laser Beam Propagation through Random Media* desarrolla en detalle:

- **Modelos de pantallas de fase (Phase Screen Models):**  
  La atmósfera se modela como múltiples pantallas discretas de fase aleatoria, equivalentes al espectro $\Phi_n(\kappa)$.  
  Este método se usa en simulaciones numéricas.

- **Beam wander y scintilación angular:**  
  Fórmulas empíricas para la varianza del ángulo de llegada y desplazamientos del spot.

- **Aperture averaging:**  
  Efecto de promediar sobre aperturas grandes, reduciendo la varianza de scintilación.

- **Fuentes parcialmente coherentes:**  
  Discuten cómo la coherencia parcial inicial puede mitigar los efectos de la turbulencia.

---

## 7. Resumen operativo

- La turbulencia afecta la propagación de haces a través de **scintilación, wander y pérdida de coherencia**.  
- La **aproximación de Rytov** describe el régimen débil, mientras que simulaciones de pantallas de fase extienden el análisis a regímenes fuertes.  
- El parámetro clave es $\sigma_R^2$, que clasifica el régimen de turbulencia.  
- *Andrews & Phillips* proveen modelos aplicados a enlaces ópticos, imágenes y láseres de alta potencia.

---

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
