# 🎯 Tema 6: Optimización

## 🎯 Información del Tema

**Duración**: 4 horas expositivas + 1 hora seminario  
**Peso en la asignatura**: ~14% del contenido total  
**Prerrequisitos**: Tema 3 (Cálculo Diferencial), Tema 1 (Álgebra Lineal)  
**Conexiones**: Aplicación directa en diseño y operación de procesos químicos  

## 📚 Objetivos de Aprendizaje

Al finalizar este tema, el estudiante será capaz de:

1. **Formular** problemas de optimización en ingeniería química
2. **Aplicar** métodos de optimización sin restricciones
3. **Resolver** problemas de optimización con restricciones de igualdad
4. **Utilizar** multiplicadores de Lagrange efectivamente
5. **Optimizar** procesos químicos industriales
6. **Interpretar** económicamente los resultados de optimización

## 📖 Contenidos Teóricos

### 6.1 Fundamentos de Optimización
- Conceptos básicos: función objetivo, variables de decisión, restricciones
- Clasificación de problemas de optimización
- Condiciones de optimalidad
- Interpretación geométrica

### 6.2 Optimización Sin Restricciones
- Condiciones necesarias y suficientes
- Métodos analíticos: derivadas primera y segunda
- Puntos críticos: máximos, mínimos y puntos de silla
- Criterio de la segunda derivada

### 6.3 Optimización Con Restricciones de Igualdad
- Método de sustitución
- Multiplicadores de Lagrange
- Condiciones de Karush-Kuhn-Tucker (KKT)
- Interpretación económica de multiplicadores

### 6.4 Programación Lineal (Introducción)
- Formulación de problemas lineales
- Método gráfico para dos variables
- Conceptos básicos del método simplex
- Interpretación de soluciones

### 6.5 Aplicaciones en Ingeniería Química
- Optimización de reactores químicos
- Diseño óptimo de intercambiadores de calor
- Optimización de procesos de separación
- Planificación de producción
- Minimización de costos operativos

## ⏰ Distribución Temporal

| Contenido | Tiempo Estimado | Tipo de Clase |
|-----------|-----------------|---------------|
| Fundamentos de optimización | 1h | Expositiva |
| Optimización sin restricciones | 1h | Expositiva |
| Multiplicadores de Lagrange | 1.5h | Expositiva |
| Programación lineal básica | 0.5h | Expositiva |
| Ejercicios y aplicaciones | 1h | Seminario |
| **TOTAL** | **5h** | **4h + 1h** |

## 📁 Recursos Disponibles

### 📖 Teoría
- **`theory/fundamentos_optimizacion.md`**: Conceptos básicos y clasificación
- **`theory/optimizacion_sin_restricciones.md`**: Métodos analíticos
- **`theory/multiplicadores_lagrange.md`**: Optimización con restricciones
- **`theory/programacion_lineal.md`**: Introducción a PL
- **`theory/aplicaciones_ingenieria.md`**: Casos específicos en procesos químicos

### 🔢 Práctica
- **`practice/ejercicios_para_resolver.md`**: 12 ejercicios graduados
- **`practice/ejercicios_resueltos.md`**: 6 ejercicios completamente desarrollados
- **`practice/problemas_aplicados.md`**: Casos de optimización industrial
- **`practice/hoja_respuestas.md`**: Resultados para verificación

### 🎯 Material Complementario
- **`extras/software_optimizacion.md`**: Uso de MATLAB Optimization Toolbox
- **`extras/interpretacion_economica.md`**: Análisis económico de soluciones
- **`extras/casos_industriales.md`**: Problemas reales de la industria química

## 📊 Criterios de Evaluación

### Conocimientos Básicos (30%)
- Formulación de problemas de optimización
- Aplicación de condiciones de optimalidad
- Uso de multiplicadores de Lagrange

### Aplicación de Métodos (45%)
- Resolución de problemas sin restricciones
- Optimización con restricciones de igualdad
- Interpretación de resultados

### Aplicaciones Prácticas (25%)
- Optimización de reactores químicos
- Diseño óptimo de equipos
- Análisis económico de procesos
- Planificación de producción

## 🔗 Conexiones con Otros Temas

### Tema 1 (Álgebra Lineal)
- Sistemas de ecuaciones en condiciones KKT
- Análisis de matrices hessianas
- Espacios vectoriales de restricciones

