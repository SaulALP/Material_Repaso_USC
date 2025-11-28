# ✅ Ejercicios Resueltos - Álgebra Lineal

## 📋 Información General

- **Tema**: Álgebra Lineal aplicada a Ingeniería Química
- **Nivel**: Intermedio-Avanzado
- **Tiempo de estudio**: 3-4 horas
- **Competencias**: CE1, CT10, CT12

---

## 🎯 Ejercicio 1: Verificación de Subespacio Vectorial
**Dificultad**: ⭐⭐☆☆☆  
**Tiempo**: 25 minutos  
**Tema**: Subespacios vectoriales

### Enunciado
Determina si el conjunto $W = \{(x, y, z) \in \mathbb{R}^3 : 2x - y + 3z = 0\}$ es un subespacio vectorial de $\mathbb{R}^3$.

### Solución Completa

Para que $W$ sea un subespacio vectorial de $\mathbb{R}^3$, debe cumplir tres condiciones:
1. $\mathbf{0} \in W$
2. Cerradura bajo la suma
3. Cerradura bajo el producto por escalar

**Verificación 1: Elemento neutro**

Necesitamos verificar si $(0, 0, 0) \in W$:
$$2(0) - (0) + 3(0) = 0 + 0 + 0 = 0 \checkmark$$

Por tanto, $\mathbf{0} \in W$.

**Verificación 2: Cerradura bajo la suma**

Sean $\mathbf{u} = (x_1, y_1, z_1), \mathbf{v} = (x_2, y_2, z_2) \in W$.

Esto significa:
- $2x_1 - y_1 + 3z_1 = 0$
- $2x_2 - y_2 + 3z_2 = 0$

Necesitamos verificar si $\mathbf{u} + \mathbf{v} = (x_1 + x_2, y_1 + y_2, z_1 + z_2) \in W$:

$$2(x_1 + x_2) - (y_1 + y_2) + 3(z_1 + z_2)$$
$$= 2x_1 + 2x_2 - y_1 - y_2 + 3z_1 + 3z_2$$
$$= (2x_1 - y_1 + 3z_1) + (2x_2 - y_2 + 3z_2)$$
$$= 0 + 0 = 0 \checkmark$$

Por tanto, $\mathbf{u} + \mathbf{v} \in W$.

**Verificación 3: Cerradura bajo producto por escalar**

Sea $\mathbf{v} = (x, y, z) \in W$ y $\alpha \in \mathbb{R}$.

Sabemos que $2x - y + 3z = 0$.

Necesitamos verificar si $\alpha\mathbf{v} = (\alpha x, \alpha y, \alpha z) \in W$:

$$2(\alpha x) - (\alpha y) + 3(\alpha z)$$
$$= \alpha(2x - y + 3z)$$
$$= \alpha \cdot 0 = 0 \checkmark$$

Por tanto, $\alpha\mathbf{v} \in W$.

### Conclusión
Como $W$ satisface las tres condiciones, **$W$ es un subespacio vectorial de $\mathbb{R}^3$**.

### Interpretación Geométrica
$W$ representa un plano que pasa por el origen con vector normal $\mathbf{n} = (2, -1, 3)$.

### Aplicación en Ingeniería Química
Este tipo de subespacio aparece en restricciones de balance de materia. Por ejemplo, si $x$, $y$, $z$ representan flujos molares de tres corrientes, la ecuación $2x - y + 3z = 0$ podría representar un balance global de un componente específico.

---

## 🧮 Ejercicio 2: Independencia Lineal en Sistemas de Reacciones
**Dificultad**: ⭐⭐⭐☆☆  
**Tiempo**: 35 minutos  
**Tema**: Independencia lineal, aplicaciones químicas

### Enunciado
En un reactor químico ocurren las siguientes reacciones con componentes A, B, C, D:

1. $A + 2B \rightarrow C$
2. $2A + B \rightarrow D$  
3. $3A + 4B \rightarrow C + D$

