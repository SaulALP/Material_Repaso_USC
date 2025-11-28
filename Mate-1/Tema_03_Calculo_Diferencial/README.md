# 📈 Tema 3: Cálculo Diferencial

## 🎯 Información del Tema

**Duración**: 8 horas expositivas + 3 horas seminario  
**Peso en la asignatura**: ~31% del contenido total  
**Prerrequisitos**: Tema 1 (Álgebra Lineal), Tema 2 (Geometría)  
**Conexiones**: Base fundamental para optimización y análisis de procesos  

## 📚 Objetivos de Aprendizaje

Al finalizar este tema, el estudiante será capaz de:

1. **Dominar** el concepto de límite y continuidad en funciones de una variable
2. **Calcular** derivadas usando diferentes técnicas y reglas
3. **Aplicar** el cálculo diferencial al análisis de velocidades de reacción
4. **Resolver** problemas de optimización en procesos químicos
5. **Interpretar** físicamente las derivadas en contextos de ingeniería
6. **Analizar** el comportamiento de funciones mediante derivadas

## 📖 Contenidos Teóricos

### 3.1 Límites y Continuidad
- Concepto intuitivo y formal de límite
- Propiedades de los límites
- Límites laterales e infinitos
- Continuidad y tipos de discontinuidades
- Teoremas fundamentales sobre funciones continuas

### 3.2 La Derivada
- Definición como límite del cociente incremental
- Interpretación geométrica y física
- Derivabilidad y continuidad
- Reglas básicas de derivación

### 3.3 Técnicas de Derivación
- Regla de la cadena
- Derivación implícita
- Derivación logarítmica
- Derivadas de funciones inversas

### 3.4 Aplicaciones de la Derivada
- Análisis de funciones: crecimiento, extremos, concavidad
- Problemas de optimización
- Velocidades relacionadas
- Aproximaciones lineales y diferenciales

### 3.5 Aplicaciones en Ingeniería Química
- Cinética de reacciones químicas
- Análisis de velocidades de transferencia
- Optimización de procesos
- Control automático de procesos

## ⏰ Distribución Temporal

| Contenido | Tiempo Estimado | Tipo de Clase |
|-----------|-----------------|---------------|
| Límites y continuidad | 2h | Expositiva |
| La derivada: concepto y cálculo | 2h | Expositiva |
| Técnicas de derivación | 2h | Expositiva |
| Aplicaciones de la derivada | 2h | Expositiva |
| Ejercicios y aplicaciones | 3h | Seminario |
| **TOTAL** | **11h** | **8h + 3h** |

## 📁 Recursos Disponibles

### 📖 Teoría
- **`theory/limites_continuidad.md`**: Conceptos fundamentales de límites
- **`theory/derivada_concepto.md`**: Definición y propiedades de la derivada
- **`theory/tecnicas_derivacion.md`**: Reglas y métodos de derivación
- **`theory/aplicaciones_derivada.md`**: Análisis de funciones y optimización
- **`theory/aplicaciones_ingenieria.md`**: Casos específicos en procesos químicos

### 🔢 Práctica
- **`practice/ejercicios_para_resolver.md`**: 12 ejercicios graduados en dificultad
- **`practice/ejercicios_resueltos.md`**: 6 ejercicios completamente desarrollados
- **`practice/hoja_respuestas.md`**: Resultados para verificación
- **`practice/problemas_optimizacion.md`**: Casos específicos de optimización

### 🎯 Material Complementario
- **`extras/software_calculo.md`**: Uso de MATLAB para cálculo simbólico
- **`extras/aplicaciones_cinetica.md`**: Análisis de velocidades de reacción
- **`extras/casos_industriales.md`**: Problemas reales de la industria química

## 📊 Criterios de Evaluación

### Conocimientos Básicos (30%)
- Cálculo de límites
- Aplicación de reglas de derivación
- Interpretación de derivadas

### Aplicación de Métodos (45%)
- Resolución de problemas de optimización
- Análisis de funciones
- Velocidades relacionadas
- Aproximaciones lineales

### Aplicaciones Prácticas (25%)
- Problemas de cinética química
- Optimización de procesos industriales
- Análisis de estabilidad de sistemas
- Control de procesos

## 🔗 Conexiones con Otros Temas

### Tema 1 (Álgebra Lineal)
- Aproximaciones lineales
- Sistemas de ecuaciones en optimización
- Análisis de sensibilidad

### Tema 2 (Geometría)
- Interpretación geométrica de la derivada
- Rectas tangentes y normales
- Optimización geométrica

### Tema 4 (Cálculo Integral)
- Teorema fundamental del cálculo
- Antiderivadas y primitivas
- Aplicaciones conjuntas

### Tema 6 (Optimización)
- Condiciones de optimalidad
- Métodos de optimización
- Análisis de sensibilidad

### Matemáticas II
- Derivadas parciales
- Gradientes y direcciones de máximo crecimiento
- Optimización multivariable

## 📚 Bibliografía Específica

### Principal
- **Ron Larson, Robert P. Hostetler, Bruce H. Edwards** - "Cálculo", Cap. 1-4
- **Eric Steiner** - "Matemáticas para las ciencias aplicadas", Cap. 4-5

### Complementaria
- **James Stewart** - "Cálculo de una variable" (8ª ed.), Cap. 2-4
- **Robert A. Adams, Christopher Essex** - "Cálculo: una variable" (9ª ed.), Cap. 1-4
- **Michael Spivak** - "Calculus" (4ª ed.), Cap. 5-10

