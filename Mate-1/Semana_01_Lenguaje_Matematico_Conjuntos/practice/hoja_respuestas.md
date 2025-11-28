# Hoja de Respuestas - Semana 01

## 📋 Instrucciones

Esta hoja contiene únicamente los resultados finales. Para el desarrollo completo, consulta los [ejercicios resueltos](ejercicios_resueltos.md).

---

## Ejercicio 1: Operaciones con Conjuntos

**a)** 
- $A \cup B = \{1, 2, 3, 4, 5, 6, 7\}$
- $A \cap B = \{3, 4, 5\}$  
- $A \setminus B = \{1, 2\}$

**b)** $(A \cup B) \cap C = \{1, 3, 5, 7\}$

**c)** Sí se cumple la ley distributiva:
- $A \cap (B \cup C) = \{1, 3, 4, 5\}$
- $(A \cap B) \cup (A \cap C) = \{1, 3, 4, 5\}$

---

## Ejercicio 2: Cuantificadores y Proposiciones

**a)** Valores de verdad:
- $P$: **Verdadera** (todo real al cuadrado es no negativo)
- $Q$: **Falsa** (no existe real cuyo cuadrado sea negativo)
- $R$: **Verdadera** (si $x > 0$, entonces $x^2 > 0$)

**b)** Negaciones:
- $\neg P$: $\exists x \in \mathbb{R} : x^2 < 0$
- $\neg Q$: $\forall x \in \mathbb{R}, x^2 \neq -1$
- $\neg R$: $\exists x \in \mathbb{R} : x > 0 \land x^2 \leq 0$

**c)** $(P \land \neg Q) \Rightarrow R$ es **Verdadera**

---

## Ejercicio 3: Demostraciones con Conjuntos

**a)** Demostración completa por doble inclusión (ver ejercicios resueltos)

**b)** Demostración: Si $x \in A \cap C$, entonces $x \in A$ y $x \in C$. Como $A \subseteq B$, tenemos $x \in B$, luego $x \in B \cap C$.

**c)** Contraejemplo: $A = \{1\}$, $B = \{2\}$, $C = \{3\}$
- $A \cup B = \{1, 2\}$ y $A \cup C = \{1, 3\}$
- $A \cup B \neq A \cup C$ pero $B \neq C$

---

## Ejercicio Adicional: Principio de Inclusión-Exclusión

**a)** Estudiantes que prefieren exactamente una materia: **35**

**b)** Estudiantes que prefieren al menos dos materias: **35**

**c)** Estudiantes que no prefieren ninguna materia: **10**

---

## 🔍 Verificación Rápida

| Ejercicio | Resultado Principal | Tipo |
|-----------|-------------------|------|
| 1a | $A \cup B = \{1,2,3,4,5,6,7\}$ | Conjunto |
| 1b | $(A \cup B) \cap C = \{1,3,5,7\}$ | Conjunto |
| 1c | Ley distributiva verificada | Booleano |
| 2a | $P$: V, $Q$: F, $R$: V | Valores verdad |
| 2c | $(P \land \neg Q) \Rightarrow R$ es V | Valor verdad |
| 3c | Contraejemplo encontrado | Conjuntos específicos |
| Adicional a | 35 estudiantes | Número |
| Adicional b | 35 estudiantes | Número |
| Adicional c | 10 estudiantes | Número |

---

## ⚠️ Notas Importantes

- **Precisión**: Los conjuntos están escritos en orden creciente para facilitar verificación
- **Notación**: Se usa la notación estándar de conjuntos con llaves $\{...\}$
- **Casos especiales**: En el ejercicio adicional, la suma total debe ser 100 estudiantes

---

**Fecha de creación**: 2024-11-28  
**Última actualización**: 2024-11-28