Determina si las tres reacciones son linealmente independientes.

### Solución Completa

**Paso 1: Escribir los vectores estequiométricos**

Para cada reacción, escribimos el vector estequiométrico en el orden (A, B, C, D):

- Reacción 1: $A + 2B \rightarrow C$  
  $\mathbf{r}_1 = (-1, -2, 1, 0)$

- Reacción 2: $2A + B \rightarrow D$  
  $\mathbf{r}_2 = (-2, -1, 0, 1)$

- Reacción 3: $3A + 4B \rightarrow C + D$  
  $\mathbf{r}_3 = (-3, -4, 1, 1)$

**Paso 2: Plantear la ecuación de dependencia lineal**

Los vectores son linealmente independientes si la única solución de:
$$\alpha_1\mathbf{r}_1 + \alpha_2\mathbf{r}_2 + \alpha_3\mathbf{r}_3 = \mathbf{0}$$

es $\alpha_1 = \alpha_2 = \alpha_3 = 0$.

**Paso 3: Escribir el sistema de ecuaciones**

$$\alpha_1(-1, -2, 1, 0) + \alpha_2(-2, -1, 0, 1) + \alpha_3(-3, -4, 1, 1) = (0, 0, 0, 0)$$

Esto nos da el sistema:
$$\begin{cases}
-\alpha_1 - 2\alpha_2 - 3\alpha_3 = 0 \quad \text{(Balance de A)} \\
-2\alpha_1 - \alpha_2 - 4\alpha_3 = 0 \quad \text{(Balance de B)} \\
\alpha_1 + 0\alpha_2 + \alpha_3 = 0 \quad \text{(Balance de C)} \\
0\alpha_1 + \alpha_2 + \alpha_3 = 0 \quad \text{(Balance de D)}
\end{cases}$$

**Paso 4: Resolver el sistema por eliminación gaussiana**

Matriz aumentada del sistema homogéneo:
$$\begin{pmatrix}
-1 & -2 & -3 & | & 0 \\
-2 & -1 & -4 & | & 0 \\
1 & 0 & 1 & | & 0 \\
0 & 1 & 1 & | & 0
\end{pmatrix}$$

Aplicando operaciones elementales:

$F_1 \leftarrow -F_1$:
$$\begin{pmatrix}
1 & 2 & 3 & | & 0 \\
-2 & -1 & -4 & | & 0 \\
1 & 0 & 1 & | & 0 \\
0 & 1 & 1 & | & 0
\end{pmatrix}$$

$F_2 \leftarrow F_2 + 2F_1$, $F_3 \leftarrow F_3 - F_1$:
$$\begin{pmatrix}
1 & 2 & 3 & | & 0 \\
0 & 3 & 2 & | & 0 \\
0 & -2 & -2 & | & 0 \\
0 & 1 & 1 & | & 0
\end{pmatrix}$$

$F_3 \leftarrow F_3 + \frac{2}{3}F_2$:
$$\begin{pmatrix}
1 & 2 & 3 & | & 0 \\
0 & 3 & 2 & | & 0 \\
0 & 0 & -\frac{2}{3} & | & 0 \\
0 & 1 & 1 & | & 0
\end{pmatrix}$$

De la tercera fila: $-\frac{2}{3}\alpha_3 = 0 \Rightarrow \alpha_3 = 0$

De la cuarta fila: $\alpha_2 + \alpha_3 = 0 \Rightarrow \alpha_2 = 0$

De la primera fila: $\alpha_1 + 2\alpha_2 + 3\alpha_3 = 0 \Rightarrow \alpha_1 = 0$

**Paso 5: Verificación mediante determinante**

Alternativamente, podemos formar la matriz con los vectores como columnas:
$$\mathbf{A} = \begin{pmatrix}
-1 & -2 & -3 \\
-2 & -1 & -4 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{pmatrix}$$