### Tema 3 (Cálculo Diferencial)
- Derivadas en condiciones de optimalidad
- Análisis de funciones multivariables
- Aproximaciones lineales

### Tema 4 (Cálculo Integral)
- Optimización de funcionales
- Cálculo de variaciones
- Integrales en funciones objetivo

### Matemáticas II
- Optimización multivariable
- Gradientes y derivadas direccionales
- Métodos numéricos de optimización

### Asignaturas de Ingeniería
- **Diseño de Procesos**: Optimización de flowsheets
- **Control de Procesos**: Optimización de controladores
- **Economía**: Análisis de costos y beneficios

## 📚 Bibliografía Específica

### Principal
- **Edgar, Himmelblau, Lasdon** - "Optimization of Chemical Processes" (2ª ed.), Cap. 1-8
- **Biegler, Grossmann, Westerberg** - "Systematic Methods of Chemical Process Design", Cap. 4-6

### Complementaria
- **Nocedal, Wright** - "Numerical Optimization" (2ª ed.), Cap. 1-3
- **Boyd, Vandenberghe** - "Convex Optimization", Cap. 1-5
- **Bazaraa, Sherali, Shetty** - "Nonlinear Programming" (3ª ed.), Cap. 1-4

## 🛠️ Herramientas Computacionales

### MATLAB
```matlab
% Ejemplo: Optimización de reactor CSTR
% Maximizar conversión sujeto a restricciones de temperatura

% Función objetivo: conversión X = k*tau/(1 + k*tau)
% donde k = k0*exp(-E/(R*T)) y tau = V/F

% Parámetros
k0 = 1e6;      % Factor pre-exponencial (1/min)
E = 8000;      % Energía de activación (cal/mol)
R = 1.987;     % Constante de gases (cal/mol·K)
F = 100;       % Flujo volumétrico (L/min)

% Variables de decisión: [V, T] (Volumen en L, Temperatura en K)
% Restricciones: 300 ≤ T ≤ 400, 50 ≤ V ≤ 500

% Función objetivo (negativa para maximización)
obj_fun = @(x) -(k0*exp(-E/(R*x(2)))*(x(1)/F)) / ...
               (1 + k0*exp(-E/(R*x(2)))*(x(1)/F));

% Restricciones de desigualdad: g(x) ≤ 0
% -T + 300 ≤ 0  →  T ≥ 300
% T - 400 ≤ 0   →  T ≤ 400
% -V + 50 ≤ 0   →  V ≥ 50
% V - 500 ≤ 0   →  V ≤ 500
A = [-1, 0; 1, 0; 0, -1; 0, 1];
b = [-50; 500; -300; 400];

% Punto inicial
x0 = [200, 350];

% Optimización
options = optimoptions('fmincon', 'Display', 'iter');
[x_opt, f_opt] = fmincon(obj_fun, x0, A, b, [], [], [], [], [], options);

% Resultados
V_opt = x_opt(1);
T_opt = x_opt(2);
X_opt = -f_opt;
k_opt = k0*exp(-E/(R*T_opt));
tau_opt = V_opt/F;

fprintf('Resultados de Optimización\n');
fprintf('=========================\n');
fprintf('Volumen óptimo: %.1f L\n', V_opt);
fprintf('Temperatura óptima: %.1f K\n', T_opt);
fprintf('Conversión máxima: %.3f\n', X_opt);
fprintf('Constante de velocidad: %.2e 1/min\n', k_opt);
fprintf('Tiempo de residencia: %.2f min\n', tau_opt);
```

### Aplicaciones Recomendadas
- **MATLAB**: Optimization Toolbox
- **Python**: SciPy.optimize, CVXPY
- **GAMS**: Modelado de optimización a gran escala
- **Excel Solver**: Problemas pequeños de optimización

## ⚠️ Puntos Críticos

### Conceptos Difíciles
1. **Multiplicadores de Lagrange**: Interpretación física y económica
2. **Condiciones KKT**: Aplicación a problemas complejos
3. **Convexidad**: Identificación de problemas convexos
4. **Interpretación de resultados**: Significado práctico de soluciones

### Errores Comunes
- Formulación incorrecta del problema
- No verificar condiciones suficientes de optimalidad
- Interpretación errónea de multiplicadores de Lagrange
- Ignorar restricciones activas en la solución

## 🎯 Estrategias de Estudio

