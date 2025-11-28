# 📐 Espacios Vectoriales - Fundamentos Teóricos

## 🎯 Introducción y Motivación

Los espacios vectoriales constituyen el pilar fundamental del álgebra lineal moderna y representan una de las estructuras algebraicas más importantes en matemáticas aplicadas. En ingeniería química, estos conceptos son esenciales para:

- **Análisis de balances de materia** en sistemas de reactores complejos
- **Optimización de procesos industriales** mediante programación lineal
- **Modelado de sistemas dinámicos** en plantas químicas
- **Análisis de estabilidad** de puntos de operación
- **Diseño de controladores** para procesos químicos

La abstracción matemática de los espacios vectoriales permite unificar conceptos aparentemente dispares como sistemas de ecuaciones lineales, transformaciones geométricas, y análisis de datos experimentales bajo un marco teórico coherente.

## 📚 Definición Formal de Espacio Vectorial

**Definición 1.1** (Espacio Vectorial): Sea $\mathbb{K}$ un cuerpo (típicamente $\mathbb{R}$ o $\mathbb{C}$). Un **espacio vectorial** $V$ sobre $\mathbb{K}$ es un conjunto no vacío dotado de dos operaciones:

1. **Suma interna**: $+ : V \times V \rightarrow V$, que asigna a cada par $(\mathbf{u}, \mathbf{v})$ un elemento $\mathbf{u} + \mathbf{v} \in V$
2. **Producto por escalar**: $\cdot : \mathbb{K} \times V \rightarrow V$, que asigna a cada par $(\alpha, \mathbf{v})$ un elemento $\alpha \mathbf{v} \in V$

Estas operaciones deben satisfacer los ocho axiomas fundamentales que se detallan a continuación.

### 🔢 Axiomas Fundamentales del Espacio Vectorial

Para cualesquiera $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$ y $\alpha, \beta \in \mathbb{K}$, deben cumplirse los siguientes axiomas:

#### A. Axiomas de la Suma Vectorial

**A1. Conmutatividad**: 
$$\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$$

*Interpretación física*: El orden de adición de componentes en una mezcla no afecta la composición final.

