# 🔢 Ejercicios para Resolver - Álgebra Lineal

## 📋 Instrucciones Generales

- **Tiempo estimado total**: 4-5 horas
- **Dificultad**: Graduada de ⭐⭐☆☆☆ a ⭐⭐⭐⭐⭐
- **Herramientas**: Calculadora, MATLAB (opcional para verificación)
- **Formato**: Desarrolla completamente cada ejercicio mostrando todos los pasos

---

## 🎯 Ejercicio 1: Verificación de Subespacio Vectorial
**Dificultad**: ⭐⭐☆☆☆  
**Tiempo estimado**: 30 minutos  
**Competencias**: CB1, CE1

### Enunciado
Determina si los siguientes conjuntos son subespacios vectoriales de $\mathbb{R}^3$:

**a)** $W_1 = \{(x, y, z) \in \mathbb{R}^3 : x + 2y - z = 0\}$

**b)** $W_2 = \{(x, y, z) \in \mathbb{R}^3 : x^2 + y^2 + z^2 = 1\}$

**c)** $W_3 = \{(x, y, z) \in \mathbb{R}^3 : x \geq 0, y \geq 0, z \geq 0\}$

### Contexto de Ingeniería
En ingeniería química, $W_1$ podría representar el conjunto de composiciones que satisfacen una restricción de balance de materia, mientras que $W_2$ representa composiciones normalizadas y $W_3$ concentraciones físicamente realizables.

### Criterios de Evaluación
- Verificación correcta de los tres axiomas de subespacio
- Justificación clara de cada paso
- Interpretación del resultado en contexto de ingeniería

---

## 🧮 Ejercicio 2: Independencia Lineal en Sistemas de Reacciones
**Dificultad**: ⭐⭐⭐☆☆  
**Tiempo estimado**: 45 minutos  
**Competencias**: CE1, CT10

### Enunciado
En un reactor químico ocurren las siguientes reacciones con los componentes A, B, C, D, E:

1. $A + 2B \rightarrow C + D$
2. $2A + B \rightarrow 2C + E$  
3. $3A + 4B \rightarrow 3C + D + E$
4. $A + B \rightarrow C$

**a)** Escribe los vectores estequiométricos para cada reacción (considera el orden A, B, C, D, E).

**b)** Determina si las cuatro reacciones son linealmente independientes.

**c)** Si son dependientes, encuentra una relación de dependencia y explica su significado químico.

**d)** ¿Cuántas reacciones independientes hay realmente en este sistema?

### Ayuda
Recuerda que en los vectores estequiométricos, los reactivos tienen coeficientes negativos y los productos positivos.

### Criterios de Evaluación
- Correcta escritura de vectores estequiométricos
- Planteamiento y resolución del sistema homogéneo
- Interpretación química de la dependencia lineal
- Determinación del número de reacciones independientes

---

## 📊 Ejercicio 3: Base y Dimensión en Balances de Materia
**Dificultad**: ⭐⭐⭐☆☆  
**Tiempo estimado**: 50 minutos  
**Competencias**: CE1, CT12

### Enunciado
Considera un proceso de separación con 4 corrientes y 3 componentes (A, B, C). Las fracciones molares deben satisfacer:

$$\begin{cases}
x_{A1} + x_{B1} + x_{C1} = 1 \\
x_{A2} + x_{B2} + x_{C2} = 1 \\
x_{A3} + x_{B3} + x_{C3} = 1 \\
x_{A4} + x_{B4} + x_{C4} = 1
\end{cases}$$

Además, por balance global de cada componente:
$$\begin{cases}
F_1 x_{A1} + F_2 x_{A2} = F_3 x_{A3} + F_4 x_{A4} \\
F_1 x_{B1} + F_2 x_{B2} = F_3 x_{B3} + F_4 x_{B4} \\
F_1 x_{C1} + F_2 x_{C2} = F_3 x_{C3} + F_4 x_{C4}
\end{cases}$$

Donde $F_i$ son los flujos molares conocidos: $F_1 = 100$, $F_2 = 50$, $F_3 = 80$, $F_4 = 70$ kmol/h.

**a)** Plantea el sistema en forma matricial $\mathbf{A}\mathbf{x} = \mathbf{b}$.

**b)** Determina el rango de la matriz de coeficientes.

**c)** ¿Cuántos grados de libertad tiene el sistema?

**d)** Encuentra una base para el espacio nulo de $\mathbf{A}$.

### Criterios de Evaluación
- Correcta formulación matricial del problema
- Cálculo del rango usando eliminación gaussiana
- Determinación de grados de libertad
- Cálculo de base del espacio nulo

---

## 🎯 Ejercicio 4: Transformaciones Lineales en Procesos
**Dificultad**: ⭐⭐⭐⭐☆  
**Tiempo estimado**: 60 minutos  
**Competencias**: CE1, CT2

### Enunciado
En un proceso de destilación, la composición de salida $\mathbf{y}$ se relaciona con la composición de entrada $\mathbf{x}$ mediante una transformación lineal:

$$\mathbf{y} = \mathbf{T}\mathbf{x}$$

donde $\mathbf{T} = \begin{pmatrix} 0.8 & 0.1 & 0.1 \\ 0.15 & 0.7 & 0.15 \\ 0.05 & 0.2 & 0.75 \end{pmatrix}$

