# 📐 Espacios Vectoriales

## 🎯 Introducción

Los espacios vectoriales constituyen la base fundamental del álgebra lineal y tienen aplicaciones directas en ingeniería química, desde el análisis de balances de materia hasta la optimización de procesos industriales.

## 📚 Definición de Espacio Vectorial

Un **espacio vectorial** $V$ sobre un cuerpo $\mathbb{K}$ (generalmente $\mathbb{R}$ o $\mathbb{C}$) es un conjunto no vacío dotado de dos operaciones:

1. **Suma de vectores**: $+: V \times V \rightarrow V$
2. **Producto por escalar**: $\cdot: \mathbb{K} \times V \rightarrow V$

### 🔢 Axiomas del Espacio Vectorial

Para todo $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$ y $\alpha, \beta \in \mathbb{K}$:

#### Axiomas de la Suma
1. **Conmutatividad**: $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$
2. **Asociatividad**: $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$
3. **Elemento neutro**: $\exists \mathbf{0} \in V : \mathbf{v} + \mathbf{0} = \mathbf{v}$
4. **Elemento opuesto**: $\forall \mathbf{v} \in V, \exists (-\mathbf{v}) \in V : \mathbf{v} + (-\mathbf{v}) = \mathbf{0}$

#### Axiomas del Producto por Escalar
5. **Asociatividad mixta**: $\alpha(\beta\mathbf{v}) = (\alpha\beta)\mathbf{v}$
6. **Elemento unidad**: $1 \cdot \mathbf{v} = \mathbf{v}$
7. **Distributividad respecto a la suma de vectores**: $\alpha(\mathbf{u} + \mathbf{v}) = \alpha\mathbf{u} + \alpha\mathbf{v}$
8. **Distributividad respecto a la suma de escalares**: $(\alpha + \beta)\mathbf{v} = \alpha\mathbf{v} + \beta\mathbf{v}$

## 🌟 Ejemplos Fundamentales

### Ejemplo 1: $\mathbb{R}^n$
El espacio $\mathbb{R}^n = \{(x_1, x_2, \ldots, x_n) : x_i \in \mathbb{R}\}$ con:
- Suma: $(x_1, \ldots, x_n) + (y_1, \ldots, y_n) = (x_1 + y_1, \ldots, x_n + y_n)$
- Producto: $\alpha(x_1, \ldots, x_n) = (\alpha x_1, \ldots, \alpha x_n)$

**Aplicación en Ingeniería**: Representación de concentraciones de $n$ componentes en un reactor.

### Ejemplo 2: Espacio de Matrices $M_{m \times n}(\mathbb{R})$
El conjunto de matrices reales $m \times n$ con suma y producto por escalar elemento a elemento.

**Aplicación en Ingeniería**: Matrices de coeficientes estequiométricos en sistemas de reacciones químicas.

### Ejemplo 3: Espacio de Funciones $C[a,b]$
El conjunto de funciones continuas en el intervalo $[a,b]$ con:
- Suma: $(f + g)(x) = f(x) + g(x)$
- Producto: $(\alpha f)(x) = \alpha f(x)$

**Aplicación en Ingeniería**: Perfiles de temperatura o concentración en reactores continuos.

## 🔍 Subespacios Vectoriales

### Definición
Un subconjunto $W \subseteq V$ es un **subespacio vectorial** si:
1. $\mathbf{0} \in W$
2. $\mathbf{u}, \mathbf{v} \in W \Rightarrow \mathbf{u} + \mathbf{v} \in W$ (cerrado para la suma)
3. $\mathbf{v} \in W, \alpha \in \mathbb{K} \Rightarrow \alpha\mathbf{v} \in W$ (cerrado para el producto por escalar)

### Ejemplo Práctico: Balance de Materia
En un sistema de $n$ componentes con $m$ reacciones, el espacio de vectores de velocidades de reacción que conservan la masa forma un subespacio de $\mathbb{R}^m$.

Si $\mathbf{A}$ es la matriz estequiométrica, entonces:
$$W = \{\mathbf{r} \in \mathbb{R}^m : \mathbf{A}\mathbf{r} = \mathbf{0}\}$$

## 🎯 Combinaciones Lineales

### Definición
Una **combinación lineal** de vectores $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k$ es:
$$\mathbf{v} = \alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_k\mathbf{v}_k$$

donde $\alpha_1, \alpha_2, \ldots, \alpha_k \in \mathbb{K}$.

### Espacio Generado
El **espacio generado** por $\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\}$ es:
$$\text{span}\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k\} = \left\{\sum_{i=1}^k \alpha_i\mathbf{v}_i : \alpha_i \in \mathbb{K}\right\}$$

## 🔗 Dependencia e Independencia Lineal