**A2. Asociatividad**: 
$$(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$$

*Interpretación física*: La agrupación en la adición de corrientes de proceso no altera el balance total.

**A3. Existencia del elemento neutro**: 
$$\exists! \mathbf{0} \in V \text{ tal que } \mathbf{v} + \mathbf{0} = \mathbf{0} + \mathbf{v} = \mathbf{v}, \quad \forall \mathbf{v} \in V$$

*Interpretación física*: Existe un estado "nulo" (sin flujo, sin concentración) que no altera el sistema.

**A4. Existencia del elemento opuesto**: 
$$\forall \mathbf{v} \in V, \exists! (-\mathbf{v}) \in V \text{ tal que } \mathbf{v} + (-\mathbf{v}) = (-\mathbf{v}) + \mathbf{v} = \mathbf{0}$$

*Interpretación física*: Para cada corriente de entrada existe una corriente de salida que la cancela exactamente.

#### B. Axiomas del Producto por Escalar

**B1. Asociatividad mixta**: 
$$\alpha(\beta\mathbf{v}) = (\alpha\beta)\mathbf{v}$$

*Interpretación física*: Escalar un flujo y luego escalarlo nuevamente equivale a escalarlo por el producto de ambos factores.

**B2. Elemento unidad**: 
$$1 \cdot \mathbf{v} = \mathbf{v}$$

*Interpretación física*: Multiplicar por la unidad no cambia las propiedades del sistema.

**B3. Distributividad respecto a la suma de vectores**: 
$$\alpha(\mathbf{u} + \mathbf{v}) = \alpha\mathbf{u} + \alpha\mathbf{v}$$

*Interpretación física*: Escalar una mezcla equivale a escalar cada componente por separado.

**B4. Distributividad respecto a la suma de escalares**: 
$$(\alpha + \beta)\mathbf{v} = \alpha\mathbf{v} + \beta\mathbf{v}$$

*Interpretación física*: La suma de factores de escala aplicados a un sistema equivale a aplicar cada factor por separado.

### 🧮 Propiedades Derivadas de los Axiomas

**Teorema 1.1** (Propiedades básicas): En todo espacio vectorial $V$ se cumplen:

1. **Unicidad del elemento neutro**: El vector cero $\mathbf{0}$ es único.

2. **Unicidad del opuesto**: Para cada $\mathbf{v} \in V$, el vector $-\mathbf{v}$ es único.

3. **Producto por cero**: $0 \cdot \mathbf{v} = \mathbf{0}$ para todo $\mathbf{v} \in V$.

4. **Producto de escalar por vector cero**: $\alpha \cdot \mathbf{0} = \mathbf{0}$ para todo $\alpha \in \mathbb{K}$.

5. **Producto por menos uno**: $(-1) \cdot \mathbf{v} = -\mathbf{v}$ para todo $\mathbf{v} \in V$.

6. **Ley de cancelación**: Si $\alpha \mathbf{v} = \mathbf{0}$ entonces $\alpha = 0$ o $\mathbf{v} = \mathbf{0}$.

**Demostración de la Propiedad 3**:
Sea $\mathbf{v} \in V$ arbitrario. Entonces:
$$0 \cdot \mathbf{v} = (0 + 0) \cdot \mathbf{v} = 0 \cdot \mathbf{v} + 0 \cdot \mathbf{v}$$

Sumando $-(0 \cdot \mathbf{v})$ a ambos lados:
$$0 \cdot \mathbf{v} + (-(0 \cdot \mathbf{v})) = (0 \cdot \mathbf{v} + 0 \cdot \mathbf{v}) + (-(0 \cdot \mathbf{v}))$$
$$\mathbf{0} = 0 \cdot \mathbf{v} + (0 \cdot \mathbf{v} + (-(0 \cdot \mathbf{v})))$$
$$\mathbf{0} = 0 \cdot \mathbf{v} + \mathbf{0} = 0 \cdot \mathbf{v}$$

Por tanto, $0 \cdot \mathbf{v} = \mathbf{0}$. $\square$

## 🌟 Ejemplos Fundamentales de Espacios Vectoriales

### Ejemplo 1: El Espacio Euclidiano $\mathbb{R}^n$

**Definición**: El espacio $\mathbb{R}^n$ es el conjunto de todas las $n$-tuplas de números reales:
$$\mathbb{R}^n = \{(x_1, x_2, \ldots, x_n) : x_i \in \mathbb{R} \text{ para } i = 1, 2, \ldots, n\}$$

**Operaciones**:
- **Suma**: $\mathbf{x} + \mathbf{y} = (x_1, x_2, \ldots, x_n) + (y_1, y_2, \ldots, y_n) = (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n)$
- **Producto por escalar**: $\alpha \mathbf{x} = \alpha(x_1, x_2, \ldots, x_n) = (\alpha x_1, \alpha x_2, \ldots, \alpha x_n)$

**Verificación de axiomas** (ejemplo con A1):
$$\mathbf{x} + \mathbf{y} = (x_1 + y_1, \ldots, x_n + y_n) = (y_1 + x_1, \ldots, y_n + x_n) = \mathbf{y} + \mathbf{x}$$

**Aplicaciones en Ingeniería Química**:
- **Vector de concentraciones**: $\mathbf{c} = (c_A, c_B, c_C, c_D) \in \mathbb{R}^4$ representa las concentraciones molares de cuatro especies químicas
- **Vector de flujos**: $\mathbf{F} = (F_1, F_2, F_3) \in \mathbb{R}^3$ representa flujos másicos en tres corrientes
- **Vector de temperaturas**: $\mathbf{T} = (T_1, T_2, \ldots, T_n) \in \mathbb{R}^n$ representa el perfil de temperaturas en $n$ puntos de un reactor

**Ejemplo numérico**: En un reactor con especies A, B, C, si tenemos:
- Estado inicial: $\mathbf{c}_0 = (2.5, 1.8, 0.0)$ mol/L
- Cambio por reacción: $\Delta\mathbf{c} = (-0.5, -0.3, 0.8)$ mol/L
- Estado final: $\mathbf{c}_f = \mathbf{c}_0 + \Delta\mathbf{c} = (2.0, 1.5, 0.8)$ mol/L

### Ejemplo 2: Espacio de Matrices $M_{m \times n}(\mathbb{R})$

**Definición**: El conjunto de todas las matrices reales de tamaño $m \times n$:
$$M_{m \times n}(\mathbb{R}) = \left\{A = (a_{ij}) : a_{ij} \in \mathbb{R}, \, 1 \leq i \leq m, \, 1 \leq j \leq n\right\}$$

**Operaciones**:
- **Suma**: $(A + B)_{ij} = a_{ij} + b_{ij}$
- **Producto por escalar**: $(\alpha A)_{ij} = \alpha a_{ij}$

**Elemento neutro**: La matriz cero $\mathbf{0}_{m \times n}$ con todas las entradas nulas.

**Aplicaciones en Ingeniería Química**:

1. **Matriz estequiométrica**: Para un sistema con $m$ especies y $n$ reacciones:
   $$\mathbf{S} = \begin{pmatrix}
   \nu_{11} & \nu_{12} & \cdots & \nu_{1n} \\
   \nu_{21} & \nu_{22} & \cdots & \nu_{2n} \\
   \vdots & \vdots & \ddots & \vdots \\
   \nu_{m1} & \nu_{m2} & \cdots & \nu_{mn}
   \end{pmatrix}$$
   donde $\nu_{ij}$ es el coeficiente estequiométrico de la especie $i$ en la reacción $j$.

2. **Matriz de transferencia de masa**: En un sistema de $n$ etapas:
   $$\mathbf{K} = \begin{pmatrix}
   k_{11} & k_{12} & \cdots & k_{1n} \\
   k_{21} & k_{22} & \cdots & k_{2n} \\
   \vdots & \vdots & \ddots & \vdots \\
   k_{n1} & k_{n2} & \cdots & k_{nn}
   \end{pmatrix}$$

**Ejemplo concreto**: Sistema de reacciones A + B → C, 2A → D:
$$\mathbf{S} = \begin{pmatrix}
-1 & -2 \\
-1 & 0 \\
1 & 0 \\
0 & 1
\end{pmatrix} \in M_{4 \times 2}(\mathbb{R})$$

### Ejemplo 3: Espacio de Funciones Continuas $C[a,b]$

**Definición**: El conjunto de todas las funciones continuas en el intervalo cerrado $[a,b]$:
$$C[a,b] = \{f : [a,b] \rightarrow \mathbb{R} : f \text{ es continua en } [a,b]\}$$

**Operaciones**:
- **Suma**: $(f + g)(x) = f(x) + g(x)$ para todo $x \in [a,b]$
- **Producto por escalar**: $(\alpha f)(x) = \alpha f(x)$ para todo $x \in [a,b]$

**Elemento neutro**: La función cero $\mathbf{0}(x) = 0$ para todo $x \in [a,b]$.

**Verificación de axiomas** (ejemplo con B3):
$$[\alpha(f + g)](x) = \alpha[(f + g)(x)] = \alpha[f(x) + g(x)] = \alpha f(x) + \alpha g(x) = (\alpha f)(x) + (\alpha g)(x)$$

**Aplicaciones en Ingeniería Química**:

1. **Perfiles de concentración**: $c_A(z) \in C[0,L]$ representa la concentración del componente A a lo largo de un reactor tubular de longitud $L$.

2. **Perfiles de temperatura**: $T(r) \in C[0,R]$ representa la distribución radial de temperatura en un reactor cilíndrico de radio $R$.

3. **Cinética de reacción**: $r(t) \in C[0,t_f]$ representa la velocidad de reacción como función del tiempo.

**Ejemplo numérico**: En un reactor tubular isotérmico con reacción de primer orden:
$$c_A(z) = c_{A0} e^{-kz/v}$$
donde $c_{A0}$ es la concentración inicial, $k$ la constante cinética, y $v$ la velocidad superficial.

### Ejemplo 4: Espacio de Polinomios $\mathbb{P}_n$

**Definición**: El conjunto de todos los polinomios de grado menor o igual a $n$:
$$\mathbb{P}_n = \{p(x) = a_0 + a_1 x + a_2 x^2 + \cdots + a_n x^n : a_i \in \mathbb{R}\}$$

**Dimensión**: $\dim(\mathbb{P}_n) = n + 1$

**Base canónica**: $\{1, x, x^2, \ldots, x^n\}$

**Aplicaciones en Ingeniería Química**:
- **Ajuste de datos experimentales**: Correlaciones polinómicas para propiedades físicas
- **Aproximación de funciones**: Modelos simplificados de cinética compleja
- **Interpolación**: Estimación de valores intermedios en tablas de propiedades

### Ejemplo 5: Espacio de Secuencias $\ell^2$

**Definición**: El espacio de secuencias de cuadrado sumable:
$$\ell^2 = \left\{(x_1, x_2, x_3, \ldots) : x_i \in \mathbb{R}, \sum_{i=1}^{\infty} x_i^2 < \infty\right\}$$

**Aplicaciones en Ingeniería Química**:
- **Series de Fourier**: Análisis de señales periódicas en control de procesos
- **Análisis espectral**: Descomposición de señales de proceso
- **Filtrado digital**: Procesamiento de datos experimentales

## 🔍 Subespacios Vectoriales

### Definición y Caracterización

**Definición 1.2** (Subespacio vectorial): Sea $V$ un espacio vectorial sobre $\mathbb{K}$. Un subconjunto no vacío $W \subseteq V$ es un **subespacio vectorial** de $V$ si y solo si $W$ es cerrado bajo las operaciones de $V$, es decir:

1. **Cerradura bajo la suma**: $\mathbf{u}, \mathbf{v} \in W \Rightarrow \mathbf{u} + \mathbf{v} \in W$
2. **Cerradura bajo el producto por escalar**: $\mathbf{v} \in W, \alpha \in \mathbb{K} \Rightarrow \alpha\mathbf{v} \in W$

**Teorema 1.2** (Caracterización de subespacios): Un subconjunto no vacío $W \subseteq V$ es un subespacio vectorial si y solo si:
$$\alpha\mathbf{u} + \beta\mathbf{v} \in W \quad \text{para cualesquiera } \mathbf{u}, \mathbf{v} \in W \text{ y } \alpha, \beta \in \mathbb{K}$$

**Demostración**: 
($\Rightarrow$) Si $W$ es subespacio, entonces por definición es cerrado bajo suma y producto por escalar, luego $\alpha\mathbf{u} \in W$ y $\beta\mathbf{v} \in W$, y por cerradura bajo suma, $\alpha\mathbf{u} + \beta\mathbf{v} \in W$.

($\Leftarrow$) Si se cumple la condición, tomando $\alpha = \beta = 1$ obtenemos cerradura bajo suma, y tomando $\beta = 0$ obtenemos cerradura bajo producto por escalar. $\square$

### Propiedades Fundamentales de Subespacios

**Teorema 1.3**: Si $W$ es un subespacio de $V$, entonces:
1. $\mathbf{0} \in W$ (el vector cero pertenece a todo subespacio)
2. Si $\mathbf{v} \in W$, entonces $-\mathbf{v} \in W$
3. $W$ es un espacio vectorial con las operaciones heredadas de $V$

**Demostración de (1)**: Sea $\mathbf{w} \in W$ (existe pues $W \neq \emptyset$). Por cerradura bajo producto por escalar, $0 \cdot \mathbf{w} \in W$. Por la propiedad derivada de los axiomas, $0 \cdot \mathbf{w} = \mathbf{0}$, luego $\mathbf{0} \in W$. $\square$

### Ejemplos Importantes de Subespacios

**Ejemplo 1**: **Núcleo de una matriz** (Aplicación en balances de materia)
En un sistema de $n$ componentes con $m$ reacciones, el espacio de vectores de velocidades de reacción que conservan la masa forma un subespacio de $\mathbb{R}^m$:

Si $\mathbf{S}$ es la matriz estequiométrica, entonces:
$$\text{Ker}(\mathbf{S}) = \{\mathbf{r} \in \mathbb{R}^m : \mathbf{S}\mathbf{r} = \mathbf{0}\}$$

**Verificación**: 
- Si $\mathbf{r}_1, \mathbf{r}_2 \in \text{Ker}(\mathbf{S})$, entonces $\mathbf{S}(\mathbf{r}_1 + \mathbf{r}_2) = \mathbf{S}\mathbf{r}_1 + \mathbf{S}\mathbf{r}_2 = \mathbf{0} + \mathbf{0} = \mathbf{0}$
- Si $\mathbf{r} \in \text{Ker}(\mathbf{S})$ y $\alpha \in \mathbb{R}$, entonces $\mathbf{S}(\alpha\mathbf{r}) = \alpha(\mathbf{S}\mathbf{r}) = \alpha \mathbf{0} = \mathbf{0}$

**Ejemplo 2**: **Hiperplanos** (Restricciones de proceso)
El conjunto $H = \{\mathbf{x} \in \mathbb{R}^n : \mathbf{a}^T\mathbf{x} = 0\}$ donde $\mathbf{a} \neq \mathbf{0}$ es un subespacio de dimensión $n-1$.

**Aplicación**: Restricciones de balance de materia global en procesos de separación.

**Ejemplo 3**: **Espacio de matrices simétricas**
$$\text{Sym}_n = \{A \in M_{n \times n}(\mathbb{R}) : A^T = A\}$$

**Aplicación**: Matrices de correlación en análisis de datos experimentales.

## 🎯 Combinaciones Lineales y Espacio Generado

### Definición de Combinación Lineal

**Definición 1.4** (Combinación lineal): Sean $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k \in V$ y $\alpha_1, \alpha_2, \ldots, \alpha_k \in \mathbb{K}$. Una **combinación lineal** de estos vectores es:
$$\mathbf{v} = \alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_k\mathbf{v}_k = \sum_{i=1}^k \alpha_i\mathbf{v}_i$$

Los escalares $\alpha_i$ se denominan **coeficientes** de la combinación lineal.

### Espacio Generado (Span)

**Definición 1.5** (Espacio generado): El **espacio generado** o **span** de un conjunto de vectores $S = \{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\}$ es:
$$\text{span}(S) = \text{span}\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\} = \left\{\sum_{i=1}^k \alpha_i\mathbf{v}_i : \alpha_i \in \mathbb{K}\right\}$$