Como $\mathbf{A}$ es $4 \times 3$, calculamos $\det(\mathbf{A}^T\mathbf{A})$:

$$\mathbf{A}^T\mathbf{A} = \begin{pmatrix}
-1 & -2 & 1 & 0 \\
-2 & -1 & 0 & 1 \\
-3 & -4 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
-1 & -2 & -3 \\
-2 & -1 & -4 \\
1 & 0 & 1 \\
0 & 1 & 1
\end{pmatrix}$$

$$= \begin{pmatrix}
6 & 4 & 10 \\
4 & 6 & 11 \\
10 & 11 & 27
\end{pmatrix}$$

$$\det(\mathbf{A}^T\mathbf{A}) = 6 \begin{vmatrix} 6 & 11 \\ 11 & 27 \end{vmatrix} - 4 \begin{vmatrix} 4 & 11 \\ 10 & 27 \end{vmatrix} + 10 \begin{vmatrix} 4 & 6 \\ 10 & 11 \end{vmatrix}$$

$$= 6(162 - 121) - 4(108 - 110) + 10(44 - 60)$$
$$= 6(41) - 4(-2) + 10(-16)$$
$$= 246 + 8 - 160 = 94 \neq 0$$

### Conclusión
Como la única solución del sistema homogéneo es la trivial, **las tres reacciones son linealmente independientes**.

### Interpretación Química
Las tres reacciones son fundamentalmente diferentes y ninguna puede expresarse como combinación lineal de las otras dos. Esto significa que las tres reacciones proporcionan información independiente sobre el sistema químico.

### Verificación con MATLAB
```matlab
% Vectores estequiométricos como columnas
A = [-1 -2 -3; -2 -1 -4; 1 0 1; 0 1 1];
rank(A)  % Debe dar 3
det(A'*A)  % Debe ser ≠ 0
```

---

## 📊 Ejercicio 3: Base y Dimensión en Balances de Materia
**Dificultad**: ⭐⭐⭐⭐☆  
**Tiempo**: 45 minutos  
**Tema**: Base, dimensión, aplicaciones en procesos

### Enunciado
Un proceso de separación tiene 4 corrientes con 3 componentes (A, B, C). Las fracciones molares deben satisfacer las restricciones de normalización y los balances globales. Determina:

a) La dimensión del espacio de estados válidos
b) Una base para este espacio
c) Los grados de libertad del sistema

**Datos**: 
- Corrientes: Alimentación (1), Destilado (2), Fondos (3), Reflujo (4)
- Flujos conocidos: $F_1 = 100$, $F_2 = 60$, $F_3 = 40$, $F_4 = 20$ kmol/h

### Solución Completa

**Paso 1: Definir las variables del sistema**

Variables: $x_{ij}$ = fracción molar del componente $i$ en la corriente $j$

$$\mathbf{x} = \begin{pmatrix}
x_{A1} \\ x_{B1} \\ x_{C1} \\
x_{A2} \\ x_{B2} \\ x_{C2} \\
x_{A3} \\ x_{B3} \\ x_{C3} \\
x_{A4} \\ x_{B4} \\ x_{C4}
\end{pmatrix} \in \mathbb{R}^{12}$$

**Paso 2: Escribir las restricciones**

**Restricciones de normalización** (4 ecuaciones):
$$\begin{cases}
x_{A1} + x_{B1} + x_{C1} = 1 \\
x_{A2} + x_{B2} + x_{C2} = 1 \\
x_{A3} + x_{B3} + x_{C3} = 1 \\
x_{A4} + x_{B4} + x_{C4} = 1
\end{cases}$$

**Balances globales** (3 ecuaciones):
$$\begin{cases}
F_1 x_{A1} = F_2 x_{A2} + F_3 x_{A3} \quad \text{(Balance de A)} \\
F_1 x_{B1} = F_2 x_{B2} + F_3 x_{B3} \quad \text{(Balance de B)} \\
F_1 x_{C1} = F_2 x_{C2} + F_3 x_{C3} \quad \text{(Balance de C)}
\end{cases}$$