### Recomendaciones
1. **Formulación sistemática**: Seguir pasos estructurados
2. **Verificación gráfica**: Visualizar problemas bidimensionales
3. **Interpretación física**: Conectar con fenómenos reales
4. **Uso de software**: Validar soluciones analíticas

### Tiempo de Estudio Estimado
- **Estudio teórico**: 8 horas
- **Resolución de ejercicios**: 12 horas
- **Práctica con software**: 4 horas
- **Casos industriales**: 3 horas
- **Repaso y síntesis**: 2 horas
- **TOTAL**: 29 horas de trabajo personal

## 🔬 Aplicaciones Específicas en Ingeniería Química

### Diseño de Reactores
- **Reactor CSTR**: Optimización de volumen y temperatura
- **Reactor PFR**: Perfil óptimo de temperatura
- **Reactores en serie**: Distribución óptima de volúmenes
- **Selectividad**: Maximización en reacciones paralelas

### Intercambiadores de Calor
- **Área mínima**: Optimización de configuración
- **Costo total**: Balance entre capital y operación
- **LMTD**: Maximización de diferencia de temperatura
- **Caída de presión**: Minimización con restricciones

### Procesos de Separación
- **Destilación**: Número óptimo de platos
- **Extracción**: Número de etapas y relación de solvente
- **Absorción**: Flujo óptimo de absorbente
- **Cristalización**: Condiciones óptimas de operación

### Planificación de Producción
- **Mezcla de productos**: Maximización de beneficios
- **Asignación de recursos**: Uso óptimo de equipos
- **Inventarios**: Minimización de costos de almacenamiento
- **Programación**: Secuenciación óptima de operaciones

### Análisis Económico
- **Valor presente neto**: Maximización de VPN
- **Tiempo de recuperación**: Minimización de payback
- **Análisis de sensibilidad**: Robustez de soluciones
- **Optimización multiobjetivo**: Balance de criterios

## 📋 Lista de Verificación

Antes de continuar al siguiente tema, asegúrate de poder:

- [ ] Formular problemas de optimización correctamente
- [ ] Aplicar condiciones de optimalidad sin restricciones
- [ ] Usar multiplicadores de Lagrange efectivamente
- [ ] Interpretar económicamente los multiplicadores
- [ ] Resolver problemas de programación lineal gráficamente
- [ ] Aplicar optimización a diseño de reactores
- [ ] Usar software de optimización básico

## 🌟 Casos de Estudio

### Caso 1: Optimización de Reactor Batch
Determinar el tiempo óptimo de reacción que maximiza el beneficio considerando costos de operación y valor del producto.

### Caso 2: Diseño de Red de Intercambiadores
Optimizar la configuración de una red de intercambiadores para minimizar el costo total de energía.

### Caso 3: Planificación de Producción Multiproducto
Determinar la mezcla óptima de productos que maximiza el beneficio sujeto a restricciones de capacidad.

### Caso 4: Optimización de Torre de Destilación
Encontrar el número óptimo de platos y la relación de reflujo que minimiza el costo total anualizado.

## 🎓 Competencias Desarrolladas

### Competencias Conceptuales
- Comprensión de principios de optimización
- Dominio de condiciones de optimalidad
- Capacidad de interpretación económica

### Competencias Procedimentales
- Habilidad para formular problemas de optimización
- Destreza en aplicación de métodos analíticos
- Competencia en uso de multiplicadores de Lagrange

### Competencias Aplicadas
- Capacidad de optimización de procesos químicos
- Habilidad para análisis económico de alternativas
- Competencia en toma de decisiones óptimas

## 🔄 Integración con Tecnologías Avanzadas

### Optimización Estocástica
- **Incertidumbre**: Optimización bajo incertidumbre
- **Programación estocástica**: Decisiones con información parcial
- **Optimización robusta**: Soluciones insensibles a perturbaciones

### Inteligencia Artificial
- **Algoritmos genéticos**: Optimización evolutiva
- **Redes neuronales**: Aproximación de funciones objetivo
- **Machine learning**: Optimización de hiperparámetros

### Optimización en Tiempo Real
- **Control predictivo**: MPC con optimización online
- **Optimización dinámica**: Problemas dependientes del tiempo
- **Sistemas adaptativos**: Optimización continua

---

*Tiempo total estimado: 29 horas de trabajo personal + 5 horas presenciales = 34 horas*

*Este tema proporciona las herramientas fundamentales de optimización para el diseño y operación eficiente de procesos químicos.*