**Teorema 1.4**: $\text{span}(S)$ es el subespacio más pequeño de $V$ que contiene a todos los vectores de $S$.

**Demostración**: 
1. $\text{span}(S)$ es un subespacio (verificar cerradura bajo operaciones)
2. $S \subseteq \text{span}(S)$ (cada $\mathbf{v}_i = 0\mathbf{v}_1 + \cdots + 1\mathbf{v}_i + \cdots + 0\mathbf{v}_k$)
3. Si $W$ es cualquier subespacio que contiene $S$, entonces $\text{span}(S) \subseteq W$ $\square$

### Propiedades del Espacio Generado

**Teorema 1.5**: Sean $S, T \subseteq V$. Entonces:
1. $\text{span}(\emptyset) = \{\mathbf{0}\}$
2. $\text{span}(S \cup T) = \text{span}(\text{span}(S) \cup \text{span}(T))$
3. Si $S \subseteq T$, entonces $\text{span}(S) \subseteq \text{span}(T)$
4. $\text{span}(\text{span}(S)) = \text{span}(S)$

### Aplicaciones en Ingeniería Química

**Ejemplo 1**: **Espacio de composiciones alcanzables**
En un reactor con $n$ componentes y $m$ reacciones independientes, el conjunto de todas las composiciones alcanzables desde una composición inicial $\mathbf{c}_0$ es:
$$\mathcal{C} = \{\mathbf{c}_0 + \mathbf{S}\boldsymbol{\xi} : \boldsymbol{\xi} \in \mathbb{R}^m\} = \mathbf{c}_0 + \text{span}\{\mathbf{s}_1, \mathbf{s}_2, \ldots, \mathbf{s}_m\}$$
donde $\mathbf{s}_j$ son las columnas de la matriz estequiométrica $\mathbf{S}$.

