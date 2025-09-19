---
layout: default
title: Herramientas Estadísticas
permalink: /herramientas-estadisticas.html
---

# Herramientas Estadísticas

En este módulo se presentan las principales herramientas estadísticas para caracterizar la turbulencia óptica: densidad espectral de potencia (PSD), análisis de fluctuaciones detrendizadas (DFA), exponentes de Hurst y pruebas de gaussianidad/estacionariedad. También se incluyen los aportes de *Andrews & Phillips* sobre estadísticos ópticos clásicos (scintilación, coherencia, distribuciones de irradiancia).

---

## 1. Procesamiento y normalización de series temporales

Sea $x(t)$ una serie temporal de centroides, irradiancia o fase.  
- **Normalización**:  

$$
x'(t) = \frac{x(t)-\mu}{\sigma},
$$

con $\mu=\langle x(t)\rangle$ y $\sigma^2=\langle (x(t)-\mu)^2\rangle$.  

Esto facilita la comparación entre condiciones experimentales distintas.

---

## 2. Análisis espectral: PSD

La **densidad espectral de potencia** (PSD) describe cómo la varianza de $x(t)$ se distribuye en frecuencia $f$:

$$
S_x(f) = \int_{-\infty}^{\infty} R_x(\tau)\, e^{-i2\pi f\tau}\, d\tau,
$$

donde $R_x(\tau)$ es la autocorrelación.  

En turbulencia inercial se observa:

$$
S_x(f) \propto f^{-\beta}, \quad \beta \approx \tfrac{5}{3}.
$$

Esto conecta con las leyes de Kolmogórov.

---

## 3. Detrended Fluctuation Analysis (DFA)

El método DFA permite detectar **memoria de largo alcance** incluso en series no estacionarias.

1. Se construye la “caminata integrada”:

$$
Y(k) = \sum_{i=1}^k (x(i)-\mu).
$$

2. Se divide en segmentos de tamaño $s$, y en cada segmento se ajusta una tendencia polinómica local.  

3. Se calcula la varianza promedio de las desviaciones respecto a la tendencia:

$$
F^2(s) = \frac{1}{N}\sum_{k=1}^N \left[ Y(k)-Y_{\text{fit}}(k;s) \right]^2.
$$

4. Se obtiene la ley de escala:

$$
F(s) \propto s^H,
$$

donde $H$ es el **exponente de Hurst**.

- $H=0.5$: proceso aleatorio sin memoria (fGn).  
- $H>0.5$: persistencia.  
- $H<0.5$: antipersistencia.

---

## 4. Comparación PSD vs DFA

Ambos métodos caracterizan memoria y escalamiento:

- PSD: $S(f)\propto f^{-\beta}$ con $\beta = 2H-1$ (para fGn).  
- DFA: $F(s)\propto s^H$ directamente en el dominio temporal.  

La combinación valida la robustez de los resultados.

---

## 5. Pruebas de hipótesis estadísticas

Para evaluar la validez de modelos gaussianos y estacionarios:

- **Test de normalidad**: Kolmogórov–Smirnov, Anderson–Darling, Shapiro–Wilk.  
- **Test de independencia**: autocorrelación parcial, Ljung–Box.  
- **Test de estacionariedad**: ADF (Augmented Dickey–Fuller), KPSS.

Estos tests permiten descartar supuestos antes de aplicar modelos.

---

## 6. Aportes de *Andrews & Phillips*

*Andrews & Phillips* aportan expresiones estadísticas específicas para óptica de propagación:

- **Índice de scintilación**:

$$
\sigma_I^2 = \frac{\langle I^2 \rangle - \langle I \rangle^2}{\langle I \rangle^2},
$$

donde $I$ es la intensidad/irradiancia.

- **Mutual coherence function** (coherencia de segundo orden):

$$
\Gamma(\mathbf{r_1},\mathbf{r_2}) = \langle U(\mathbf{r_1})\,U^*(\mathbf{r_2}) \rangle,
$$

con $U$ el campo complejo.

- **Distribuciones de irradiancia**:  
  - Log-normal (turbulencia débil).  
  - Gamma-Gamma (turbulencia moderada/fuerte).  

Estas descripciones son base para el diseño de enlaces ópticos.

---

## 7. Resumen operativo

- La **PSD** revela leyes de escala en frecuencia ($f^{-5/3}$).  
- El **DFA** estima el exponente de Hurst y detecta multiescala.  
- Las **pruebas estadísticas** validan o rechazan hipótesis gaussianas/estacionarias.  
- *Andrews & Phillips* proporcionan métricas ópticas clásicas (scintilación, coherencia, distribuciones), integrables con el análisis estocástico moderno.

---

[⬅️ Volver al menú principal]({{ '/' | relative_url }})
