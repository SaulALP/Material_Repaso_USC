# 📐 Tema 2: Geometría Analítica

## 🎯 Información del Tema

**Duración**: 4 horas expositivas + 1 hora seminario  
**Peso en la asignatura**: ~14% del contenido total  
**Prerrequisitos**: Tema 1 (Álgebra Lineal)  
**Conexiones**: Base para cálculo diferencial y optimización  

## 📚 Objetivos de Aprendizaje

Al finalizar este tema, el estudiante será capaz de:

1. **Dominar** la geometría analítica en el plano y el espacio
2. **Representar** matemáticamente elementos geométricos en procesos químicos
3. **Resolver** problemas de intersecciones y distancias en sistemas industriales
4. **Aplicar** conceptos geométricos al diseño de equipos y análisis espacial
5. **Visualizar** y modelar geometrías complejas en ingeniería química

## 📖 Contenidos Teóricos

### 2.1 Geometría en el Plano (ℝ²)
- Sistemas de coordenadas cartesianas y polares
- Ecuaciones de rectas: punto-pendiente, general, paramétrica
- Distancias y ángulos entre rectas
- Circunferencias y cónicas

### 2.2 Geometría en el Espacio (ℝ³)
- Sistemas de coordenadas: cartesianas, cilíndricas, esféricas
- Ecuaciones de rectas y planos en el espacio
- Intersecciones entre elementos geométricos
- Superficies cuadráticas

### 2.3 Transformaciones Geométricas
- Traslaciones, rotaciones y reflexiones
- Matrices de transformación
- Cambios de coordenadas

### 2.4 Aplicaciones en Ingeniería Química
- Geometría de reactores y equipos
- Análisis espacial de procesos
- Optimización geométrica de diseños
- Modelado de flujos en geometrías complejas

## ⏰ Distribución Temporal

| Contenido | Tiempo Estimado | Tipo de Clase |
|-----------|-----------------|---------------|
| Geometría en el plano | 1.5h | Expositiva |
| Geometría en el espacio | 2h | Expositiva |
| Transformaciones geométricas | 0.5h | Expositiva |
| Aplicaciones y ejercicios | 1h | Seminario |
| **TOTAL** | **5h** | **4h + 1h** |

## 📁 Recursos Disponibles

### 📖 Teoría
- **`theory/geometria_plano.md`**: Geometría analítica en ℝ²
- **`theory/geometria_espacio.md`**: Geometría analítica en ℝ³
- **`theory/transformaciones.md`**: Transformaciones geométricas
- **`theory/aplicaciones_ingenieria.md`**: Casos prácticos en procesos químicos

### 🔢 Práctica
- **`practice/ejercicios_para_resolver.md`**: 8 ejercicios graduados en dificultad
- **`practice/ejercicios_resueltos.md`**: 4 ejercicios completamente desarrollados
- **`practice/hoja_respuestas.md`**: Resultados para verificación

### 🎯 Material Complementario
- **`extras/visualizacion_3d.md`**: Herramientas de visualización
- **`extras/software_cad.md`**: Integración con software CAD
- **`extras/casos_industriales.md`**: Ejemplos de la industria química

## 📊 Criterios de Evaluación

### Conocimientos Básicos (35%)
- Ecuaciones de rectas y planos
- Sistemas de coordenadas
- Cálculo de distancias y ángulos

### Aplicación de Métodos (40%)
- Resolución de problemas de intersecciones
- Transformaciones geométricas
- Análisis de superficies

### Aplicaciones Prácticas (25%)
- Problemas de diseño de equipos
- Análisis geométrico de procesos
- Optimización espacial

## 🔗 Conexiones con Otros Temas

### Tema 1 (Álgebra Lineal)
- Vectores y espacios vectoriales
- Sistemas de ecuaciones lineales
- Transformaciones lineales

### Tema 3 (Cálculo Diferencial)
- Derivadas direccionales
- Gradientes y planos tangentes
- Optimización con restricciones geométricas

### Tema 6 (Optimización)
- Programación lineal geométrica
- Restricciones espaciales
- Optimización de formas

### Matemáticas II
- Geometría diferencial
- Superficies parametrizadas
- Campos vectoriales

## 📚 Bibliografía Específica

### Principal
- **Eric Steiner** - "Matemáticas para las ciencias aplicadas", Cap. 2-3
- **Ron Larson, Robert P. Hostetler, Bruce H. Edwards** - "Cálculo", Cap. 10-11