### Dependencia Lineal
Los vectores $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k$ son **linealmente dependientes** si existen escalares $\alpha_1, \alpha_2, \ldots, \alpha_k$, no todos nulos, tales que:
$$\alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_k\mathbf{v}_k = \mathbf{0}$$

### Independencia Lineal
Los vectores son **linealmente independientes** si la única solución de la ecuación anterior es $\alpha_1 = \alpha_2 = \cdots = \alpha_k = 0$.

### Ejemplo en Ingeniería Química
En un reactor con 3 componentes A, B, C y 2 reacciones:
- Reacción 1: $A + B \rightarrow C$
- Reacción 2: $2A + B \rightarrow 2C$

Los vectores estequiométricos son:
- $\mathbf{r}_1 = (-1, -1, 1)$
- $\mathbf{r}_2 = (-2, -1, 2)$

¿Son linealmente independientes? Resolvemos:
$$\alpha_1(-1, -1, 1) + \alpha_2(-2, -1, 2) = (0, 0, 0)$$

Sistema resultante:
$$\begin{cases}
-\alpha_1 - 2\alpha_2 = 0 \\
-\alpha_1 - \alpha_2 = 0 \\
\alpha_1 + 2\alpha_2 = 0
\end{cases}$$

De la segunda ecuación: $\alpha_1 = -\alpha_2$  
Sustituyendo en la primera: $\alpha_2 - 2\alpha_2 = -\alpha_2 = 0$  
Por tanto, $\alpha_1 = \alpha_2 = 0$, y los vectores son **linealmente independientes**.

## 📏 Base y Dimensión

### Base
Un conjunto $\mathcal{B} = \{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n\}$ es una **base** de $V$ si:
1. Los vectores son linealmente independientes
2. $\text{span}(\mathcal{B}) = V$

### Dimensión
La **dimensión** de $V$ es el número de vectores en cualquier base de $V$:
$$\dim(V) = |\mathcal{B}|$$

### Propiedades Importantes
- Todo espacio vectorial de dimensión finita tiene una base
- Todas las bases de un espacio vectorial tienen el mismo número de elementos
- En $\mathbb{R}^n$, cualquier conjunto de $n$ vectores linealmente independientes forma una base

## 🧮 Coordenadas

Si $\mathcal{B} = \{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n\}$ es una base de $V$, entonces todo vector $\mathbf{v} \in V$ se puede escribir de forma única como:
$$\mathbf{v} = \alpha_1\mathbf{v}_1 + \alpha_2\mathbf{v}_2 + \cdots + \alpha_n\mathbf{v}_n$$

El vector $[\mathbf{v}]_\mathcal{B} = (\alpha_1, \alpha_2, \ldots, \alpha_n)^T$ se llama **vector de coordenadas** de $\mathbf{v}$ respecto a la base $\mathcal{B}$.

## 🔬 Aplicación: Análisis de Grados de Libertad

En un proceso químico con:
- $n$ componentes
- $m$ reacciones independientes
- $p$ fases

El número de **grados de libertad** para especificar completamente el sistema es:
$$\text{GL} = n - m - p + 2$$

Este análisis se basa en conceptos de dimensión de espacios vectoriales y independencia lineal de las ecuaciones de balance.

## 📊 Resumen de Conceptos Clave

| Concepto | Definición | Aplicación en Ingeniería |
|----------|------------|-------------------------|
| Espacio Vectorial | Conjunto con suma y producto por escalar | Espacio de estados de un proceso |
| Subespacio | Subconjunto cerrado para operaciones | Restricciones de balance de materia |
| Independencia Lineal | No hay combinación lineal nula no trivial | Reacciones químicas independientes |
| Base | Conjunto independiente que genera el espacio | Variables independientes del proceso |
| Dimensión | Número de elementos en una base | Grados de libertad del sistema |

## 🎯 Ejercicios de Autoevaluación

### Ejercicio 1
Determina si el conjunto $W = \{(x, y, z) \in \mathbb{R}^3 : x + 2y - z = 0\}$ es un subespacio vectorial de $\mathbb{R}^3$.

### Ejercicio 2
En un reactor con componentes A, B, C, D y reacciones:
- $A + B \rightarrow C$
- $2A + C \rightarrow D$
- $B + C \rightarrow A + D$

Determina si las tres reacciones son linealmente independientes.

### Ejercicio 3
Encuentra una base para el espacio solución del sistema homogéneo:
$$\begin{cases}
x_1 + 2x_2 - x_3 + x_4 = 0 \\
2x_1 + 4x_2 + x_3 - 2x_4 = 0
\end{cases}$$

---

## 🔗 Conexiones

- **Siguiente tema**: Matrices y determinantes utilizarán estos conceptos
- **Aplicaciones**: Sistemas de ecuaciones lineales en balances de materia
- **Software**: MATLAB para verificación de independencia lineal

---

*Este contenido proporciona la base teórica fundamental para todo el álgebra lineal aplicada a ingeniería química.*