**Ejemplo 2**: **Espacio de estados de un proceso**
En un sistema dinámico lineal $\dot{\mathbf{x}} = \mathbf{A}\mathbf{x} + \mathbf{B}\mathbf{u}$, el espacio de estados alcanzables desde el origen es:
$$\mathcal{R} = \text{span}\{\mathbf{B}, \mathbf{A}\mathbf{B}, \mathbf{A}^2\mathbf{B}, \ldots, \mathbf{A}^{n-1}\mathbf{B}\}$$

## 🔗 Dependencia e Independencia Lineal

### Definiciones Fundamentales

**Definición 1.6** (Dependencia lineal): Un conjunto de vectores $\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\}$ es **linealmente dependiente** si existen escalares $\alpha_1, \alpha_2, \ldots, \alpha_k \in \mathbb{K}$, no todos nulos, tales que:
$$\alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_k\mathbf{v}_k = \mathbf{0}$$

**Definición 1.7** (Independencia lineal): Un conjunto de vectores $\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\}$ es **linealmente independiente** si la única solución de la ecuación:
$$\alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_k\mathbf{v}_k = \mathbf{0}$$
es $\alpha_1 = \alpha_2 = \cdots = \alpha_k = 0$.

### Interpretación Geométrica y Física

**Interpretación geométrica**:
- En $\mathbb{R}^2$: Dos vectores son linealmente dependientes si y solo si son colineales (uno es múltiplo escalar del otro)
- En $\mathbb{R}^3$: Tres vectores son linealmente dependientes si y solo si son coplanares

**Interpretación en ingeniería química**:
- **Reacciones dependientes**: Si una reacción puede expresarse como combinación lineal de otras, es redundante
- **Variables de proceso**: Variables independientes determinan completamente el estado del sistema

### Teoremas Fundamentales

**Teorema 1.6** (Caracterización de dependencia): Los vectores $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k$ son linealmente dependientes si y solo si al menos uno de ellos puede expresarse como combinación lineal de los demás.