## 🛠️ Herramientas Computacionales

### MATLAB
```matlab
% Ejemplo: Análisis de función y sus derivadas
syms x
f = x^3 - 6*x^2 + 9*x + 1;
df = diff(f, x);      % Primera derivada
d2f = diff(f, x, 2);  % Segunda derivada

% Encontrar puntos críticos
critical_points = solve(df == 0, x);

% Graficar función y derivadas
fplot(f, [-1, 5]); hold on;
fplot(df, [-1, 5]);
fplot(d2f, [-1, 5]);
legend('f(x)', "f'(x)", "f''(x)");
```

### Aplicaciones Recomendadas
- **MATLAB**: Cálculo simbólico y numérico
- **Mathematica**: Análisis simbólico avanzado
- **Python (SymPy)**: Cálculo simbólico libre
- **GeoGebra**: Visualización de conceptos

## ⚠️ Puntos Críticos

### Conceptos Difíciles
1. **Concepto de límite**: Requiere comprensión de aproximación
2. **Regla de la cadena**: Aplicación en funciones compuestas complejas
3. **Derivación implícita**: Técnica para funciones no explícitas
4. **Optimización**: Interpretación de condiciones de optimalidad

### Errores Comunes
- Confundir límite con valor de la función
- Aplicación incorrecta de la regla de la cadena
- No verificar condiciones de optimalidad
- Interpretación errónea de derivadas en contexto físico

## 🎯 Estrategias de Estudio

### Recomendaciones
1. **Práctica sistemática**: Resolver ejercicios de complejidad creciente
2. **Visualización**: Usar gráficas para entender comportamiento de funciones
3. **Aplicaciones**: Conectar con problemas reales de ingeniería química
4. **Verificación**: Usar software para comprobar cálculos

### Tiempo de Estudio Estimado
- **Estudio teórico**: 10 horas
- **Resolución de ejercicios**: 15 horas
- **Práctica con software**: 4 horas
- **Aplicaciones industriales**: 3 horas
- **Repaso y síntesis**: 3 horas
- **TOTAL**: 35 horas de trabajo personal

## 🔬 Aplicaciones Específicas en Ingeniería Química

### Cinética de Reacciones
- **Velocidad de reacción**: $r = -\frac{dC_A}{dt} = kC_A^n$
- **Análisis de orden de reacción**: Determinación de $n$ mediante derivadas
- **Tiempo de vida media**: Cálculo para diferentes órdenes de reacción

### Transferencia de Masa y Calor
- **Ley de Fick**: $J = -D\frac{dC}{dx}$ (flujo difusivo)
- **Ley de Fourier**: $q = -k\frac{dT}{dx}$ (flujo de calor)
- **Perfiles de concentración y temperatura**: Análisis mediante derivadas

### Optimización de Procesos
- **Maximización de conversión**: Optimización de condiciones de operación
- **Minimización de costos**: Análisis económico de procesos
- **Eficiencia energética**: Optimización de intercambiadores de calor

### Control de Procesos
- **Controladores PID**: Uso de derivadas en algoritmos de control
- **Análisis de estabilidad**: Derivadas en análisis de sistemas dinámicos
- **Respuesta transitoria**: Caracterización mediante derivadas

### Diseño de Reactores
- **Reactores de flujo pistón**: Análisis de perfiles de concentración
- **Reactores CSTR**: Optimización de volumen y tiempo de residencia
- **Reactores de lecho fijo**: Análisis de gradientes de concentración

## 📋 Lista de Verificación

Antes de continuar al siguiente tema, asegúrate de poder:

- [ ] Calcular límites usando diferentes técnicas
- [ ] Aplicar todas las reglas de derivación correctamente
- [ ] Resolver problemas de optimización paso a paso
- [ ] Interpretar físicamente el significado de derivadas
- [ ] Analizar el comportamiento completo de una función
- [ ] Aplicar derivadas a problemas de cinética química
- [ ] Usar software para verificar cálculos analíticos

## 🌟 Casos de Estudio

### Caso 1: Optimización de Reactor Batch
Determinar el tiempo óptimo de reacción que maximiza la concentración del producto deseado en una reacción consecutiva A → B → C.

### Caso 2: Análisis de Estabilidad de CSTR
Analizar la estabilidad de un reactor continuo mediante el estudio de las derivadas de las ecuaciones de balance.

### Caso 3: Diseño de Intercambiador de Calor
Optimizar las dimensiones de un intercambiador para minimizar el costo total considerando costos de capital y operación.

### Caso 4: Control de Temperatura en Reactor
Diseñar un sistema de control que mantenga la temperatura óptima usando la derivada del error como señal de control.

## 🎓 Competencias Desarrolladas

### Competencias Conceptuales
- Comprensión profunda del concepto de derivada
- Dominio de técnicas de derivación
- Capacidad de análisis de funciones

### Competencias Procedimentales
- Habilidad para resolver problemas de optimización
- Destreza en el cálculo de límites y derivadas
- Competencia en análisis gráfico de funciones

### Competencias Aplicadas
- Capacidad de modelado matemático de procesos químicos
- Habilidad para optimización de procesos industriales
- Competencia en análisis de cinética de reacciones

---

*Tiempo total estimado: 35 horas de trabajo personal + 11 horas presenciales = 46 horas*

*Este tema proporciona las herramientas fundamentales del cálculo diferencial para el análisis cuantitativo y la optimización de procesos químicos.*