Sustituyendo los flujos:
$$\begin{cases}
100 x_{A1} = 60 x_{A2} + 40 x_{A3} \\
100 x_{B1} = 60 x_{B2} + 40 x_{B3} \\
100 x_{C1} = 60 x_{C2} + 40 x_{C3}
\end{cases}$$

**Paso 3: Formar la matriz del sistema**

El sistema completo es $\mathbf{A}\mathbf{x} = \mathbf{b}$ donde:

$$\mathbf{A} = \begin{pmatrix}
1 & 1 & 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 1 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 1 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 1 & 1 \\
100 & 0 & 0 & -60 & 0 & 0 & -40 & 0 & 0 & 0 & 0 & 0 \\
0 & 100 & 0 & 0 & -60 & 0 & 0 & -40 & 0 & 0 & 0 & 0 \\
0 & 0 & 100 & 0 & 0 & -60 & 0 & 0 & -40 & 0 & 0 & 0
\end{pmatrix}$$

$$\mathbf{b} = \begin{pmatrix} 1 \\ 1 \\ 1 \\ 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}$$

**Paso 4: Calcular el rango de la matriz de coeficientes**

Aplicando eliminación gaussiana a $\mathbf{A}$:

Después de las operaciones elementales, obtenemos:
$$\text{rango}(\mathbf{A}) = 6$$

**Paso 5: Determinar la dimensión del espacio de soluciones**

Para el sistema homogéneo asociado $\mathbf{A}\mathbf{x} = \mathbf{0}$:
$$\dim(\text{Ker}(\mathbf{A})) = 12 - 6 = 6$$

**Paso 6: Encontrar una base para el espacio nulo**

Resolviendo $\mathbf{A}\mathbf{x} = \mathbf{0}$, encontramos que las variables libres pueden ser:
$x_{A4}, x_{B4}, x_{C4}, x_{A2}, x_{B2}, x_{C2}$

Una base para $\text{Ker}(\mathbf{A})$ es:

$$\mathcal{B} = \left\{
\begin{pmatrix} 0.6 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0.4 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \end{pmatrix},
\begin{pmatrix} 0 \\ 0.6 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0.4 \\ 0 \\ 0 \\ 0 \\ 0 \end{pmatrix},
\begin{pmatrix} 0 \\ 0 \\ 0.6 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0.4 \\ 0 \\ 0 \\ 0 \end{pmatrix},
\ldots
\right\}$$

**Paso 7: Análisis de grados de libertad**

- **Variables totales**: 12
- **Ecuaciones independientes**: 6
- **Grados de libertad**: $12 - 6 = 6$

### Respuestas

a) **Dimensión del espacio de estados válidos**: 6

b) **Base**: Los 6 vectores encontrados en el paso 6

c) **Grados de libertad**: 6

### Interpretación Física

El sistema tiene 6 grados de libertad, lo que significa que necesitamos especificar 6 variables independientes para determinar completamente el estado del proceso. Por ejemplo, podríamos especificar las composiciones del destilado ($x_{A2}, x_{B2}, x_{C2}$) y del reflujo ($x_{A4}, x_{B4}, x_{C4}$).

### Verificación con MATLAB
```matlab
% Matriz de coeficientes
A = [1 1 1 0 0 0 0 0 0 0 0 0;
     0 0 0 1 1 1 0 0 0 0 0 0;
     0 0 0 0 0 0 1 1 1 0 0 0;
     0 0 0 0 0 0 0 0 0 1 1 1;
     100 0 0 -60 0 0 -40 0 0 0 0 0;
     0 100 0 0 -60 0 0 -40 0 0 0 0;
     0 0 100 0 0 -60 0 0 -40 0 0 0];

rank(A)  % Debe dar 6
null(A)  % Base del espacio nulo
```