**Demostración**: 
($\Rightarrow$) Si son dependientes, existe una relación no trivial $\sum_{i=1}^k \alpha_i\mathbf{v}_i = \mathbf{0}$ con algún $\alpha_j \neq 0$. Entonces:
$$\mathbf{v}_j = -\frac{1}{\alpha_j}\sum_{i \neq j} \alpha_i\mathbf{v}_i$$

($\Leftarrow$) Si $\mathbf{v}_j = \sum_{i \neq j} \beta_i\mathbf{v}_i$, entonces $\sum_{i \neq j} \beta_i\mathbf{v}_i - \mathbf{v}_j = \mathbf{0}$ es una relación no trivial. $\square$

**Teorema 1.7** (Propiedades de independencia):
1. El conjunto $\{\mathbf{0}\}$ es linealmente dependiente
2. Cualquier conjunto que contenga el vector cero es linealmente dependiente
3. Si $\{\mathbf{v}_1, \ldots, \mathbf{v}_k\}$ es linealmente independiente, entonces cualquier subconjunto también lo es
4. Si $\{\mathbf{v}_1, \ldots, \mathbf{v}_k\}$ es linealmente dependiente, entonces cualquier conjunto que lo contenga también lo es

### Métodos para Determinar Independencia Lineal

#### Método 1: Resolución Directa del Sistema Homogéneo

Para determinar si $\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\}$ son linealmente independientes:

1. Plantear la ecuación $\alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_k\mathbf{v}_k = \mathbf{0}$
2. Escribir el sistema de ecuaciones lineales resultante
3. Resolver el sistema homogéneo
4. Si la única solución es trivial ($\alpha_i = 0$ para todo $i$), son independientes

#### Método 2: Análisis Matricial

Si los vectores están en $\mathbb{R}^n$, formar la matriz $\mathbf{A} = [\mathbf{v}_1 | \mathbf{v}_2 | \cdots | \mathbf{v}_k]$ y:
- Los vectores son linealmente independientes $\Leftrightarrow$ $\text{rango}(\mathbf{A}) = k$
- Los vectores son linealmente dependientes $\Leftrightarrow$ $\text{rango}(\mathbf{A}) < k$

### Ejemplo Detallado en Ingeniería Química

**Problema**: Análisis de independencia de reacciones químicas

Considere un reactor con 4 componentes (A, B, C, D) y las siguientes reacciones:
1. $A + B \rightarrow C$ 
2. $2A + B \rightarrow 2C$
3. $A \rightarrow D$
4. $B + C \rightarrow A + D$

**Paso 1**: Escribir los vectores estequiométricos (orden: A, B, C, D)
- $\mathbf{r}_1 = (-1, -1, 1, 0)$
- $\mathbf{r}_2 = (-2, -1, 2, 0)$
- $\mathbf{r}_3 = (-1, 0, 0, 1)$
- $\mathbf{r}_4 = (1, -1, -1, 1)$

**Paso 2**: Plantear la ecuación de dependencia lineal
$$\alpha_1\mathbf{r}_1 + \alpha_2\mathbf{r}_2 + \alpha_3\mathbf{r}_3 + \alpha_4\mathbf{r}_4 = \mathbf{0}$$

**Paso 3**: Escribir el sistema matricial
$$\begin{pmatrix}
-1 & -2 & -1 & 1 \\
-1 & -1 & 0 & -1 \\
1 & 2 & 0 & -1 \\
0 & 0 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
\alpha_1 \\ \alpha_2 \\ \alpha_3 \\ \alpha_4
\end{pmatrix} = 
\begin{pmatrix}
0 \\ 0 \\ 0 \\ 0
\end{pmatrix}$$

**Paso 4**: Resolver por eliminación gaussiana
$$\begin{pmatrix}
-1 & -2 & -1 & 1 \\
-1 & -1 & 0 & -1 \\
1 & 2 & 0 & -1 \\
0 & 0 & 1 & 1
\end{pmatrix} \sim 
\begin{pmatrix}
1 & 2 & 1 & -1 \\
0 & 1 & 1 & -2 \\
0 & 0 & -1 & 0 \\
0 & 0 & 1 & 1
\end{pmatrix} \sim 
\begin{pmatrix}
1 & 0 & -1 & 3 \\
0 & 1 & 1 & -2 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}$$

**Resultado**: $\text{rango} = 4$, por tanto las 4 reacciones son **linealmente independientes**.

**Interpretación química**: Las cuatro reacciones son fundamentalmente diferentes y ninguna puede expresarse como combinación de las otras. Todas son necesarias para describir completamente el sistema de reacciones.

## 📏 Base y Dimensión - Conceptos Fundamentales

### Definición de Base

**Definición 1.8** (Base): Un conjunto $\mathcal{B} = \{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n\}$ es una **base** del espacio vectorial $V$ si y solo si:
1. **Independencia lineal**: Los vectores $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n$ son linealmente independientes
2. **Generación**: $\text{span}(\mathcal{B}) = V$ (los vectores generan todo el espacio)

**Interpretación**: Una base es un conjunto "mínimo" de vectores que genera todo el espacio, sin redundancia.

### Teoremas Fundamentales sobre Bases

**Teorema 1.8** (Existencia de bases): Todo espacio vectorial de dimensión finita tiene al menos una base.

**Teorema 1.9** (Unicidad del cardinal): Si $V$ es un espacio vectorial de dimensión finita, entonces todas las bases de $V$ tienen el mismo número de elementos.

**Demostración** (Esquema): Usar el lema de intercambio de Steinitz: si $\{\mathbf{u}_1, \ldots, \mathbf{u}_m\}$ es linealmente independiente y $\{\mathbf{v}_1, \ldots, \mathbf{v}_n\}$ genera $V$, entonces $m \leq n$. $\square$

