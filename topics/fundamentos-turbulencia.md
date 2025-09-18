---
layout: default
title: Fundamentos de Turbulencia Física
permalink: /fundamentos-turbulencia.html
---

> Esta página resume los fundamentos físicos y estadísticos necesarios para el resto de la wiki/tesis: dinámica de fluidos (Navier–Stokes, Reynolds), teoría K41/K62, espectros espaciales del índice de refracción y nociones de procesos aleatorios (PSD, ergodicidad).

## 1. Ecuaciones de Navier–Stokes y número de Reynolds

Consideremos un fluido **incompresible** y **newtoniano** con densidad constante \(\rho\) y viscosidad cinemática \(\nu\). Las ecuaciones de movimiento son
\[
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u}\!\cdot\!\nabla)\mathbf{u}
= -\frac{1}{\rho}\nabla p + \nu \nabla^2 \mathbf{u} + \mathbf{f}, 
\qquad \nabla\!\cdot\!\mathbf{u} = 0,
\]
donde \(\mathbf{u}(\mathbf{x},t)\) es la velocidad, \(p(\mathbf{x},t)\) la presión y \(\mathbf{f}\) fuerzas volumétricas (p.ej. gradientes de densidad/temperatura o forzamientos mecánicos).

### 1.1 No dimensionalización y \(Re\)
Sea \(U\) una velocidad típica y \(L\) una escala de longitud. Definimos variables adimensionales
\[
\mathbf{x}'=\frac{\mathbf{x}}{L},\quad t'=\frac{tU}{L},\quad
\mathbf{u}'=\frac{\mathbf{u}}{U},\quad p'=\frac{p}{\rho U^2}.
\]
Las ecuaciones quedan
\[
\frac{\partial \mathbf{u}'}{\partial t'} + (\mathbf{u}'\!\cdot\!\nabla')\mathbf{u}'
= -\nabla' p' + \frac{1}{Re}\nabla'^2 \mathbf{u}' + \mathbf{f}',
\]
donde aparece el **número de Reynolds**
\[
Re \equiv \frac{UL}{\nu}.
\]
- \(Re \ll 10^3\): flujo usualmente **laminar** (dominancia viscosa).
- \(Re \gg 10^3\): régimen **turbulento** (no linealidad dominante, cascada de energía).

### 1.2 Tasas y escalas de Kolmogórov
La **tasa de disipación de energía** por unidad de masa es
\[
\varepsilon(\mathbf{x},t) = 2\nu\, s_{ij} s_{ij}, \quad
s_{ij}=\tfrac{1}{2}\!\left(\frac{\partial u_i}{\partial x_j}+\frac{\partial u_j}{\partial x_i}\right),
\]
y su promedio \(\varepsilon=\langle \varepsilon(\mathbf{x},t)\rangle\) fija las **escalas microscópicas** de Kolmogórov:
\[
\eta = \left(\frac{\nu^3}{\varepsilon}\right)^{1/4},\quad
u_\eta = \left(\nu \varepsilon\right)^{1/4},\quad
\tau_\eta = \left(\frac{\nu}{\varepsilon}\right)^{1/2}.
\]
Aquí \(\eta\) es la longitud de disipación, \(u_\eta\) la velocidad típica y \(\tau_\eta\) el tiempo característico más pequeño.

---

## 2. Teoría de Kolmogórov K41 y su refinamiento K62

### 2.1 Hipótesis K41
Bajo **homogeneidad**, **isotropía** y **alto Reynolds**, Kolmogórov postuló que en el **intervalo inercial** \( \eta \ll r \ll L_0 \) (con \(L_0\) la **escala integral** o de inyección) la estadística está gobernada únicamente por \(\varepsilon\) y \(r\). De ahí se deduce que los incrementos longitudinales
\[
\delta u_L(\mathbf{x},\mathbf{r}) = [\mathbf{u}(\mathbf{x}+\mathbf{r})-\mathbf{u}(\mathbf{x})]\cdot \frac{\mathbf{r}}{r}
\]
tienen **funciones de estructura** 
\[
S_p(r) \equiv \left\langle |\delta u_L|^p \right\rangle \propto (\varepsilon r)^{\zeta_p},
\qquad \zeta_p^{\text{K41}}=\frac{p}{3}.
\]

#### Ley de los 2/3 (segundo orden)
\[
S_2(r) = C_2 (\varepsilon r)^{2/3}.
\]

