---
layout: default
title: Fundamentos de Turbulencia Física
permalink: /fundamentos-turbulencia.html
---

## 1. Ecuaciones de Navier–Stokes y número de Reynolds

## 1. Ecuaciones de Navier–Stokes y número de Reynolds

Las **ecuaciones de Navier–Stokes** describen el movimiento de un fluido newtoniano incompresible y constituyen el punto de partida para el estudio de la turbulencia:

$$
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\nabla)\mathbf{u}
= -\frac{1}{\rho}\nabla p + \nu \nabla^2 \mathbf{u} + \mathbf{f}, 
\qquad \nabla\cdot\mathbf{u} = 0,
$$

donde:

- $\mathbf{u}(\mathbf{x},t)$ es el **campo de velocidad**,  
- $p(\mathbf{x},t)$ la **presión dinámica**,  
- $\rho$ la **densidad constante**,  
- $\nu = \mu/\rho$ la **viscosidad cinemática**,  
- $\mathbf{f}$ representa **fuerzas externas** (p. ej., gravedad o forzamiento).  

Estas ecuaciones pueden interpretarse como un **balance de momento lineal**:  
- $\partial_t \mathbf{u}$ describe la aceleración local.  
- $(\mathbf{u}\cdot\nabla)\mathbf{u}$ es la convección no lineal de momento.  
- $-\nabla p/\rho$ asegura la condición de incompresibilidad.  
- $\nu \nabla^2 \mathbf{u}$ representa difusión viscosa.  
- $\mathbf{f}$ inyecta energía al sistema.  

---

### 1.1 Forma adimensional y número de Reynolds

**Objetivo.** Reescalar Navier–Stokes para identificar los grupos adimensionales que controlan la dinámica y, en particular, el **número de Reynolds**.

#### 1.1.1 Elección de escalas y variables sin dimensiones

Sea $L$ una longitud típica, $U$ una velocidad característica y $T=L/U$ el tiempo convectivo. Se definen

$$
\mathbf{x}^*=\frac{\mathbf{x}}{L},\quad 
t^*=\frac{t}{T},\quad 
\mathbf{u}^*=\frac{\mathbf{u}}{U},\quad 
p^*=\frac{p}{\rho U^2}.
$$

Sustituyendo en Navier–Stokes y omitiendo asteriscos:

$$
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\cdot\nabla)\mathbf{u}
= -\nabla p + \frac{1}{Re}\,\nabla^2 \mathbf{u} + \mathbf{f}^*, 
\qquad \nabla\cdot\mathbf{u} = 0,
$$

donde aparece el **número de Reynolds**:

$$
Re = \frac{UL}{\nu}.
$$

Este parámetro mide la razón entre inercia y viscosidad:  
- $Re \ll 1$: régimen de Stokes (viscoso).  
- $Re \sim 10^2-10^3$: transición laminar–turbulento.  
- $Re \gg 10^3$: régimen turbulento desarrollado.

#### 1.1.2 Escalado alternativo de la presión y equivalencia

Otra elección común es **escalar la presión con $\rho\nu U/L$** (escala viscosa),

$$
\tilde p=\frac{p}{\rho \nu U/L}.
$$

En ese caso, la ecuación adimensional toma la forma

$$
\frac{\partial \mathbf{u}^*}{\partial t^*}+(\mathbf{u}^*\!\cdot\!\nabla^*)\mathbf{u}^*
=-Re\,\nabla^* \tilde p+\nabla^{*2}\mathbf{u}^*+\mathbf{f}^*,
$$

donde el factor $Re$ migra al término de presión. Ambas formulaciones son **equivalentes**: la física no cambia; sólo cambia dónde aparece $Re$. El escalado dinámico es preferido cuando la presión juega el papel de **campo de Lagrange** que impone $\nabla\!\cdot\!\mathbf{u}=0$ al mismo orden que la inercia.

---

#### 1.1.3 Ecuación adimensional en vorticidad

Para resaltar la competencia entre estiramiento y difusión, sea $\boldsymbol{\omega}=\nabla\times\mathbf{u}$ y $\boldsymbol{\omega}^*=(L/U)\boldsymbol{\omega}$. Se obtiene

