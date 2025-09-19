---
layout: default
title: Campos Escalares Pasivos e Índice de Refracción
permalink: /campos-escalares.html
---

# Campos Escalares Pasivos e Índice de Refracción

Este módulo trata el papel de los **campos escalares** (como la temperatura o trazadores pasivos) en la turbulencia, y cómo estas ideas se trasladan al **índice de refracción atmosférico**. Además, se presentan los aportes clásicos de *Andrews & Phillips* sobre perfiles $C_n^2(h)$ y espectros de refracción.

---

## 1. Campo escalar pasivo

Un **campo escalar pasivo** $\theta(\mathbf{x},t)$ (ej. temperatura, concentración de contaminantes) obedece la ecuación de advección-difusión:

$$
\frac{\partial \theta}{\partial t} + \mathbf{u}\cdot\nabla \theta
= \kappa \nabla^2 \theta + S,
$$

donde $\mathbf{u}(\mathbf{x},t)$ es el campo de velocidades, $\kappa$ la difusividad escalar y $S$ una fuente.  
El término “pasivo” indica que $\theta$ **no retroalimenta** a $\mathbf{u}$, sino que es transportado por el flujo.

- Para escalas en el rango inercial, Obukhov y Corrsin (1949, 1951) postularon la ley:

$$
D_\theta(r) = \langle [\theta(\mathbf{x}+\mathbf{r})-\theta(\mathbf{x})]^2 \rangle
\propto (\varepsilon_\theta \, \varepsilon^{-1/3})\, r^{2/3},
$$

con $\varepsilon_\theta$ la tasa de disipación escalar y $\varepsilon$ la de energía cinética.

---

## 2. Modelo de Kraichnan y escalamiento anómalo

El **modelo de Kraichnan** (1968) supone un campo de velocidades gaussiano, delta-correlacionado en tiempo:

$$
\langle u_i(\mathbf{x},t)\,u_j(\mathbf{x}',t') \rangle
= D_{ij}(\mathbf{x}-\mathbf{x}') \, \delta(t-t').
$$

Bajo este supuesto:
- El problema se hace analíticamente tratable.
- Se predice **escalamiento anómalo** en las funciones de estructura escalares:

$$
S_p^\theta(r) = \langle |\theta(\mathbf{x}+\mathbf{r})-\theta(\mathbf{x})|^p \rangle
\propto r^{\zeta_p^\theta},
$$

con exponentes $\zeta_p^\theta$ no triviales (desviaciones del valor dimensional $p/3$).  
Este resultado explica la **intermitencia** observada en campos escalares pasivos.

---

## 3. Índice de refracción turbulento como proceso estocástico

El índice de refracción $n(\mathbf{x},t)$ depende de presión y temperatura.  
En la atmósfera estándar, se aproxima:

$$
n-1 \approx K(\lambda)\,\frac{P}{T},
$$

donde $P$ es la presión, $T$ la temperatura y $K(\lambda)$ un coeficiente débilmente dependiente de la longitud de onda.

- Las fluctuaciones $\delta n$ se modelan como **escalar pasivo** transportado por la turbulencia.  
- Se han usado modelos de **movimiento browniano fraccional (fBm)**:

$$
\langle [n(x+r)-n(x)]^2 \rangle \propto r^{2H},
$$

donde $H$ es el **exponente de Hurst** ($H=1/3$ en el modelo de Kolmogórov clásico, $H\neq 1/3$ cuando hay intermitencia o anisotropía).  
- Este marco conecta estadística de turbulencia con procesos estocásticos.

---

## 4. Aportes de *Andrews & Phillips*

El libro *Laser Beam Propagation through Random Media* (Andrews & Phillips) es referencia clave para aplicaciones ópticas. Sus aportes relevantes aquí son:

- **Perfil vertical $C_n^2(h)$**  
  El parámetro de estructura se modela como función de la altura $h$:

  $$
  C_n^2(h) \sim \text{función decreciente de } h,
  $$

  con diferentes modelos empíricos para capa límite, atmósfera libre y estratosfera.  
  Ejemplo típico para la superficie:

  $$
  C_n^2(h) = C_{n0}^2 \, \exp\!\left(-\frac{h}{H}\right),
  $$

  donde $H$ es una altura de decaimiento característica.

- **Espectros de refracción**  
  Presentan el espectro de Kolmogórov:

  $$
  \Phi_n(\kappa) = 0.033 \, C_n^2 \, \kappa^{-11/3},
  $$

  y su extensión de von Kármán con cortes interior/exterior:

  $$
  \Phi_n(\kappa) = 0.033\, C_n^2 \, (\kappa^2+\kappa_0^2)^{-11/6}
  \exp\!\left(-\kappa^2/\kappa_m^2\right).
  $$

- **Turbulencia no homogénea**  
  Reconocen que $C_n^2$ varía en espacio y tiempo, y proponen parametrizaciones para diferentes entornos atmosféricos.

---

## 5. Resumen operativo

- Los **campos escalares pasivos** explican cómo gradientes de temperatura se mezclan en la turbulencia.  
- El **modelo de Kraichnan** muestra que surgen **exponentes anómalos**.  
- El **índice de refracción** se interpreta como un **fBm**, con $H$ como descriptor de persistencia y memoria.  
- *Andrews & Phillips* aportan la base empírica: **perfiles $C_n^2(h)$** y **espectros de refracción**, fundamentales para aplicaciones ópticas.

---

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
