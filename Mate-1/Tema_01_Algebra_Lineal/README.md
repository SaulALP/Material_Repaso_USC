# 📐 Tema 1: Álgebra Lineal

## 🎯 Información del Tema

**Duración**: 4 horas expositivas + 1 hora seminario  
**Peso en la asignatura**: ~14% del contenido total  
**Prerrequisitos**: Matemáticas de Bachillerato  
**Conexiones**: Base fundamental para todos los temas posteriores  

## 📚 Objetivos de Aprendizaje

Al finalizar este tema, el estudiante será capaz de:

1. **Comprender** los conceptos fundamentales de espacios vectoriales
2. **Operar** con matrices y calcular determinantes
3. **Resolver** sistemas de ecuaciones lineales por diferentes métodos
4. **Calcular** valores y vectores propios
5. **Aplicar** conceptos de álgebra lineal a problemas de ingeniería química

## 📖 Contenidos Teóricos

### 1.1 Espacios Vectoriales
- Definición y propiedades
- Subespacios vectoriales
- Dependencia e independencia lineal
- Base y dimensión

### 1.2 Matrices y Determinantes
- Operaciones con matrices
- Tipos especiales de matrices
- Cálculo de determinantes
- Propiedades de los determinantes

### 1.3 Sistemas de Ecuaciones Lineales
- Método de Gauss
- Método de Gauss-Jordan
- Regla de Cramer
- Interpretación geométrica

### 1.4 Valores y Vectores Propios
- Definición y cálculo
- Diagonalización de matrices
- Aplicaciones en ingeniería

### 1.5 Aplicaciones en Ingeniería Química
- Balances de materia
- Sistemas de reactores
- Análisis de procesos estacionarios

## ⏰ Distribución Temporal

| Contenido | Tiempo Estimado | Tipo de Clase |
|-----------|-----------------|---------------|
| Espacios vectoriales | 1h | Expositiva |
| Matrices y determinantes | 1.5h | Expositiva |
| Sistemas de ecuaciones | 1h | Expositiva |
| Valores propios | 0.5h | Expositiva |
| Ejercicios y aplicaciones | 1h | Seminario |
| **TOTAL** | **5h** | **4h + 1h** |

## 📁 Recursos Disponibles

### 📖 Teoría
- **`theory/espacios_vectoriales.md`**: Conceptos fundamentales y definiciones
- **`theory/matrices_determinantes.md`**: Operaciones matriciales y cálculo de determinantes
- **`theory/sistemas_ecuaciones.md`**: Métodos de resolución
- **`theory/valores_propios.md`**: Diagonalización y aplicaciones

### 🔢 Práctica
- **`practice/ejercicios_para_resolver.md`**: 6 ejercicios graduados en dificultad
- **`practice/ejercicios_resueltos.md`**: 3 ejercicios completamente desarrollados
- **`practice/hoja_respuestas.md`**: Resultados para verificación

### 🎯 Material Complementario
- **`extras/aplicaciones_ingenieria.md`**: Casos prácticos en procesos químicos
- **`extras/software_matlab.md`**: Uso de MATLAB para álgebra lineal
- **`extras/problemas_adicionales.md`**: Ejercicios de profundización

## 📊 Criterios de Evaluación

### Conocimientos Básicos (40%)
- Definiciones de espacios vectoriales
- Operaciones con matrices
- Cálculo de determinantes

### Aplicación de Métodos (40%)
- Resolución de sistemas de ecuaciones
- Cálculo de valores propios
- Interpretación de resultados

### Aplicaciones Prácticas (20%)
- Problemas de ingeniería química
- Uso de software matemático
- Análisis crítico de soluciones

## 🔗 Conexiones con Otros Temas

### Tema 2 (Geometría)
- Representación vectorial de rectas y planos
- Transformaciones lineales

### Tema 3 (Cálculo Diferencial)
- Matrices jacobianas
- Sistemas de ecuaciones diferenciales

### Tema 6 (Optimización)
- Métodos de optimización lineal
- Análisis de sensibilidad

### Matemáticas II
- Cálculo vectorial
- Campos vectoriales

## 📚 Bibliografía Específica

### Principal
- **David C. Lay** - "Algebra lineal y sus aplicaciones" (4ª ed.), Cap. 1-5
- **Eric Steiner** - "Matemáticas para las ciencias aplicadas", Cap. 3

### Complementaria
- **Aranda, E.** - "Álgebra lineal con aplicaciones y Python", Cap. 1-4
- **David Poole** - "Algebra lineal. Una introducción moderna" (3ª ed.), Cap. 1-6

## 🛠️ Herramientas Computacionales

### MATLAB
```matlab
% Ejemplo básico de operaciones matriciales
A = [1 2; 3 4];
B = [5 6; 7 8];
C = A * B;  % Multiplicación de matrices
det_A = det(A);  % Determinante
[V, D] = eig(A);  % Valores y vectores propios
```

### Aplicaciones Recomendadas
- **MATLAB**: Cálculos matriciales avanzados
- **Octave**: Alternativa libre a MATLAB
- **Python (NumPy)**: Para programación científica

## ⚠️ Puntos Críticos

### Conceptos Difíciles
1. **Independencia lineal**: Requiere práctica con ejemplos
2. **Interpretación geométrica**: Visualización en 2D y 3D
3. **Valores propios**: Conexión con aplicaciones físicas

### Errores Comunes
- Confundir dependencia con independencia lineal
- Errores de cálculo en determinantes grandes
- Interpretación incorrecta de soluciones de sistemas

## 🎯 Estrategias de Estudio

### Recomendaciones
1. **Práctica regular**: Resolver ejercicios diariamente
2. **Visualización**: Usar gráficos para conceptos geométricos
3. **Software**: Verificar cálculos con herramientas computacionales
4. **Aplicaciones**: Conectar con problemas de ingeniería

### Tiempo de Estudio Estimado
- **Estudio teórico**: 6 horas
- **Resolución de ejercicios**: 8 horas
- **Práctica con software**: 2 horas
- **Repaso y síntesis**: 2 horas
- **TOTAL**: 18 horas de trabajo personal

---

## 📋 Lista de Verificación

Antes de continuar al siguiente tema, asegúrate de poder:

- [ ] Definir qué es un espacio vectorial
- [ ] Calcular determinantes de matrices 3×3
- [ ] Resolver sistemas de ecuaciones por Gauss
- [ ] Encontrar valores propios de una matriz 2×2
- [ ] Aplicar álgebra lineal a un problema de balances de materia
- [ ] Usar MATLAB para operaciones matriciales básicas

---

*Tiempo total estimado: 18 horas de trabajo personal + 5 horas presenciales = 23 horas*