$$
\frac{\partial \boldsymbol{\omega}^*}{\partial t^*}+(\mathbf{u}^*\!\cdot\!\nabla^*)\boldsymbol{\omega}^*
=(\boldsymbol{\omega}^*\!\cdot\!\nabla^*)\mathbf{u}^*+\frac{1}{Re}\,\nabla^{*2}\boldsymbol{\omega}^*+\left(\nabla^*\times\mathbf{f}^*\right).
$$

- Término de **estiramiento** $(\boldsymbol{\omega}^*\!\cdot\!\nabla^*)\mathbf{u}^*$: fuente de multiescala en $Re$ altos.  
- Término **difusivo** $Re^{-1}\nabla^{*2}\boldsymbol{\omega}^*$: suaviza gradientes, dominante en $Re$ bajos.

---

#### 1.1.4 Balance energético adimensional

Sea la energía cinética específica $k=\tfrac12 |\mathbf{u}|^2$ y $k^*=\tfrac12 |\mathbf{u}^*|^2$. En ausencia de flujo de frontera y con forzamiento $\mathbf{f}$, el balance integrado conduce a

$$
\frac{d}{dt^*}\langle k^*\rangle \;=\; \langle \mathbf{u}^*\!\cdot\!\mathbf{f}^*\rangle \;-\; \frac{1}{Re}\,\langle |\nabla^*\mathbf{u}^*|^2\rangle,
$$

lo que muestra explícitamente que la disipación viscosa está **ponderada por $Re^{-1}$**.

---

#### 1.1.5 Inclusión de otras fuerzas y números adimensionales

Si la dinámica incluye efectos adicionales, surgen otros parámetros al adimensionalizar:

- **Gravedad (flujos libres superficiales o estratificados)**: número de Froude  
  $$
  Fr=\frac{U}{\sqrt{gH}}.
  $$

- **Rotación (marcos en rotación a $2\Omega$)**: número de Rossby  
  $$
  Ro=\frac{U}{2\Omega L}.
  $$

- **Compresibilidad**: número de Mach  
  $$
  Ma=\frac{U}{c}.
  $$

- **Magnetohidrodinámica (MHD)**: Reynolds magnético  
  $$
  Rm=\frac{U L}{\eta_m}, \quad A=\frac{U}{V_A}.
  $$

Estos parámetros coexisten con $Re$ y definen **regímenes asintóticos** distintos (p. ej., $Re\gg1$, $Ro\ll1$ para dinámica casi geostrófica).

---

#### 1.1.6 Límites asintóticos y estructura de capas

- **Límite $Re\to 0$ (Stokes):** la inercia es despreciable frente a la viscosidad; las ecuaciones se linealizan y no hay cascada de energía.  
- **Límite $Re\to \infty$:** la viscosidad sólo actúa en **capas delgadas** (de pared o de cizalla) y en las **pequeñas escalas**; la dinámica a gran escala es esencialmente inercial y no lineal.  
- **Compatibilidad con condiciones de contorno:** incluso cuando $Re\gg1$, la condición de no deslizamiento en paredes sólidas induce **capas límite** cuya física requiere un reescalado local.

---

#### 1.1.7 Comentario sobre la elección de $L$ y $U$

La definición de $Re$ depende de la **elección informada** de $L$ y $U$. En flujos libres suele tomarse la **escala de inyección** (p. ej., tamaño del chorro), mientras que en flujos de pared puede usarse $L$ como dimensión hidráulica. La elección de $U$ como velocidad a granel o de fricción modifica la forma adimensional, pero **no** la física subyacente: el número de Reynolds siempre cuantifica la relación inercia/viscosidad.

---

### 1.2 Escalas energéticas y disipación

La tasa de disipación de energía por unidad de masa se define como

$$
\varepsilon = 2\nu\, s_{ij} s_{ij}, \quad
s_{ij}=\tfrac{1}{2}\left(\frac{\partial u_i}{\partial x_j}+\frac{\partial u_j}{\partial x_i}\right).
$$

A partir de $\varepsilon$ y $\nu$ se introducen las **escalas de Kolmogórov**:

$$
\eta = \left(\frac{\nu^3}{\varepsilon}\right)^{1/4}, \quad
u_\eta = \left(\nu \varepsilon\right)^{1/4}, \quad
\tau_\eta = \left(\frac{\nu}{\varepsilon}\right)^{1/2}.
$$

Estas representan las longitudes, velocidades y tiempos característicos de los remolinos más pequeños donde domina la disipación viscosa.


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
