---
layout: page
title: Scientific Engine
---

BlastCAD is powered by a robust, deterministic scientific backend engine designed to provide accurate predictions for rock fragmentation, ground vibration, and blast geometry. The engine leverages industry-standard empirical models and established blasting theories to ensure safety and optimize operational efficiency.

## 1. Fragmentation Analysis (Kuz-Ram Model)

BlastCAD utilizes the **Kuznetsov-Cunningham-Rosin-Rammler (Kuz-Ram)** model to predict the fragment size distribution of the blasted rock.

### Mean Fragment Size (Kuznetsov Equation)
The mean fragment size ($x_{mean}$) is calculated using Kuznetsov's original equation (1973), modified by Cunningham (1983) to account for different explosive strengths:

$$ x_{mean} = A \times \left(\frac{V}{Q}\right)^{0.8} \times \left(Q \times \frac{RWS}{115}\right)^{\frac{1}{6}} $$

* **$A$**: Rock Factor (e.g., 7 for very hard rock, 13+ for soft rock).
* **$V$**: Breakage volume per hole ($m^3$).
* **$Q$**: Charge mass per hole ($kg$).
* **$RWS$**: Relative Weight Strength of the explosive (ANFO = 100).

### Size Distribution (Rosin-Rammler Curve)
To generate the cumulative passing percentage for any given screen size, the engine applies the Rosin-Rammler (1933) distribution:

$$ P(x) = \left[ 1 - e^{-\left(\frac{x}{x_c}\right)^n} \right] \times 100 $$

* **$P(x)$**: Percentage of rock passing through screen size $x$.
* **$x_c$**: Characteristic size, derived from $x_{mean}$ and the uniformity index.
* **$n$**: Uniformity Index, defining the spread of the size distribution.

*BlastCAD automatically calculates key performance indicators such as **P80, P50, and P20** passing sizes.*

## 2. Vibration & PPV Analysis

Ground vibration is a critical safety parameter. BlastCAD predicts Peak Particle Velocity (PPV) based on the **Attewell & Farmer (1976)** model, ensuring compliance with standards such as **AS 2187.2-2006**.

### Peak Particle Velocity (PPV)
$$ PPV = K \times \left( \frac{R}{\sqrt{MIC}} \right)^{-\alpha} $$

* **$K$**: Site-specific transmission constant (Default: 1140).
* **$\alpha$**: Site-specific attenuation exponent (Default: 1.6).
* **$R$**: Distance to the monitoring point ($m$).
* **$MIC$**: Maximum Instantaneous Charge ($kg$).

The engine also calculates the **Minimum Safe Distance** to ensure vibrations do not exceed user-defined regulatory limits.

## 3. Livingston Crater Theory & Radius

To prevent underloading or overloading, the engine calculates the critical and breakage radii for each individually charged hole using **Livingston's Crater Theory**.

$$ R_c = C_b \times Q^{\frac{1}{3}} $$

* **$R_c$**: Critical Radius ($m$).
* **$C_b$**: Strain energy factor (Default rock constant: 0.84).
* **$Q$**: Charge mass ($kg$).

*BlastCAD uses these theoretical radii to recommend optimal **Burden** and **Spacing** values automatically.*

---
**References:**
1. Kuznetsov, A. (1973). *The mean diameter of the fragments formed by blasting rock.*
2. Cunningham, C.V.B. (1983). *The Kuz-Ram model for prediction of fragmentation from blasting.*
3. Rosin, P. & Rammler, E. (1933). *The laws governing the fineness of powdered coal.*
4. Attewell, P.B. & Farmer, I.W. (1976). *Principles of Engineering Geology.*
5. Langefors, U. & Kihlström, B. (1963). *The Modern Technique of Rock Blasting.*