#### Ley de los 4/5 (tercer orden, exacta)
\[
\langle (\delta u_L)^3 \rangle = -\frac{4}{5}\,\varepsilon\, r.
\]

### 2.2 Espectro de energía \(\,E(k)\)
Por la transformada de Wiener–Khinchin entre \(S_2\) y el **espectro unidimensional** \(E(k)\),
\[
E(k) = C_K\, \varepsilon^{2/3}\, k^{-5/3}, \qquad \frac{1}{L_0}\ll k \ll \frac{1}{\eta},
\]
la conocida “ley de \(-5/3\)”. \(C_K\) es la **constante de Kolmogórov** (orden unidad).

### 2.3 Refinamiento K62: intermitencia (modelo log-normal)
Las fluctuaciones de \(\varepsilon\) a múltiples escalas introducen **intermitencia** y desvíos de \(\zeta_p=p/3\). El **modelo log-normal** de 1962 propone
\[
\zeta_p^{\text{K62}}=\frac{p}{3}-\frac{\mu}{18}\,p(p-3),
\]
donde \(\mu\) (\(\approx 0.2\)–\(0.25\) en muchos flujos) cuantifica la intensidad de la intermitencia. Este refinamiento preserva la ley exacta de los 4/5 para \(p=3\).

---

## 3. Espectros espaciales del índice de refracción \(n(\mathbf{x})\)

En óptica atmosférica, las **fluctuaciones del índice de refracción** \(\delta n(\mathbf{x})\) se tratan como un **campo escalar pasivo** movido por la turbulencia. Su **función de estructura** en el intervalo inercial satisface
\[
D_n(r)\equiv \left\langle [n(\mathbf{x}+\mathbf{r})-n(\mathbf{x})]^2 \right\rangle
= C_n^2\, r^{2/3}, \qquad \eta \ll r \ll L_0,
\]
donde \(C_n^2\) es el **parámetro de estructura** (con dimensiones \( \text{m}^{-2/3}\)), que cuantifica la fuerza de turbulencia óptica.

### 3.1 Espectros tridimensionales: Kolmogórov y von Kármán
Denotando por \(\Phi_n(\kappa)\) el **espectro tridimensional** (densidad espectral en el espacio de números de onda \(\kappa=|\boldsymbol{\kappa}|\)), tenemos:

- **Modelo de Kolmogórov (inercial puro)**  
  \[
  \Phi_n(\kappa)=0.033\, C_n^2\, \kappa^{-11/3},
  \qquad \kappa_0 \ll \kappa \ll \kappa_m,
  \]
  con \(\kappa_0\sim 1/L_0\) (exterior) y \(\kappa_m\sim 1/\eta\) (interior).

- **Modelo de von Kármán (con cortes en interior y exterior)**  
  \[
  \Phi_n(\kappa)=0.033\, C_n^2\,\bigl(\kappa^2+\kappa_0^2\bigr)^{-11/6}
  \exp\!\left(-\frac{\kappa^2}{\kappa_m^2}\right),
  \]
  un regularizador que incorpora explícitamente **escala exterior** \(L_0=2\pi/\kappa_0\) y **escala interior** \(l_0\approx 5.92/\kappa_m\).

> **Relaciones de consistencia.** Con la **covarianza** \(B_n(r)=\langle n(\mathbf{x})\,n(\mathbf{x}+\mathbf{r})\rangle\),
\[
B_n(r) = \frac{1}{(2\pi)^3}\!\int_{\mathbb{R}^3}\! 
\Phi_n(\boldsymbol{\kappa})\, e^{i\boldsymbol{\kappa}\cdot\mathbf{r}}\, d^3\kappa,
\qquad
D_n(r)=2\,[B_n(0)-B_n(r)].
\]
En el rango inercial, \( \Phi_n\!\propto\!\kappa^{-11/3} \Longleftrightarrow D_n(r)\!\propto\! r^{2/3}\).

