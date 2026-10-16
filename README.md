# ⚖️ FactorLab — Entrenador Guiado de Factores de Conversión

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deploy-success?style=flat&logo=github)](https://pages.github.com/)
[![Materia](https://img.shields.io/badge/Física%20y%20Química-1º%20Bachillerato%20%2F%20ESO-indigo)](#)
[![Metodología](https://img.shields.io/badge/Aprendizaje-Guiado%20por%20Arrastre-blue)](#)
[![Idiomas](https://img.shields.io/badge/Idiomas-Català%20%7C%20Castellano-orange)](#)
[![Licencia](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-lightgrey)](#)

**FactorLab** es una aplicación web interactiva de código abierto (*Single-File*) diseñada para el **Departament de Física i Química del IEDIB** (Institut d'Ensenyaments a Distància de les Illes Balears). Su propósito es que el alumnado domine el método de los **factores de conversión** mediante un aprendizaje 100% guiado, manipulativo e interactivo, superando la memorización mecánica de fórmulas y la clásica «regla de tres».

---

## 🎯 Enfoque Pedagógico y Dinámica de Trabajo

La aplicación elimina la sobrecarga cognitiva concentrándose en una única vista limpia y estructurada en dos pasos secuenciales:

```
┌─────────────────────────────────────────────────────────────┐
│  Paso 1: Decisión estratégica inicial (elección múltiple)   │
└──────────────────────────────┬──────────────────────────────┘
                               ▼
┌─────────────────────────────────────────────────────────────┐
│  Paso 2: Arrastre interactivo de etiquetas (Drag & Drop)    │
│          y tachado visual en tiempo real de unidades        │
└──────────────────────────────┬──────────────────────────────┘
                               ▼
┌─────────────────────────────────────────────────────────────┐
│  Cálculo numérico final integrado junto al signo igual (=)  │
└─────────────────────────────────────────────────────────────┘
```

### 1. 🚀 Bloque de Física
* **Velocidad lineal ($km/h \leftrightarrow m/s$):** Encadenado simultáneo de factores de longitud ($1000\text{ m} = 1\text{ km}$) y tiempo ($3600\text{ s} = 1\text{ h}$).
* **Densidad con unidades volumétricas ($g/cm^3 \rightarrow kg/m^3$):** Manejo de potencias cúbicas ($10^6\text{ cm}^3 = 1\text{ m}^3$) para evitar el error habitual de no elevar al cubo la equivalencia decimal.
* **Presión de gases ($mmHg \rightarrow kPa$):** Paso en dos etapas ($760\text{ mmHg} = 1\text{ atm}$ y $1\text{ atm} = 101{,}3\text{ kPa}$).
* **Energía y potencia ($kW\cdot h \rightarrow kJ$):** Conversión de horas a segundos con equivalencia directa de potencia ($1\text{ kW}\cdot\text{s} = 1\text{ kJ}$).

### 2. 🧪 Bloque de Química
* **Masa a cantidad de sustancia ($g \rightarrow mol$):** Uso de la masa molar ($M_m$) de compuestos habituales ($\text{H}_2\text{O}$, $\text{NaOH}$, $\text{H}_2\text{SO}_4$, $\text{NaCl}$, $\text{CO}_2$, $\text{CaCO}_3$).
* **Volumen molar en c.n. ($g \rightarrow mol \rightarrow L$):** Conversión en dos factores encadenados utilizando los $22{,}4\text{ L/mol}$ a $0\text{ }^\circ\text{C}$ y $1\text{ atm}$.
* **Preparación de disoluciones ($mL \rightarrow L \rightarrow mol \rightarrow g$):** Tres factores encadenados desde el volumen de matraz hasta la masa de soluto puro a pesar en la balanza.
* **Reactivos comerciales concentrados ($mL \rightarrow g\text{ disolución} \rightarrow g\text{ soluto puro}$):** Distinción estricta entre soluto puro y disolución mediante la densidad ($\rho$) y el porcentaje en masa (% riqueza).

---

## ✨ Características Principales

* **Arrastre táctil con tachado visual en rojo:** Al soltar la etiqueta correcta en la casilla punteada, las unidades opuestas (tanto de los factores colocados como de la **tarjeta inicial**) se tachan automáticamente con una línea roja diagonal (`.unit-cancelled`).
* **Banco con distractores realistas:** Se incluyen etiquetas invertidas y relaciones dimensionales erróneas para forzar al estudiante a razonar qué unidad debe ir en el numerador y cuál en el denominador.
* **Recuadro de cálculo integrado:** El campo de introducción numérica se habilita únicamente cuando todas las unidades intermedias han sido canceladas, situado a la derecha del signo $=$ junto a la unidad final superviviente.
* **Tolerancia decimal automática:** El motor corrector admite un margen de redondeo del $\pm 3{,}5\%$ y acepta tanto coma como punto decimal.
* **Gamificación y seguimiento:**
  - Contador de **Aciertos** y récord de **Racha** consecutiva (🔥).
  - Cronómetro de sesión con pausa, reanudación y reinicio.
  - Desglose en tiempo real de ejercicios resueltos en Física y Química.
* **Informe oficial de auditoría en PDF:** Al pulsar *«Generar PDF de Sesión»*, se genera una ventana de impresión limpia con el nombre del estudiante, fecha, tiempo invertido y tabla completa de ejercicios para entregar en Moodle.
* **Bilingüe instantáneo:** Conmutador directo entre **Català** y **Castellano** en la cabecera.

---


## 🛠️ Tecnologías Empleadas

* **HTML5 semántico** y diseño totalmente responsive.
* **JavaScript estándar (Vanilla ES6+):** Motor algorítmico paramétrico y control de eventos Drag & Drop nativo.
* **Tailwind CSS (CDN):** Estilo visual limpio adaptado a pantallas de aula y dispositivos móviles.
* **KaTeX (CDN):** Renderizado tipográfico de alta velocidad para fórmulas matemáticas.
* **CSS Print API:** Generador de informes PDF de sesión sin dependencias externas pesadas.

---

## 📄 Autoría y Licencia

* **Autora:** Elena Ruiz Alfaro
* **Curso académico:** 2026-2027
* **Licencia:** [Creative Commons Reconeixement-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
