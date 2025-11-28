# 🌐 Tema 2: Cálculo Diferencial Multivariable

## 🎯 Información del Tema

**Duración**: 8 horas expositivas + 3 horas seminario  
**Peso en la asignatura**: ~31% del contenido total  
**Prerrequisitos**: Tema 1 (Geometría del Plano y Espacio), Matemáticas I completo  
**Conexiones**: Base fundamental para optimización multivariable y análisis vectorial  

## 📚 Objetivos de Aprendizaje

Al finalizar este tema, el estudiante será capaz de:

1. **Calcular** límites y analizar continuidad en funciones multivariables
2. **Determinar** derivadas parciales y direccionales
3. **Aplicar** la regla de la cadena multivariable
4. **Encontrar** planos tangentes y aproximaciones lineales
5. **Resolver** problemas de optimización con restricciones
6. **Modelar** fenómenos multivariables en procesos químicos

## 📖 Contenidos Teóricos

### 2.1 Funciones de Varias Variables
- Dominio y rango de funciones multivariables
- Representaciones gráficas: curvas de nivel, superficies
- Límites y continuidad en varias variables
- Teoremas de continuidad

### 2.2 Derivadas Parciales
- Definición e interpretación geométrica
- Derivadas parciales de orden superior
- Teorema de Schwarz (igualdad de derivadas mixtas)
- Aplicaciones en gradientes de concentración y temperatura

### 2.3 Diferenciabilidad y Aproximación Lineal
- Diferencial total
- Planos tangentes a superficies
- Aproximaciones lineales y propagación de errores
- Teorema de la función implícita

### 2.4 Regla de la Cadena Multivariable
- Regla de la cadena para funciones compuestas
- Derivación implícita multivariable
- Cambio de variables
- Aplicaciones en termodinámica

### 2.5 Derivadas Direccionales y Gradiente
- Definición de derivada direccional
- Vector gradiente y sus propiedades
- Interpretación física del gradiente
- Aplicaciones en transferencia de masa y calor

### 2.6 Optimización Multivariable
- Extremos locales: condiciones necesarias y suficientes
- Multiplicadores de Lagrange para restricciones
- Optimización con múltiples restricciones
- Aplicaciones en diseño de procesos

## ⏰ Distribución Temporal

| Contenido | Tiempo Estimado | Tipo de Clase |
|-----------|-----------------|---------------|
| Funciones multivariables y límites | 1.5h | Expositiva |
| Derivadas parciales | 2h | Expositiva |
| Diferenciabilidad y aproximación | 1.5h | Expositiva |
| Regla de la cadena multivariable | 1.5h | Expositiva |
| Gradiente y derivadas direccionales | 1.5h | Expositiva |
| Ejercicios y aplicaciones | 3h | Seminario |
| **TOTAL** | **11h** | **8h + 3h** |

## 📁 Recursos Disponibles

### 📖 Teoría
- **`theory/funciones_multivariables.md`**: Conceptos fundamentales
- **`theory/derivadas_parciales.md`**: Cálculo de derivadas parciales
- **`theory/diferenciabilidad.md`**: Diferencial total y aproximaciones
- **`theory/regla_cadena.md`**: Regla de la cadena multivariable
- **`theory/gradiente.md`**: Vector gradiente y derivadas direccionales
- **`theory/optimizacion_multivariable.md`**: Extremos y multiplicadores de Lagrange

### 🔢 Práctica
- **`practice/ejercicios_para_resolver.md`**: 15 ejercicios graduados
- **`practice/ejercicios_resueltos.md`**: 8 ejercicios completamente desarrollados
- **`practice/problemas_optimizacion.md`**: Casos de optimización multivariable
- **`practice/hoja_respuestas.md`**: Resultados para verificación

### 🎯 Material Complementario
- **`extras/software_multivariable.md`**: Uso de MATLAB para cálculo multivariable
- **`extras/visualizacion_3d.md`**: Herramientas de visualización avanzada
- **`extras/aplicaciones_termodinamica.md`**: Casos específicos en termodinámica

## 📊 Criterios de Evaluación

### Conocimientos Básicos (30%)
- Cálculo de derivadas parciales
- Aplicación de la regla de la cadena
- Interpretación geométrica de conceptos

### Aplicación de Métodos (45%)
- Resolución de problemas de optimización
- Cálculo de planos tangentes
- Análisis de funciones multivariables
- Propagación de errores

### Aplicaciones Prácticas (25%)
- Modelado de procesos multivariables
- Optimización de sistemas químicos
- Análisis de sensibilidad
- Diseño de experimentos

## 🔗 Conexiones con Otros Temas

### Tema 1 (Geometría del Plano y Espacio)
- Superficies y curvas de nivel
- Planos tangentes
- Sistemas de coordenadas

### Tema 3 (Cálculo Integral Multivariable)
- Teorema fundamental del cálculo multivariable
- Integrales de funciones multivariables
- Aplicaciones conjuntas

### Tema 5 (Optimización Multivariable)
- Condiciones de optimalidad
- Métodos numéricos de optimización
- Análisis de sensibilidad

### Asignaturas de Ingeniería
- **Termodinámica**: Relaciones de Maxwell
- **Transferencia**: Gradientes de concentración y temperatura
- **Control**: Sistemas multivariables