**Teorema 1.10** (Caracterización de bases): Sea $V$ un espacio vectorial de dimensión $n$. Para un conjunto $\mathcal{S} = \{\mathbf{v}_1, \ldots, \mathbf{v}_n\}$ de $n$ vectores, las siguientes afirmaciones son equivalentes:
1. $\mathcal{S}$ es una base de $V$
2. $\mathcal{S}$ es linealmente independiente
3. $\mathcal{S}$ genera $V$

### Definición de Dimensión

**Definición 1.9** (Dimensión): La **dimensión** de un espacio vectorial $V$, denotada $\dim(V)$, es el número de vectores en cualquier base de $V$.

**Convenciones**:
- $\dim(\{\mathbf{0}\}) = 0$ (el espacio trivial tiene dimensión cero)
- Si $V$ no tiene una base finita, se dice que $V$ tiene dimensión infinita

### Propiedades de la Dimensión

**Teorema 1.11** (Propiedades básicas):
1. $\dim(V) = 0 \Leftrightarrow V = \{\mathbf{0}\}$
2. Si $W$ es un subespacio de $V$, entonces $\dim(W) \leq \dim(V)$
3. Si $W$ es un subespacio de $V$ y $\dim(W) = \dim(V) < \infty$, entonces $W = V$
4. $\dim(\mathbb{R}^n) = n$
5. $\dim(M_{m \times n}(\mathbb{R})) = mn$
6. $\dim(\mathbb{P}_n) = n + 1$

### Bases Canónicas y Ejemplos

#### Base Canónica de $\mathbb{R}^n$
$$\mathcal{E}_n = \{\mathbf{e}_1, \mathbf{e}_2, \ldots, \mathbf{e}_n\}$$
donde $\mathbf{e}_i = (0, \ldots, 0, 1, 0, \ldots, 0)$ (1 en la posición $i$-ésima).

**Verificación**:
- **Independencia**: $\alpha_1\mathbf{e}_1 + \cdots + \alpha_n\mathbf{e}_n = (\alpha_1, \ldots, \alpha_n) = \mathbf{0} \Rightarrow \alpha_i = 0$ para todo $i$
- **Generación**: Todo vector $(x_1, \ldots, x_n) = x_1\mathbf{e}_1 + \cdots + x_n\mathbf{e}_n$

#### Base Canónica de $M_{2 \times 2}(\mathbb{R})$
$$\mathcal{B} = \left\{\begin{pmatrix}1&0\\0&0\end{pmatrix}, \begin{pmatrix}0&1\\0&0\end{pmatrix}, \begin{pmatrix}0&0\\1&0\end{pmatrix}, \begin{pmatrix}0&0\\0&1\end{pmatrix}\right\}$$

#### Base Canónica de $\mathbb{P}_3$
$$\mathcal{B} = \{1, x, x^2, x^3\}$$

### Coordenadas Respecto a una Base

**Definición 1.10** (Coordenadas): Sea $\mathcal{B} = \{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n\}$ una base de $V$. Para cualquier vector $\mathbf{v} \in V$, existen únicos escalares $\alpha_1, \alpha_2, \ldots, \alpha_n$ tales que:
$$\mathbf{v} = \alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_n\mathbf{v}_n$$

El vector $[\mathbf{v}]_\mathcal{B} = (\alpha_1, \alpha_2, \ldots, \alpha_n)^T$ se llama **vector de coordenadas** de $\mathbf{v}$ respecto a la base $\mathcal{B}$.

**Teorema 1.12** (Isomorfismo de coordenadas): La función $T: V \rightarrow \mathbb{K}^n$ definida por $T(\mathbf{v}) = [\mathbf{v}]_\mathcal{B}$ es un isomorfismo de espacios vectoriales.

### Proceso de Construcción de Bases

#### Método 1: Extensión de Conjuntos Linealmente Independientes

**Teorema 1.13** (Extensión a base): Sea $V$ un espacio vectorial de dimensión finita $n$ y sea $\mathcal{S} = \{\mathbf{v}_1, \ldots, \mathbf{v}_k\}$ un conjunto linealmente independiente con $k < n$. Entonces $\mathcal{S}$ puede extenderse a una base de $V$.

**Algoritmo**:
1. Comenzar con el conjunto independiente $\mathcal{S}$
2. Si $\text{span}(\mathcal{S}) = V$, entonces $\mathcal{S}$ es una base
3. Si no, existe $\mathbf{w} \in V \setminus \text{span}(\mathcal{S})$
4. El conjunto $\mathcal{S} \cup \{\mathbf{w}\}$ es linealmente independiente
5. Repetir hasta obtener una base

#### Método 2: Reducción de Conjuntos Generadores

**Teorema 1.14** (Reducción a base): Sea $V$ un espacio vectorial de dimensión finita y sea $\mathcal{G} = \{\mathbf{w}_1, \ldots, \mathbf{w}_m\}$ un conjunto generador de $V$. Entonces existe un subconjunto de $\mathcal{G}$ que es una base de $V$.

**Algoritmo**:
1. Comenzar con el conjunto generador $\mathcal{G}$
2. Eliminar vectores que sean combinación lineal de los anteriores
3. El conjunto resultante es una base

### Aplicaciones en Ingeniería Química

#### Ejemplo 1: Espacio de Composiciones Válidas

En un sistema con $n$ componentes sujeto a $m$ restricciones lineales independientes (balances de elementos), el espacio de composiciones válidas tiene dimensión $n - m$.