---

## 🎯 Ejercicio 4: Valores Propios en Análisis de Estabilidad
**Dificultad**: ⭐⭐⭐⭐☆  
**Tiempo**: 40 minutos  
**Tema**: Valores propios, estabilidad de sistemas

### Enunciado
Un reactor CSTR con reacciones en serie $A \rightarrow B \rightarrow C$ tiene la matriz jacobiana:

$$\mathbf{J} = \begin{pmatrix}
-3 & 0 & 0 \\
2 & -4 & 0 \\
0 & 3 & -1
\end{pmatrix}$$

Analiza la estabilidad del punto de equilibrio.

### Solución Completa

**Paso 1: Calcular el polinomio característico**

$$p(\lambda) = \det(\mathbf{J} - \lambda\mathbf{I}) = \det\begin{pmatrix}
-3-\lambda & 0 & 0 \\
2 & -4-\lambda & 0 \\
0 & 3 & -1-\lambda
\end{pmatrix}$$

Como la matriz es triangular superior, el determinante es el producto de los elementos diagonales:
$$p(\lambda) = (-3-\lambda)(-4-\lambda)(-1-\lambda)$$

**Paso 2: Encontrar los valores propios**

$$p(\lambda) = 0 \Rightarrow (-3-\lambda)(-4-\lambda)(-1-\lambda) = 0$$

Los valores propios son:
- $\lambda_1 = -3$
- $\lambda_2 = -4$  
- $\lambda_3 = -1$

**Paso 3: Análisis de estabilidad**

Para que el punto de equilibrio sea estable, todos los valores propios deben tener parte real negativa.

En nuestro caso:
- $\text{Re}(\lambda_1) = -3 < 0$ ✓
- $\text{Re}(\lambda_2) = -4 < 0$ ✓
- $\text{Re}(\lambda_3) = -1 < 0$ ✓

**Conclusión**: El punto de equilibrio es **asintóticamente estable**.

**Paso 4: Encontrar los vectores propios**

Para $\lambda_1 = -3$:
$$(\mathbf{J} - (-3)\mathbf{I})\mathbf{v}_1 = \mathbf{0}$$
$$\begin{pmatrix}
0 & 0 & 0 \\
2 & -1 & 0 \\
0 & 3 & 2
\end{pmatrix}\mathbf{v}_1 = \mathbf{0}$$

Resolviendo: $\mathbf{v}_1 = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$

Para $\lambda_2 = -4$:
$$\begin{pmatrix}
1 & 0 & 0 \\
2 & 0 & 0 \\
0 & 3 & 3
\end{pmatrix}\mathbf{v}_2 = \mathbf{0}$$

Resolviendo: $\mathbf{v}_2 = \begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix}$

Para $\lambda_3 = -1$:
$$\begin{pmatrix}
-2 & 0 & 0 \\
2 & -3 & 0 \\
0 & 3 & 0
\end{pmatrix}\mathbf{v}_3 = \mathbf{0}$$

Resolviendo: $\mathbf{v}_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}$

**Paso 5: Interpretación física**

Los valores propios representan las constantes de tiempo características:
- $\tau_1 = \frac{1}{|\lambda_1|} = \frac{1}{3}$ (modo más rápido)
- $\tau_2 = \frac{1}{|\lambda_2|} = \frac{1}{4}$ (modo intermedio)
- $\tau_3 = \frac{1}{|\lambda_3|} = 1$ (modo más lento)

El sistema se aproxima al equilibrio con una constante de tiempo dominante de $\tau_3 = 1$.

### Verificación con MATLAB
```matlab
J = [-3 0 0; 2 -4 0; 0 3 -1];
[V, D] = eig(J);
eigenvalues = diag(D)
eigenvectors = V
```

---

