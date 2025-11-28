# Ejercicios para Resolver - Semana 01

## 📋 Instrucciones Generales

- Resuelve cada ejercicio paso a paso
- Justifica todos los procedimientos utilizados
- Verifica tus respuestas cuando sea posible
- Consulta la [hoja de respuestas](hoja_respuestas.md) solo después de intentar resolver

---

## Ejercicio 1: Operaciones con Conjuntos

**Dificultad**: ⭐⭐☆☆☆ (2/5)  
**Tiempo estimado**: 20 minutos  
**Conceptos**: Operaciones básicas con conjuntos, diagramas de Venn

### Enunciado

Sean los conjuntos:
- $A = \{1, 2, 3, 4, 5\}$
- $B = \{3, 4, 5, 6, 7\}$
- $C = \{1, 3, 5, 7, 9\}$

**Se pide:**
a) Calcular $A \cup B$, $A \cap B$ y $A \setminus B$
b) Determinar $(A \cup B) \cap C$
c) Verificar si se cumple la ley distributiva: $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

### Ayuda
> **💡 Pista**: Para la parte c), calcula ambos lados de la igualdad por separado y compara los resultados.

---

## Ejercicio 2: Cuantificadores y Proposiciones

**Dificultad**: ⭐⭐⭐☆☆ (3/5)  
**Tiempo estimado**: 25 minutos  
**Conceptos**: Cuantificadores, negación de proposiciones, lógica proposicional

### Enunciado

Considera las siguientes proposiciones sobre números reales:

- $P$: $\forall x \in \mathbb{R}, x^2 \geq 0$
- $Q$: $\exists x \in \mathbb{R} : x^2 = -1$
- $R$: $\forall x \in \mathbb{R}, x > 0 \Rightarrow x^2 > 0$

**Se pide:**
a) Determinar el valor de verdad de cada proposición ($P$, $Q$, $R$)
b) Escribir la negación de cada proposición usando símbolos matemáticos
c) Evaluar la proposición compuesta: $(P \land \neg Q) \Rightarrow R$

### Ayuda
> **💡 Pista**: Recuerda que la negación de $\forall x, P(x)$ es $\exists x : \neg P(x)$, y la negación de $\exists x : P(x)$ es $\forall x, \neg P(x)$.

---

## Ejercicio 3: Demostraciones con Conjuntos

**Dificultad**: ⭐⭐⭐⭐☆ (4/5)  
**Tiempo estimado**: 35 minutos  
**Conceptos**: Demostraciones formales, inclusión de conjuntos, propiedades de operaciones

### Enunciado

Sean $A$, $B$ y $C$ conjuntos cualesquiera.

**Se pide:**
a) Demostrar que $A \cap (B \setminus C) = (A \cap B) \setminus C$
b) Demostrar que si $A \subseteq B$, entonces $A \cap C \subseteq B \cap C$ para cualquier conjunto $C$
c) Encontrar un contraejemplo que muestre que la proposición "$A \cup B = A \cup C \Rightarrow B = C$" es falsa

### Ayuda
> **💡 Pista**: Para las demostraciones, usa el método de doble inclusión. Para el contraejemplo, busca conjuntos específicos donde la implicación falle.

---

## Ejercicio Adicional (Opcional): Principio de Inclusión-Exclusión

**Dificultad**: ⭐⭐⭐⭐⭐ (5/5)  
**Tiempo estimado**: 40 minutos  
**Conceptos**: Cardinalidad, principio de inclusión-exclusión, conjuntos finitos

### Enunciado

En una encuesta a 100 estudiantes sobre sus preferencias en matemáticas:
- 60 estudiantes prefieren Álgebra
- 45 estudiantes prefieren Análisis  
- 30 estudiantes prefieren Geometría
- 25 estudiantes prefieren tanto Álgebra como Análisis
- 15 estudiantes prefieren tanto Álgebra como Geometría
- 10 estudiantes prefieren tanto Análisis como Geometría
- 5 estudiantes prefieren las tres materias

**Se pide:**
Determinar cuántos estudiantes:
a) Prefieren exactamente una materia
b) Prefieren al menos dos materias
c) No prefieren ninguna de las tres materias

### Ayuda
> **💡 Pista**: Usa el principio de inclusión-exclusión: $|A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C|$

---

## 🎯 Objetivos de Práctica

Al completar estos ejercicios deberías ser capaz de:

- [ ] **Realizar operaciones básicas con conjuntos** de manera fluida
- [ ] **Interpretar y construir proposiciones** con cuantificadores
- [ ] **Aplicar métodos de demostración** para propiedades de conjuntos
- [ ] **Resolver problemas de cardinalidad** usando principios combinatorios

---

## 📚 Recursos de Apoyo

- **Teoría relacionada**: [theory/lenguaje_matematico.md](../theory/lenguaje_matematico.md)
- **Ejercicios resueltos**: [ejercicios_resueltos.md](ejercicios_resueltos.md)
- **Fórmulas clave**: Sección 2.4 y 2.5 de la teoría (operaciones y propiedades)

---

**Fecha de creación**: 2024-11-28  
**Última actualización**: 2024-11-28