---
layout: default
title: Fundamentos de Turbulencia Física
permalink: /fundamentos-turbulencia.html
---

## 1. Ecuaciones de Navier–Stokes y número de Reynolds

Las ecuaciones de Navier–Stokes para un fluido incompresible son:

$$
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\nabla)\mathbf{u}
= -\frac{1}{\rho}\nabla p + \nu \nabla^2 \mathbf{u} + \mathbf{f}, 
\qquad \nabla\cdot\mathbf{u} = 0
$$

donde $\mathbf{u}(\mathbf{x},t)$ es la velocidad, $p$ la presión, $\rho$ la densidad y $\nu$ la viscosidad cinemática.

Al no dimensionalizar con una longitud $L$ y velocidad $U$ típicas aparece el **número de Reynolds**:

$$
Re = \frac{UL}{\nu}.
$$

- $Re \ll 10^3$: flujo laminar.  
- $Re \gg 10^3$: flujo turbulento.

La tasa de disipación de energía por unidad de masa es:

$$
\varepsilon = 2\nu\, s_{ij} s_{ij}, \quad
s_{ij}=\tfrac{1}{2}\left(\frac{\partial u_i}{\partial x_j}+\frac{\partial u_j}{\partial x_i}\right).
$$

Las **escalas de Kolmogórov** se definen como:

$$
\eta = \left(\frac{\nu^3}{\varepsilon}\right)^{1/4}, \quad
u_\eta = \left(\nu \varepsilon\right)^{1/4}, \quad
\tau_\eta = \left(\frac{\nu}{\varepsilon}\right)^{1/2}.
$$

---

## 2. Teoría de Kolmogórov K41 y K62

### 2.1 Hipótesis K41

En el intervalo inercial $\eta \ll r \ll L_0$, los incrementos longitudinales de velocidad:

$$
\delta u_L(\mathbf{x},\mathbf{r}) = [\mathbf{u}(\mathbf{x}+\mathbf{r})-\mathbf{u}(\mathbf{x})]\cdot \frac{\mathbf{r}}{r}
$$

tienen funciones de estructura:

$$
S_p(r) = \left\langle |\delta u_L|^p \right\rangle \propto (\varepsilon r)^{\zeta_p}, 
\qquad \zeta_p^{K41} = \frac{p}{3}.
$$

- **Ley de los 2/3**:

$$
S_2(r) = C_2 (\varepsilon r)^{2/3}.
$$

- **Ley de los 4/5**:

$$
\langle (\delta u_L)^3 \rangle = -\frac{4}{5}\,\varepsilon\, r.
$$

### 2.2 Espectro de energía

El espectro de energía en el rango inercial es:

$$
E(k) = C_K\, \varepsilon^{2/3}\, k^{-5/3}, 
\qquad \frac{1}{L_0}\ll k \ll \frac{1}{\eta}.
$$

### 2.3 Refinamiento K62

Kolmogórov (1962) propuso que la intermitencia modifica los exponentes:

$$
\zeta_p^{K62} = \frac{p}{3} - \frac{\mu}{18}\,p(p-3),
$$

donde $\mu \approx 0.2-0.25$ describe la intensidad de la intermitencia.

---

## 3. Espectros espaciales del índice de refracción

Las fluctuaciones de índice $\delta n(\mathbf{x})$ siguen:

$$
D_n(r)=\langle [n(\mathbf{x}+\mathbf{r})-n(\mathbf{x})]^2 \rangle
= C_n^2\, r^{2/3}, \quad \eta \ll r \ll L_0,
$$

con $C_n^2$ el **parámetro de estructura**.

- **Espectro de Kolmogórov**:

$$
\Phi_n(\kappa)=0.033\, C_n^2\, \kappa^{-11/3},
\quad \kappa_0 \ll \kappa \ll \kappa_m.
$$

- **Espectro de von Kármán**:

$$
\Phi_n(\kappa)=0.033\, C_n^2\, (\kappa^2+\kappa_0^2)^{-11/6}
\exp\!\left(-\frac{\kappa^2}{\kappa_m^2}\right).
$$

Aquí $\kappa_0 \sim 1/L_0$ y $\kappa_m \sim 1/\eta$.

---

## 4. Procesos aleatorios: PSD y ergodicidad

Sea $x(t)$ un proceso aleatorio estacionario en sentido amplio, con autocorrelación:

$$
R_x(\tau)=\mathbb{E}[(x(t)-\mu)(x(t+\tau)-\mu)].
$$

La **densidad espectral de potencia** se obtiene por Fourier:

$$
S_x(\omega) = \int_{-\infty}^{\infty} R_x(\tau)\, e^{-i\omega \tau}\, d\tau.
$$

La ergodicidad implica que el promedio temporal coincide con el promedio de conjunto:

$$
\lim_{T\to\infty}\frac{1}{T}\int_0^T x(t)\,dt = \mathbb{E}[x(t)].
$$

En turbulencia, esta propiedad permite estimar $S_x(\omega)$ a partir de una sola serie temporal larga.

---

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
