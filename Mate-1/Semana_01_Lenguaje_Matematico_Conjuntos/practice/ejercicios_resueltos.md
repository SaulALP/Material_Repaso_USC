# Ejercicios Resueltos - Semana 01

## Ejercicio Resuelto 1: Demostración de Propiedades de Conjuntos

### 📋 Enunciado

Demostrar que para cualesquiera conjuntos $A$ y $B$: $(A \cup B) \setminus B = A \setminus B$

**Se pide:**
Realizar una demostración formal usando el método de doble inclusión.

---

### 🔍 Análisis Previo

**Conceptos involucrados:**
- Operaciones con conjuntos: unión, diferencia
- Método de demostración por doble inclusión
- Definiciones de pertenencia a conjuntos

**Estrategia de resolución:**
1. Demostrar que $(A \cup B) \setminus B \subseteq A \setminus B$
2. Demostrar que $A \setminus B \subseteq (A \cup B) \setminus B$
3. Concluir la igualdad por doble inclusión

---

### ✏️ Resolución Paso a Paso

### Paso 1: Demostrar $(A \cup B) \setminus B \subseteq A \setminus B$

Sea $x \in (A \cup B) \setminus B$ un elemento arbitrario.

Por definición de diferencia de conjuntos:
$$x \in (A \cup B) \setminus B \Leftrightarrow x \in (A \cup B) \land x \notin B$$

Como $x \in (A \cup B)$, por definición de unión:
$$x \in A \lor x \in B$$

Pero sabemos que $x \notin B$, por lo tanto:
$$x \in A$$

Combinando $x \in A$ y $x \notin B$:
$$x \in A \setminus B$$

Por tanto: $(A \cup B) \setminus B \subseteq A \setminus B$

### Paso 2: Demostrar $A \setminus B \subseteq (A \cup B) \setminus B$

Sea $x \in A \setminus B$ un elemento arbitrario.

Por definición de diferencia:
$$x \in A \setminus B \Leftrightarrow x \in A \land x \notin B$$

Como $x \in A$, por definición de unión:
$$x \in A \cup B$$

Combinando $x \in A \cup B$ y $x \notin B$:
$$x \in (A \cup B) \setminus B$$

Por tanto: $A \setminus B \subseteq (A \cup B) \setminus B$

### Paso 3: Conclusión

Por los pasos 1 y 2, tenemos:
- $(A \cup B) \setminus B \subseteq A \setminus B$
- $A \setminus B \subseteq (A \cup B) \setminus B$

Por definición de igualdad de conjuntos:
$$(A \cup B) \setminus B = A \setminus B$$

---

### 🎯 Resultado Final

**Demostración completa:** Hemos probado que $(A \cup B) \setminus B = A \setminus B$ para cualesquiera conjuntos $A$ y $B$.

---

### 💡 Comentario Conceptual

**¿Qué hemos aprendido?**

Esta demostración ilustra una propiedad fundamental de las operaciones con conjuntos: cuando restamos un conjunto $B$ de la unión $A \cup B$, el resultado es equivalente a restar $B$ solo de $A$. Esto tiene sentido intuitivo: los elementos de $B$ que estaban en la unión se eliminan completamente, dejando solo los elementos de $A$ que no estaban en $B$.

**Puntos clave:**
- **Método de doble inclusión**: Técnica estándar para demostrar igualdad de conjuntos
- **Definiciones operacionales**: Uso riguroso de las definiciones de unión y diferencia
- **Lógica proposicional**: Aplicación de conectivos lógicos ($\land$, $\lor$, $\neg$)

**Conexiones:**
- Se relaciona con las leyes de absorción en álgebra de conjuntos
- Prepara para demostraciones más complejas con múltiples operaciones
- Aplicación práctica en teoría de probabilidades y análisis combinatorio

---

## Ejercicio Resuelto 2: Análisis de Proposiciones con Cuantificadores

### 📋 Enunciado

Analizar la siguiente proposición y determinar su valor de verdad:

$$\forall x \in \mathbb{R}, \exists y \in \mathbb{R} : x + y = 0$$