### 3.2 Conexión termodinámica (ideal gas, vía densidad)
Para longitudes de onda ópticas en aire estándar, la **refractividad** \(N\equiv (n-1)\!\times\!10^6\) es aproximadamente proporcional a la densidad \(\rho\): \(n-1 \approx K(\lambda)\,\rho\).  
Usando la ecuación de estado \( \rho\approx P/(R T)\), fluctuaciones de temperatura/presión inducen
\[
\delta n \approx \left(\frac{\partial n}{\partial \rho}\right)\delta \rho 
= K(\lambda)\,\delta \rho
\quad\Rightarrow\quad
\delta n \simeq K(\lambda)\!\left(\frac{\delta P}{R T}-\frac{P}{R T^2}\delta T\right).
\]
Bajo condiciones casi isobáricas cerca del suelo, frecuentemente domina el término \(\delta T\) (turbulencia escalar térmica), lo que justifica modelar \(n\) como **escalar pasivo** mezclado por el flujo.

---

## 4. Procesos aleatorios: PSD y ergodicidad

Sea \(x(t)\) un **proceso aleatorio** real, de media \(\mu=\mathbb{E}[x(t)]\). 

### 4.1 Estacionaridad y autocovarianza
- **Estacionario estricto**: todas las distribuciones finito-dimensionales son invariantes ante traslaciones temporales.  
- **Estacionario en sentido amplio (WSS)**: media constante y autocovarianza que depende solo del **retardo** \(\tau\):
\[
R_x(\tau)=\mathbb{E}\!\big[(x(t)-\mu)(x(t+\tau)-\mu)\big].
\]

### 4.2 Densidad espectral de potencia (PSD)
Por el **teorema de Wiener–Khintchin**, la PSD \(S_x(\omega)\) es la transformada de Fourier de \(R_x(\tau)\):
\[
S_x(\omega) = \int_{-\infty}^{\infty} R_x(\tau)\, e^{-i\omega \tau}\, d\tau,
\qquad
R_x(\tau)=\frac{1}{2\pi}\int_{-\infty}^{\infty} S_x(\omega)\, e^{i\omega \tau}\, d\omega.
\]
Para **campos espaciales** \(X(\mathbf{x})\) (p.ej. \(\delta n\)), la generalización multivariada usa transformadas en \(\mathbf{k}\) y correlaciones \(B_X(\mathbf{r})\).

> **Estimación discreta (periodograma).** Con \(N\) muestras a \(\Delta t\) y DFT \(X_k\),
\[
\widehat{S}_x(f_k) = \frac{\Delta t}{N}\,|X_k|^2,\quad f_k=\frac{k}{N\Delta t},
\]
que suele suavizarse (promedios de Welch/multitaper) para reducir varianza.

### 4.3 Ergodicidad y promedios tiempo-conjunto
Un proceso WSS es **ergódico en media** si el promedio temporal coincide con el promedio de conjunto:
\[
\lim_{T\to\infty}\frac{1}{T}\!\int_0^T x(t)\,dt=\mathbb{E}[x(t)]\quad \text{c.s.}
\]
De forma análoga, hay ergodicidad en autocovarianza si
\[
\lim_{T\to\infty}\frac{1}{T}\!\int_0^T (x(t)-\mu)(x(t+\tau)-\mu)\,dt = R_x(\tau).
\]
En práctica, **ergodicidad + WSS** permiten **estimar \(S_x\)** a partir de **una sola realización larga** (p.ej. una serie temporal de irradiancia o de centroides).

### 4.4 Escalamiento espectral y Hurst (nota útil)
Si \(x\) es **fGn** (derivada en distribución de un fBm con exponente de Hurst \(H\in(0,1)\)), entonces para frecuencias bajas
\[
S_x(f) \propto f^{-(2H-1)}\quad (0.5<H<1),
\]
mientras que para el propio **fBm** vale \(S_{fBm}(f)\propto f^{-(2H+1)}\).  
Estas leyes conectan **PSD** con **memoria/persistencia** en procesos escalares usados en turbulencia óptica.

---

## 5. Resumen operativo

- **Navier–Stokes + \(Re\)** fijan el régimen y justifican la existencia de un **intervalo inercial**.  
- **K41** entrega leyes de escala universales (\(S_2\sim r^{2/3}\), \(E(k)\sim k^{-5/3}\)); **K62** corrige con **intermitencia**.  
- El **índice de refracción** se modela como **escalar pasivo** con
  \(D_n(r)=C_n^2 r^{2/3}\) y espectro \(\Phi_n(\kappa)\) tipo Kolmogórov/von Kármán (cortes \(L_0,l_0\)).  
- La **PSD** y la **ergodicidad** permiten estimar estadísticos de segunda orden a partir de realizaciones únicas (series temporales o mapas espaciales), conectando datos con teoría.

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