## 📈 Ejercicio 5: Problema Integrador - Optimización de Reactor
**Dificultad**: ⭐⭐⭐⭐⭐  
**Tiempo**: 60 minutos  
**Tema**: Aplicación integral de álgebra lineal

### Enunciado
Un complejo petroquímico tiene 3 reactores en paralelo que procesan una mezcla de hidrocarburos. El sistema se describe mediante:

$$\frac{d\mathbf{c}}{dt} = \mathbf{A}\mathbf{c} + \mathbf{B}\mathbf{u} + \mathbf{f}$$

donde:
- $\mathbf{c} = (c_1, c_2, c_3)^T$: concentraciones en cada reactor
- $\mathbf{u} = (u_1, u_2)^T$: variables de control (flujos de alimentación)
- $\mathbf{f}$: perturbaciones externas

$$\mathbf{A} = \begin{pmatrix}
-2 & 0.5 & 0.2 \\
0.8 & -3 & 0.1 \\
0.3 & 0.7 & -1.5
\end{pmatrix}, \quad \mathbf{B} = \begin{pmatrix}
1 & 0 \\
0 & 1 \\
0.5 & 0.3
\end{pmatrix}$$

Analiza:
a) Estabilidad del sistema
b) Controlabilidad
c) Estado estacionario óptimo

### Solución Completa

**Parte a: Análisis de Estabilidad**

**Paso 1: Calcular valores propios de $\mathbf{A}$**

Polinomio característico:
$$p(\lambda) = \det(\mathbf{A} - \lambda\mathbf{I})$$

$$= \det\begin{pmatrix}
-2-\lambda & 0.5 & 0.2 \\
0.8 & -3-\lambda & 0.1 \\
0.3 & 0.7 & -1.5-\lambda
\end{pmatrix}$$

Expandiendo por la primera fila:
$$p(\lambda) = (-2-\lambda)\det\begin{pmatrix} -3-\lambda & 0.1 \\ 0.7 & -1.5-\lambda \end{pmatrix} - 0.5\det\begin{pmatrix} 0.8 & 0.1 \\ 0.3 & -1.5-\lambda \end{pmatrix} + 0.2\det\begin{pmatrix} 0.8 & -3-\lambda \\ 0.3 & 0.7 \end{pmatrix}$$

$$= (-2-\lambda)[(-3-\lambda)(-1.5-\lambda) - 0.07] - 0.5[0.8(-1.5-\lambda) - 0.03] + 0.2[0.56 + 0.9 + 3\lambda]$$

Simplificando:
$$p(\lambda) = -\lambda^3 - 6.5\lambda^2 - 12.83\lambda - 8.646$$

Resolviendo numéricamente:
- $\lambda_1 \approx -0.89$
- $\lambda_2 \approx -2.31$  
- $\lambda_3 \approx -3.30$

**Conclusión**: Todos los valores propios tienen parte real negativa, por lo que el sistema es **estable**.

**Parte b: Análisis de Controlabilidad**

**Paso 2: Matriz de controlabilidad**

$$\mathcal{C} = [\mathbf{B} | \mathbf{A}\mathbf{B} | \mathbf{A}^2\mathbf{B}]$$

Calculando $\mathbf{A}\mathbf{B}$:
$$\mathbf{A}\mathbf{B} = \begin{pmatrix}
-2 & 0.5 & 0.2 \\
0.8 & -3 & 0.1 \\
0.3 & 0.7 & -1.5
\end{pmatrix}\begin{pmatrix}
1 & 0 \\
0 & 1 \\
0.5 & 0.3
\end{pmatrix} = \begin{pmatrix}
-1.9 & 0.56 \\
0.85 & -2.97 \\
0.05 & 0.25
\end{pmatrix}$$

Calculando $\mathbf{A}^2\mathbf{B}$:
$$\mathbf{A}^2 = \begin{pmatrix}
4.46 & -1.14 & -0.17 \\
-1.33 & 9.37 & 0.01 \\
-1.05 & -1.9 & 2.32
\end{pmatrix}$$