**Caso específico**: Sistema C-H-O con 5 especies (CH₄, H₂O, CO, CO₂, H₂)
- Restricciones: Balance de C, balance de H, balance de O
- Dimensión del espacio de composiciones: $5 - 3 = 2$
- Base posible: $\{(1,0,-1,0,0), (0,1,0,0,-1)\}$ (representando reacciones independientes)

#### Ejemplo 2: Grados de Libertad en Procesos

**Regla de Gibbs generalizada**: En un proceso con $n$ variables, $m$ ecuaciones independientes y $p$ especificaciones, los grados de libertad son:
$$\text{GL} = n - m - p = \dim(\text{Espacio de soluciones})$$

#### Ejemplo 3: Análisis de Controlabilidad

En un sistema dinámico $\dot{\mathbf{x}} = \mathbf{A}\mathbf{x} + \mathbf{B}\mathbf{u}$, el sistema es completamente controlable si y solo si:
$$\dim(\text{span}\{\mathbf{B}, \mathbf{A}\mathbf{B}, \mathbf{A}^2\mathbf{B}, \ldots, \mathbf{A}^{n-1}\mathbf{B}\}) = n$$

### Cambio de Base

**Definición 1.11** (Matriz de cambio de base): Sean $\mathcal{B} = \{\mathbf{v}_1, \ldots, \mathbf{v}_n\}$ y $\mathcal{C} = \{\mathbf{w}_1, \ldots, \mathbf{w}_n\}$ dos bases de $V$. La **matriz de cambio de base** de $\mathcal{B}$ a $\mathcal{C}$ es:
$$\mathbf{P}_{\mathcal{B} \rightarrow \mathcal{C}} = [[\mathbf{v}_1]_\mathcal{C} | [\mathbf{v}_2]_\mathcal{C} | \cdots | [\mathbf{v}_n]_\mathcal{C}]$$

**Propiedad fundamental**: Si $[\mathbf{v}]_\mathcal{B}$ son las coordenadas de $\mathbf{v}$ en la base $\mathcal{B}$, entonces:
$$[\mathbf{v}]_\mathcal{C} = \mathbf{P}_{\mathcal{B} \rightarrow \mathcal{C}} [\mathbf{v}]_\mathcal{B}$$

### Dimensión de Subespacios Importantes

**Teorema 1.15** (Fórmula de la dimensión): Para una transformación lineal $T: V \rightarrow W$:
$$\dim(V) = \dim(\text{Ker}(T)) + \dim(\text{Im}(T))$$

**Aplicaciones**:
- **Núcleo de matriz estequiométrica**: $\dim(\text{Ker}(\mathbf{S})) = m - \text{rango}(\mathbf{S})$ (número de reacciones independientes)
- **Espacio de soluciones**: Para $\mathbf{A}\mathbf{x} = \mathbf{b}$, si es consistente, $\dim(\text{Sol}) = n - \text{rango}(\mathbf{A})$

## 🔬 Aplicaciones Avanzadas en Ingeniería Química

### Análisis de Grados de Libertad

En un proceso químico, el análisis de grados de libertad se basa fundamentalmente en conceptos de álgebra lineal:

**Regla general**: Para un sistema con:
- $n$ variables de proceso
- $m$ ecuaciones independientes (balances, restricciones)
- $p$ especificaciones externas

El número de **grados de libertad** es:
$$\text{GL} = n - m - p = \dim(\text{Espacio de soluciones})$$

**Ejemplo detallado**: Reactor CSTR con reacción $A \rightarrow B$
- Variables: $F_A^{in}, F_B^{in}, F_A^{out}, F_B^{out}, V, k, C_A, C_B$ (8 variables)
- Ecuaciones: Balance de A, balance de B, cinética, definición de concentración (4 ecuaciones)
- Especificaciones típicas: $F_A^{in}, F_B^{in}, V, k$ (4 especificaciones)
- Grados de libertad: $8 - 4 - 4 = 0$ (sistema completamente especificado)

### Análisis de Redes de Reacciones

**Teorema**: En una red de reacciones con matriz estequiométrica $\mathbf{S}$, el número de reacciones independientes es:
$$r = \text{rango}(\mathbf{S}) = \dim(\text{Im}(\mathbf{S}))$$

Y el número de invariantes de conservación es:
$$c = n - r = \dim(\text{Ker}(\mathbf{S}^T))$$

donde $n$ es el número de especies.

### Espacios de Estados Alcanzables

En sistemas dinámicos de procesos químicos, el conjunto de estados alcanzables desde un estado inicial $\mathbf{x}_0$ forma un subespacio afín:
$$\mathcal{R}(\mathbf{x}_0) = \mathbf{x}_0 + \text{span}\{\text{columnas de } \mathbf{S}\}$$

## 📊 Resumen Conceptual Integrado

### Jerarquía de Conceptos

```
Espacio Vectorial V
├── Subespacios W ⊆ V
│   ├── Núcleo: Ker(T) = {v : T(v) = 0}
│   ├── Imagen: Im(T) = {T(v) : v ∈ V}
│   └── Hiperplanos: {v : a·v = 0}
├── Combinaciones Lineales
│   └── Espacio Generado: span{v₁, ..., vₖ}
├── Independencia Lineal
│   ├── Conjuntos LI: α₁v₁ + ... + αₖvₖ = 0 ⟹ αᵢ = 0
│   └── Conjuntos LD: ∃αᵢ ≠ 0 tal que Σαᵢvᵢ = 0
└── Base y Dimensión
    ├── Base: Conjunto LI que genera V
    ├── Dimensión: |Base| = dim(V)
    └── Coordenadas: [v]ᵦ ∈ Kⁿ
```