### Complementaria
- **Dennis G. Zill** - "Cálculo con geometría analítica" (2ª ed.), Cap. 1-3
- **Earl W. Swokowski** - "Geometría analítica con introducción al cálculo", Cap. 1-8
- **Michael Sullivan** - "Precálculo" (4ª ed.), Cap. 2-10

## 🛠️ Herramientas Computacionales

### MATLAB
```matlab
% Ejemplo: Visualización de superficies
[X, Y] = meshgrid(-5:0.1:5, -5:0.1:5);
Z = X.^2 + Y.^2;  % Paraboloide
surf(X, Y, Z);
xlabel('x'); ylabel('y'); zlabel('z');
title('Superficie cuadrática');
```

### Aplicaciones Recomendadas
- **MATLAB**: Visualización 3D y cálculos geométricos
- **GeoGebra**: Geometría interactiva
- **AutoCAD**: Diseño técnico
- **SolidWorks**: Modelado 3D para ingeniería

## ⚠️ Puntos Críticos

### Conceptos Difíciles
1. **Cambios de coordenadas**: Requiere práctica con transformaciones
2. **Geometría 3D**: Visualización espacial puede ser desafiante
3. **Intersecciones complejas**: Métodos sistemáticos son esenciales

### Errores Comunes
- Confundir ecuaciones paramétricas con implícitas
- Errores en cambios de coordenadas
- Interpretación incorrecta de resultados geométricos

## 🎯 Estrategias de Estudio

### Recomendaciones
1. **Visualización**: Usar software para representar geometrías
2. **Práctica sistemática**: Resolver problemas de complejidad creciente
3. **Conexión con aplicaciones**: Relacionar con problemas de ingeniería
4. **Verificación gráfica**: Comprobar resultados analíticos visualmente

### Tiempo de Estudio Estimado
- **Estudio teórico**: 6 horas
- **Resolución de ejercicios**: 8 horas
- **Práctica con software**: 3 horas
- **Aplicaciones industriales**: 2 horas
- **Repaso y síntesis**: 2 horas
- **TOTAL**: 21 horas de trabajo personal

## 🔬 Aplicaciones Específicas en Ingeniería Química

### Diseño de Reactores
- **Geometría de reactores tubulares**: Análisis de trayectorias de flujo
- **Reactores de lecho fijo**: Optimización de geometría para transferencia de masa
- **Mezcladores**: Diseño de geometrías para mezcla eficiente

### Equipos de Separación
- **Torres de destilación**: Análisis geométrico de platos y empaques
- **Intercambiadores de calor**: Optimización de configuraciones geométricas
- **Ciclones**: Diseño de trayectorias para separación eficiente

### Análisis de Procesos
- **Diagramas de flujo**: Representación espacial de procesos
- **Análisis de redes**: Geometría de sistemas de tuberías
- **Optimización espacial**: Distribución óptima de equipos en plantas

### Fenómenos de Transporte
- **Perfiles de velocidad**: Geometría de flujos en conductos
- **Transferencia de calor**: Análisis geométrico de superficies
- **Difusión**: Geometrías complejas en procesos de separación

## 📋 Lista de Verificación

Antes de continuar al siguiente tema, asegúrate de poder:

- [ ] Escribir ecuaciones de rectas y planos en diferentes formas
- [ ] Calcular distancias y ángulos entre elementos geométricos
- [ ] Realizar cambios entre sistemas de coordenadas
- [ ] Resolver problemas de intersecciones en 3D
- [ ] Aplicar transformaciones geométricas
- [ ] Interpretar resultados en contexto de ingeniería química
- [ ] Usar software para visualización geométrica

## 🌟 Casos de Estudio

### Caso 1: Diseño de Reactor Tubular
Optimización de la geometría de un reactor tubular para maximizar la conversión considerando restricciones de caída de presión y transferencia de calor.

### Caso 2: Intercambiador de Calor de Carcasa y Tubos
Análisis geométrico para determinar la configuración óptima de tubos que maximice el área de transferencia de calor.

### Caso 3: Sistema de Separación Ciclónica
Diseño de la geometría interna de un ciclón para optimizar la eficiencia de separación de partículas.

---

*Tiempo total estimado: 21 horas de trabajo personal + 5 horas presenciales = 26 horas*

*Este tema proporciona las herramientas geométricas fundamentales para el análisis y diseño de equipos y procesos en ingeniería química.*