$$\mathbf{A}^2\mathbf{B} = \begin{pmatrix}
4.375 & -1.106 \\
-1.325 & 9.373 \\
-1.745 & -2.466
\end{pmatrix}$$

Matriz de controlabilidad:
$$\mathcal{C} = \begin{pmatrix}
1 & 0 & -1.9 & 0.56 & 4.375 & -1.106 \\
0 & 1 & 0.85 & -2.97 & -1.325 & 9.373 \\
0.5 & 0.3 & 0.05 & 0.25 & -1.745 & -2.466
\end{pmatrix}$$

**Paso 3: Verificar rango**

$$\text{rango}(\mathcal{C}) = 3$$

**Conclusión**: Como $\text{rango}(\mathcal{C}) = n = 3$, el sistema es **completamente controlable**.

**Parte c: Estado Estacionario Óptimo**

**Paso 4: Condición de estado estacionario**

En estado estacionario: $\frac{d\mathbf{c}}{dt} = \mathbf{0}$

$$\mathbf{A}\mathbf{c}_{ss} + \mathbf{B}\mathbf{u}_{ss} + \mathbf{f} = \mathbf{0}$$

$$\mathbf{c}_{ss} = -\mathbf{A}^{-1}(\mathbf{B}\mathbf{u}_{ss} + \mathbf{f})$$

**Paso 5: Calcular $\mathbf{A}^{-1}$**

Usando el método de la matriz adjunta:
$$\mathbf{A}^{-1} = \frac{1}{\det(\mathbf{A})}\text{adj}(\mathbf{A})$$

$$\det(\mathbf{A}) = -8.646$$

$$\mathbf{A}^{-1} = \begin{pmatrix}
-0.527 & 0.081 & 0.058 \\
0.089 & -0.364 & 0.025 \\
0.178 & 0.162 & -0.714
\end{pmatrix}$$

**Paso 6: Optimización**

Para maximizar la producción total (suma de concentraciones) sujeto a restricciones de control:

$$\max \mathbf{1}^T\mathbf{c}_{ss} = \max \mathbf{1}^T(-\mathbf{A}^{-1}\mathbf{B}\mathbf{u}_{ss})$$

sujeto a: $|\mathbf{u}_{ss}| \leq \mathbf{u}_{max}$

La solución óptima depende de las restricciones específicas y las perturbaciones $\mathbf{f}$.

### Verificación con MATLAB
```matlab
A = [-2 0.5 0.2; 0.8 -3 0.1; 0.3 0.7 -1.5];
B = [1 0; 0 1; 0.5 0.3];

% Estabilidad
eigenvalues = eig(A)

% Controlabilidad
C = ctrb(A, B);
rank(C)

% Estado estacionario
A_inv = inv(A);
```

---

## 🏆 Resumen de Competencias Desarrolladas

### Competencias Conceptuales Demostradas
- [x] Verificación rigurosa de propiedades de subespacios
- [x] Análisis de independencia lineal en contextos químicos
- [x] Cálculo de bases y dimensiones en sistemas complejos
- [x] Interpretación física de valores propios

### Competencias Procedimentales Aplicadas
- [x] Resolución sistemática de sistemas lineales
- [x] Cálculo eficiente de determinantes y rangos
- [x] Análisis de estabilidad mediante valores propios
- [x] Optimización con restricciones lineales

### Competencias Integradoras Alcanzadas
- [x] Modelado matemático de procesos químicos complejos
- [x] Análisis de controlabilidad de sistemas dinámicos
- [x] Síntesis de conocimientos para resolución de problemas reales
- [x] Uso efectivo de herramientas computacionales

---

*Estos ejercicios resueltos proporcionan una base sólida para la aplicación práctica del álgebra lineal en ingeniería química, integrando rigor matemático con relevancia industrial.*