**Se pide:**
a) Determinar si la proposición es verdadera o falsa
b) Escribir la negación de la proposición
c) Proporcionar una interpretación en lenguaje natural

---

### 🔍 Análisis Previo

**Conceptos involucrados:**
- Cuantificadores universal ($\forall$) y existencial ($\exists$)
- Negación de proposiciones cuantificadas
- Propiedades de los números reales

**Estrategia de resolución:**
1. Interpretar la proposición en lenguaje natural
2. Analizar si para cada $x$ real existe un $y$ real que satisface la condición
3. Construir la negación usando las reglas de cuantificadores

---

### ✏️ Resolución Paso a Paso

### Paso 1: Interpretación en lenguaje natural

La proposición afirma:
"Para todo número real $x$, existe un número real $y$ tal que $x + y = 0$"

En otras palabras: "Todo número real tiene un opuesto aditivo en los reales"

### Paso 2: Análisis de veracidad

Para cualquier $x \in \mathbb{R}$, podemos tomar $y = -x$.

**Verificación:**
- $y = -x \in \mathbb{R}$ (el opuesto de un real es real)
- $x + y = x + (-x) = 0$ ✓

Como para cada $x$ real podemos encontrar un $y$ real (específicamente $y = -x$) que satisface la ecuación, la proposición es **VERDADERA**.

### Paso 3: Construcción de la negación

Aplicando las reglas de negación de cuantificadores:
$$\neg(\forall x \in \mathbb{R}, \exists y \in \mathbb{R} : x + y = 0)$$

$$\equiv \exists x \in \mathbb{R} : \neg(\exists y \in \mathbb{R} : x + y = 0)$$

$$\equiv \exists x \in \mathbb{R} : \forall y \in \mathbb{R}, x + y \neq 0$$

**En lenguaje natural:** "Existe un número real $x$ tal que para todo número real $y$, se cumple que $x + y \neq 0$"

---

### 🎯 Resultado Final

**Respuesta a):** La proposición es **VERDADERA**

**Respuesta b):** $\exists x \in \mathbb{R} : \forall y \in \mathbb{R}, x + y \neq 0$

**Respuesta c):** "Todo número real tiene un opuesto aditivo"

---

### 💡 Comentario Conceptual

**¿Qué hemos aprendido?**

Este ejercicio demuestra la importancia de los cuantificadores en matemáticas y cómo se relacionan con propiedades algebraicas fundamentales. La proposición original expresa la propiedad de que $(\mathbb{R}, +)$ es un grupo abeliano (todo elemento tiene inverso aditivo).

**Puntos clave:**
- **Orden de cuantificadores**: $\forall x \exists y$ significa que $y$ puede depender de $x$
- **Negación sistemática**: Aplicación de las reglas $\neg\forall \equiv \exists\neg$ y $\neg\exists \equiv \forall\neg$
- **Conexión con álgebra**: La proposición expresa una propiedad estructural de los números reales

**Conexiones:**
- Se relaciona con la estructura de grupo de $(\mathbb{R}, +)$
- Prepara para el estudio de espacios vectoriales y estructuras algebraicas
- Aplicación en resolución de ecuaciones lineales

---

## ⚠️ Errores Comunes

### En Demostraciones de Conjuntos:
1. **Confundir $\in$ con $\subseteq$**: $\{1\} \in \{\{1\}, 2\}$ vs $\{1\} \subseteq \{1, 2\}$
2. **Omitir casos en la demostración**: No considerar todos los casos posibles en uniones
3. **Usar elementos específicos**: Demostrar solo con ejemplos en lugar de elementos arbitrarios

### En Proposiciones con Cuantificadores:
1. **Intercambiar el orden**: $\forall x \exists y$ ≠ $\exists y \forall x$
2. **Negar incorrectamente**: Olvidar cambiar $\forall$ por $\exists$ al negar
3. **Interpretación ambigua**: No especificar claramente el dominio de los cuantificadores

---

**Dificultad**: ⭐⭐⭐☆☆ (3/5)  
**Tiempo estimado**: 30 minutos cada ejercicio  
**Conceptos clave**: Demostraciones formales, cuantificadores, operaciones con conjuntos