## 🛠️ Herramientas Computacionales

### MATLAB
```matlab
% Ejemplo: Análisis de función de dos variables
% f(x,y) = x²y - xy² + xy (función de producción química)

% Definir función simbólica
syms x y
f = x^2*y - x*y^2 + x*y;

% Derivadas parciales
fx = diff(f, x);
fy = diff(f, y);
fxx = diff(fx, x);
fyy = diff(fy, y);
fxy = diff(fx, y);

fprintf('Función: f(x,y) = %s\n', char(f));
fprintf('∂f/∂x = %s\n', char(fx));
fprintf('∂f/∂y = %s\n', char(fy));
fprintf('∂²f/∂x² = %s\n', char(fxx));
fprintf('∂²f/∂y² = %s\n', char(fyy));
fprintf('∂²f/∂x∂y = %s\n', char(fxy));

% Gradiente
grad_f = [fx; fy];
fprintf('∇f = [%s; %s]\n', char(fx), char(fy));

% Puntos críticos
critical_eqs = [fx == 0, fy == 0];
critical_points = solve(critical_eqs, [x, y]);
fprintf('Puntos críticos:\n');
for i = 1:length(critical_points.x)
    fprintf('  (%s, %s)\n', char(critical_points.x(i)), char(critical_points.y(i)));
end

% Visualización
[X, Y] = meshgrid(-2:0.1:2, -2:0.1:2);
F = X.^2.*Y - X.*Y.^2 + X.*Y;

figure;
subplot(2,2,1);
surf(X, Y, F);
title('Superficie f(x,y)');
xlabel('x'); ylabel('y'); zlabel('f(x,y)');

subplot(2,2,2);
contour(X, Y, F, 20);
title('Curvas de Nivel');
xlabel('x'); ylabel('y');

% Gradiente en un punto específico
x0 = 1; y0 = 1;
grad_at_point = double(subs(grad_f, [x, y], [x0, y0]));
fprintf('∇f(1,1) = [%.3f; %.3f]\n', grad_at_point(1), grad_at_point(2));

% Derivada direccional en dirección u = [1/√2, 1/√2]
u = [1/sqrt(2); 1/sqrt(2)];
dir_deriv = dot(grad_at_point, u);
fprintf('Derivada direccional en (1,1) hacia [1/√2, 1/√2]: %.3f\n', dir_deriv);
```

## 🔬 Aplicaciones Específicas en Ingeniería Química

### Termodinámica
- **Relaciones de Maxwell**: $\left(\frac{\partial T}{\partial V}\right)_S = -\left(\frac{\partial P}{\partial S}\right)_V$
- **Ecuaciones de estado**: $PV = nRT + f(P,T,n)$
- **Potenciales termodinámicos**: Energía libre de Gibbs, Helmholtz

### Transferencia de Masa
- **Ley de Fick multidimensional**: $\vec{J} = -D\nabla C$
- **Difusión en múltiples direcciones**: Análisis de gradientes
- **Coeficientes de transferencia**: Dependencia de múltiples variables

### Transferencia de Calor
- **Conducción multidimensional**: $q = -k\nabla T$
- **Convección**: Coeficientes dependientes de múltiples variables
- **Radiación**: Factores de forma y configuración

### Cinética Química
- **Velocidades de reacción**: $r = f(C_1, C_2, ..., T, P)$
- **Análisis de sensibilidad**: $\frac{\partial r}{\partial T}, \frac{\partial r}{\partial C_i}$
- **Optimización de condiciones**: Múltiples variables de proceso

### Diseño de Reactores
- **Reactores multifásicos**: Variables espaciales múltiples
- **Distribución de temperatura**: Gradientes en múltiples direcciones
- **Optimización de geometría**: Múltiples parámetros de diseño

## 🌟 Casos de Estudio

### Caso 1: Optimización de Reactor Tubular
Optimizar temperatura y presión a lo largo de un reactor tubular para maximizar la selectividad del producto deseado.

### Caso 2: Diseño de Intercambiador de Calor
Determinar las dimensiones óptimas (longitud, diámetro, número de tubos) que minimizan el costo total.

### Caso 3: Control Multivariable de Columna de Destilación
Analizar la sensibilidad de la pureza del destilado respecto a la relación de reflujo y el flujo de vapor.

### Caso 4: Análisis de Propagación de Errores
Determinar cómo los errores en medición de temperatura y presión afectan el cálculo de densidad de un gas.

## 🎓 Competencias Desarrolladas

### Competencias Conceptuales
- Comprensión de funciones multivariables
- Dominio de derivadas parciales y direccionales
- Capacidad de visualización en múltiples dimensiones

### Competencias Procedimentales
- Habilidad para calcular gradientes y derivadas direccionales
- Destreza en optimización multivariable
- Competencia en análisis de sensibilidad

### Competencias Aplicadas
- Capacidad de modelado multivariable de procesos
- Habilidad para optimización de sistemas complejos
- Competencia en análisis de propagación de errores

---

*Tiempo total estimado: 45 horas de trabajo personal + 11 horas presenciales = 56 horas*

*Este tema proporciona las herramientas fundamentales del cálculo multivariable para el análisis y optimización de procesos químicos complejos.*