### Tabla de Correspondencias Ingeniería-Matemáticas

| Concepto Matemático | Interpretación en Ingeniería Química |
|---------------------|--------------------------------------|
| **Espacio vectorial** | Espacio de estados del proceso |
| **Vector** | Estado del sistema (concentraciones, temperaturas, presiones) |
| **Subespacio** | Conjunto de estados válidos (restricciones físicas) |
| **Combinación lineal** | Superposición de efectos/estados |
| **Independencia lineal** | Variables/reacciones no redundantes |
| **Base** | Conjunto mínimo de variables independientes |
| **Dimensión** | Número de grados de libertad |
| **Coordenadas** | Valores específicos de variables de proceso |
| **Núcleo** | Estados de equilibrio, invariantes |
| **Imagen** | Estados alcanzables |

### Propiedades Fundamentales Unificadas

**Teorema Central**: Para cualquier transformación lineal $T: V \rightarrow W$:
$$\dim(V) = \dim(\text{Ker}(T)) + \dim(\text{Im}(T))$$

**Aplicaciones directas**:
1. **Sistemas de ecuaciones**: $\mathbf{A}\mathbf{x} = \mathbf{b}$
   - $\dim(\text{Sol}) = n - \text{rango}(\mathbf{A})$ si es consistente
2. **Redes de reacciones**: Matriz estequiométrica $\mathbf{S}$
   - Reacciones independientes: $\text{rango}(\mathbf{S})$
   - Invariantes de conservación: $n - \text{rango}(\mathbf{S})$
3. **Control de procesos**: Matriz de controlabilidad
   - Estados controlables: $\text{rango}([\mathbf{B}|\mathbf{A}\mathbf{B}|\cdots|\mathbf{A}^{n-1}\mathbf{B}])$

## 🎯 Ejercicios de Síntesis

### Ejercicio Integrador 1: Análisis Completo de Red de Reacciones

Considere el sistema de reacciones:
1. $A + B \rightarrow C + D$
2. $C + D \rightarrow E$
3. $2A \rightarrow F$
4. $B + E \rightarrow A + F$

**Tareas**:
a) Construir la matriz estequiométrica $\mathbf{S}$
b) Determinar el rango y la dimensión del núcleo
c) Encontrar una base para el espacio de reacciones independientes
d) Identificar los invariantes de conservación
e) Calcular los grados de libertad del sistema

### Ejercicio Integrador 2: Espacio de Estados de Proceso

Un proceso de separación tiene 4 corrientes con 3 componentes cada una. Las fracciones molares deben sumar 1 en cada corriente, y hay 2 balances globales independientes.

**Tareas**:
a) Determinar la dimensión del espacio de estados válidos
b) Construir una base para este espacio
c) Expresar un estado específico en coordenadas de esta base
d) Analizar la controlabilidad del sistema

### Ejercicio Integrador 3: Optimización con Restricciones

En un reactor con 5 especies y 3 reacciones independientes, se desea maximizar la producción de una especie específica sujeto a restricciones de balance de materia.

**Tareas**:
a) Formular el problema como optimización en un subespacio
b) Determinar la dimensión del espacio factible
c) Encontrar la dirección óptima de operación
d) Analizar la sensibilidad a perturbaciones

## 🔗 Conexiones con Temas Posteriores

### Hacia Matrices y Determinantes
- **Representación matricial** de transformaciones lineales
- **Determinantes** como medida de "volumen" en espacios vectoriales
- **Sistemas de ecuaciones** como aplicación directa

### Hacia Cálculo Diferencial
- **Espacios tangentes** como espacios vectoriales
- **Diferencial** como transformación lineal
- **Gradientes** como vectores en espacios duales

### Hacia Optimización
- **Programación lineal** en espacios vectoriales
- **Multiplicadores de Lagrange** y subespacios
- **Direcciones factibles** como elementos de subespacios

## 📚 Recursos Complementarios

### Para Profundización Teórica
- **Hoffman, K. & Kunze, R.** - "Linear Algebra" (2ª ed.)
- **Axler, S.** - "Linear Algebra Done Right" (3ª ed.)
- **Strang, G.** - "Introduction to Linear Algebra" (5ª ed.)

### Para Aplicaciones en Ingeniería
- **Aris, R.** - "Mathematical Modeling in Chemical Engineering"
- **Himmelblau, D.M.** - "Basic Principles and Calculations in Chemical Engineering"
- **Felder, R.M. & Rousseau, R.W.** - "Elementary Principles of Chemical Processes"

### Software y Herramientas
- **MATLAB**: Symbolic Math Toolbox para cálculos exactos
- **Python**: NumPy, SciPy, SymPy para álgebra lineal
- **Mathematica**: Para visualización y cálculos simbólicos

---

## 🏆 Objetivos de Aprendizaje Alcanzados

Al completar este tema, el estudiante habrá desarrollado:

### Competencias Conceptuales
- [x] Comprensión profunda de la estructura de espacios vectoriales
- [x] Dominio de conceptos de independencia lineal y base
- [x] Capacidad de análisis dimensional en sistemas complejos

### Competencias Procedimentales
- [x] Habilidad para verificar propiedades de subespacios
- [x] Destreza en cálculo de bases y dimensiones
- [x] Competencia en resolución de sistemas lineales

### Competencias Aplicadas
- [x] Capacidad de modelado matemático de procesos químicos
- [x] Habilidad para análisis de grados de libertad
- [x] Competencia en optimización con restricciones lineales

---

*Este desarrollo teórico proporciona una base sólida y rigurosa para el álgebra lineal aplicada a ingeniería química, integrando conceptos fundamentales con aplicaciones prácticas relevantes.*