**a)** Verifica que $\mathbf{T}$ conserva la masa (suma de fracciones = 1).

**b)** Calcula los valores propios de $\mathbf{T}$.

**c)** Encuentra los vectores propios correspondientes.

**d)** ¿Qué representan físicamente los vectores propios en este contexto?

**e)** Si la alimentación es $\mathbf{x} = (0.4, 0.3, 0.3)^T$, calcula la composición de salida.

**f)** Usa MATLAB para verificar tus cálculos.

### Código MATLAB de Apoyo
```matlab
T = [0.8 0.1 0.1; 0.15 0.7 0.15; 0.05 0.2 0.75];
[V, D] = eig(T);  % Valores y vectores propios
x = [0.4; 0.3; 0.3];
y = T * x;  % Composición de salida
```

### Criterios de Evaluación
- Verificación de conservación de masa
- Cálculo correcto de valores propios
- Determinación de vectores propios
- Interpretación física de los resultados
- Uso apropiado de software

---

## 🔬 Ejercicio 5: Análisis de Estabilidad de Reactores
**Dificultad**: ⭐⭐⭐⭐☆  
**Tiempo estimado**: 70 minutos  
**Competencias**: CE1, CT10, CT12

### Enunciado
En un reactor CSTR con reacciones múltiples, la matriz jacobiana del sistema en el punto de equilibrio es:

$$\mathbf{J} = \begin{pmatrix} -2 & 1 & 0 \\ 1 & -3 & 1 \\ 0 & 2 & -1 \end{pmatrix}$$

**a)** Calcula el polinomio característico de $\mathbf{J}$.

**b)** Encuentra todos los valores propios.

**c)** Para cada valor propio real, calcula el vector propio correspondiente.

**d)** Determina si el punto de equilibrio es estable (todos los valores propios tienen parte real negativa).

**e)** Si hay valores propios complejos, calcula su parte real e imaginaria.

**f)** Interpreta el resultado en términos de estabilidad del reactor.

### Contexto Teórico
Un punto de equilibrio es estable si todos los valores propios de la matriz jacobiana tienen parte real negativa. Valores propios con parte real positiva indican inestabilidad.

### Criterios de Evaluación
- Cálculo correcto del polinomio característico
- Resolución de la ecuación característica
- Determinación de vectores propios
- Análisis de estabilidad
- Interpretación en contexto de ingeniería

---

## 🚀 Ejercicio 6: Problema Integrador (Opcional)
**Dificultad**: ⭐⭐⭐⭐⭐  
**Tiempo estimado**: 90 minutos  
**Competencias**: CE1, CT2, CT10, CT12

### Enunciado
Una planta química tiene 3 reactores en serie con recirculación. El sistema se describe mediante:

$$\frac{d\mathbf{c}}{dt} = \mathbf{A}\mathbf{c} + \mathbf{b}$$

donde $\mathbf{c} = (c_1, c_2, c_3)^T$ son las concentraciones en cada reactor, y:

$$\mathbf{A} = \begin{pmatrix} -3 & 0 & 1 \\ 2 & -4 & 0 \\ 0 & 3 & -2 \end{pmatrix}, \quad \mathbf{b} = \begin{pmatrix} 10 \\ 0 \\ 0 \end{pmatrix}$$

**a)** En estado estacionario ($\frac{d\mathbf{c}}{dt} = \mathbf{0}$), encuentra las concentraciones de equilibrio.

**b)** Analiza la estabilidad del punto de equilibrio.

**c)** Si el sistema se perturba ligeramente del equilibrio, ¿cómo evoluciona?

**d)** Calcula la matriz exponencial $e^{\mathbf{A}t}$ usando diagonalización.

**e)** Resuelve la ecuación diferencial completa con condición inicial $\mathbf{c}(0) = (5, 3, 2)^T$.

### Herramientas Recomendadas
- MATLAB/Octave para cálculos numéricos
- Verificación analítica de resultados
- Gráficas de evolución temporal

### Criterios de Evaluación
- Resolución del sistema en equilibrio
- Análisis completo de estabilidad
- Cálculo de matriz exponencial
- Solución de la ecuación diferencial
- Interpretación física de resultados

---

## 📚 Recursos de Apoyo

### Fórmulas Importantes
- **Polinomio característico**: $\det(\mathbf{A} - \lambda\mathbf{I}) = 0$
- **Rango de matriz**: Número de filas linealmente independientes
- **Dimensión del espacio nulo**: $n - \text{rango}(\mathbf{A})$

### Software Recomendado
- **MATLAB**: Para verificación de cálculos
- **Octave**: Alternativa libre
- **Python + NumPy**: Para programación científica

### Bibliografía
- David C. Lay - "Algebra lineal y sus aplicaciones", Cap. 1-5
- Eric Steiner - "Matemáticas para las ciencias aplicadas", Cap. 3

---

## ✅ Autoevaluación

Antes de revisar las soluciones, verifica que puedas:
- [ ] Identificar subespacios vectoriales
- [ ] Determinar independencia lineal
- [ ] Calcular valores y vectores propios
- [ ] Interpretar resultados en contexto de ingeniería
- [ ] Usar software para verificación

---

*Tiempo total estimado: 4-5 horas*  
*Recuerda: La práctica regular es clave para dominar el álgebra lineal*