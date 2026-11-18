# Laboratorio 4: Polinomios en Wolfram Alpha y SymPy
**Métodos Numéricos (2026-II) - Universidad Nacional de Colombia**

## Información del Estudiante
- **Nombre:** Juan Manuel Cristancho Alvarez
- **Usuario UNAL:** `jcristanchoa`
- **Correo Institucional:** `jcristanchoa@unal.edu.co`
- **Usuario GitHub:** `SajoOP`
- **Repositorio:** `MetNumUN2026II/Lab4`
- **Cuaderno Principal:** [`jcristanchoaSymPyLab4.ipynb`](./jcristanchoaSymPyLab4.ipynb)
- **Número de Lista:** **16**
- **Raíz Base Asignada ($16 \pmod{10}$):** $\mathbf{6}$

---
## Resumen de Ejemplos Desarrollados

### **My own example 1: Polinomio de Grado 10**
- **Raíz obligatoria:** $r_1 = 6$ ($16 \pmod{10}$).
- **Raíces adicionales (enteras y racionales):** $\{1, 2, 3, 4, 5, -1, -2, \frac{1}{2}, -\frac{1}{2}\}$.
- **Forma producto de monomios:**
  $$P_{10}(x) = (x - 6)(x - 1)(x - 2)(x - 3)(x - 4)(x - 5)(x + 1)(x + 2)\left(x - \frac{1}{2}\right)\left(x + \frac{1}{2}\right)$$
- **Forma extendida:**
  $$P_{10}(x) = x^{10} - 18x^9 + \frac{455}{4}x^8 - \frac{495}{2}x^7 - \frac{519}{2}x^6 + 1701x^5 - \frac{5065}{4}x^4 - \frac{3555}{2}x^3 + 1771x^2 + 342x - 360$$
- **Conteo de Operaciones ($n = 10$):**
  - **Extended Form:** $\frac{10 \cdot 11}{2} (*) + 10 (+) = 55 (*) + 10 (+) = \mathbf{65 \text{ operaciones}}$.
  - **Monomials Product Form:** $9 (*) + 10 (-) = \mathbf{19 \text{ operaciones}}$.
  - **Nested (Horner) Form:** $10 (*) + 10 (+) = \mathbf{20 \text{ operaciones}}$.

### **My own example 2: División por un Monomio que NO es parte del producto**
- **Monomio divisor:** $(x - 7)$ ($7$ no es raíz).
- **Cociente (grado 9):**
  $$Q_9(x) = x^9 - 11x^8 + \frac{147}{4}x^7 + \frac{39}{4}x^6 - \frac{765}{4}x^5 + \frac{1449}{4}x^4 + \frac{2539}{2}x^3 + 7109x^2 + 51534x + 361080$$
- **Residuo:** $R = \mathbf{2\,527\,200} \neq 0$.
- **Verificación Teorema del Resto:** $P_{10}(7) = 2\,527\,200$.

### **My own example 3: División Sucesiva por Cada Monomio del Producto**
- División paso a paso por $(x - 6), (x - 1), (x - 2), (x - 3), (x - 4), (x - 5), (x + 1), (x + 2), (x - 1/2), (x + 1/2)$.
- En cada paso el residuo es estrictamente $0$, reduciendo el grado en 1 hasta obtener el cociente final $Q(x) = 1$.

### **My own example 4: Factorización con SymPy**
- Factorización univariada exacta de $P_{10}(x)$ y de polinomios ciclotómicos / de grado superior como $x^{10} - 1024$ y $x^{12} - 1$.

### **My own example 5: Resolución de Ecuaciones con solveset**
- Resolución simbólica de $P_{10}(x) = 0$, recuperando exactamente el conjunto de raíces $\{-2, -1, -1/2, 1/2, 1, 2, 3, 4, 5, 6\}$.
- Resolución de ecuaciones polinómicas racionales como $x^{10} - \frac{1}{1024} = 0$.

### **My own example 6: Ecuaciones con Raíces Irracionales**
- Polinomio: $(x - \sqrt{5})(x - \pi)(x - \sqrt{2}) = 0$.
- Expansión simbólica, resolución sobre $\mathbb{R}$ y evaluación de alta precisión (25 cifras decimales).

### **My own example 7: Cuerpos Finitos / Campos de Galois GF(p)**
- Factorización de $x^{10} - 1$ sobre $\mathbb{Z}$, $\text{GF}(2)$, $\text{GF}(3)$, $\text{GF}(5)$ y $\text{GF}(7)$.
- Demostración del Endomorfismo de Frobenius en característica 5: $(x^2 - 1)^5 \equiv (x - 1)^5 (x + 1)^5 \pmod 5$.

### **My own example 8: Evaluaciones Complejas Simbólicas y Numéricas**
- Multiplicación y expansión de $z_1 \cdot z_2 \cdot z_3$ con separación de parte real e imaginaria.
- Evaluación numérica de $w = \frac{1}{e + \sqrt{2}i}$ y $w_2 = (1 + i\sqrt{3})^8 = -128 + 128\sqrt{3}i$ con 30 dígitos de precisión.

### **My own example 9: Consultas en Lenguaje Natural Wolfram Alpha vs ChatGPT**
- Distancia geodésica, coordenadas y tiempo de vuelo entre Bogotá y Tokio.
- Datos meteorológicos, altitud y precipitación en Bogotá en noviembre.
- Tabla comparativa entre el motor computacional y el modelo de lenguaje.

### **My own example 10: Integración Simbólica y Numérica**
- Integral indefinida: $\int x^2 \sin(x) e^x \, dx = \frac{e^x}{2}\left[(x^2 - 1)\sin(x) - (x - 1)^2 \cos(x)\right] + C$.
- Integral definida: $\int_0^{\pi} x^2 \sin(x) e^x \, dx = \frac{e^\pi(\pi - 1)^2 + 1}{2} \approx 53.5665$.
- Gráfica del área bajo la curva integrada.
