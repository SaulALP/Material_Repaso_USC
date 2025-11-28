# 📊 Tema 5: Estadística Descriptiva

## 🎯 Información del Tema

**Duración**: 3 horas expositivas + 1 hora seminario  
**Peso en la asignatura**: ~11% del contenido total  
**Prerrequisitos**: Conocimientos básicos de cálculo  
**Conexiones**: Base para análisis de datos experimentales y control de calidad  

## 📚 Objetivos de Aprendizaje

Al finalizar este tema, el estudiante será capaz de:

1. **Organizar** y presentar datos experimentales de manera efectiva
2. **Calcular** medidas de tendencia central y dispersión
3. **Interpretar** distribuciones de datos en contextos de ingeniería
4. **Aplicar** técnicas estadísticas al control de calidad de procesos
5. **Analizar** la variabilidad en datos de proceso
6. **Tomar decisiones** basadas en análisis estadístico de datos

## 📖 Contenidos Teóricos

### 5.1 Organización y Presentación de Datos
- Tipos de variables: cualitativas y cuantitativas
- Tablas de frecuencias
- Representaciones gráficas: histogramas, diagramas de caja
- Distribuciones de frecuencia

### 5.2 Medidas de Tendencia Central
- Media aritmética, geométrica y armónica
- Mediana y moda
- Percentiles y cuartiles
- Aplicaciones en datos de proceso

### 5.3 Medidas de Dispersión
- Rango y rango intercuartílico
- Varianza y desviación estándar
- Coeficiente de variación
- Interpretación de la variabilidad

### 5.4 Análisis de Distribuciones
- Forma de las distribuciones: simetría y curtosis
- Distribución normal y sus propiedades
- Estandarización de variables
- Regla empírica (68-95-99.7)

### 5.5 Aplicaciones en Ingeniería Química
- Control estadístico de procesos (SPC)
- Análisis de datos experimentales
- Caracterización de materias primas
- Evaluación de la calidad del producto
- Análisis de incertidumbre en mediciones

## ⏰ Distribución Temporal

| Contenido | Tiempo Estimado | Tipo de Clase |
|-----------|-----------------|---------------|
| Organización y presentación de datos | 1h | Expositiva |
| Medidas de tendencia central | 0.5h | Expositiva |
| Medidas de dispersión | 0.5h | Expositiva |
| Análisis de distribuciones | 1h | Expositiva |
| Ejercicios y aplicaciones | 1h | Seminario |
| **TOTAL** | **4h** | **3h + 1h** |

## 📁 Recursos Disponibles

### 📖 Teoría
- **`theory/organizacion_datos.md`**: Presentación y visualización de datos
- **`theory/medidas_centrales.md`**: Tendencia central y posición
- **`theory/medidas_dispersion.md`**: Variabilidad y dispersión
- **`theory/distribuciones.md`**: Análisis de formas de distribución
- **`theory/aplicaciones_proceso.md`**: Control estadístico de procesos

### 🔢 Práctica
- **`practice/ejercicios_para_resolver.md`**: 10 ejercicios graduados
- **`practice/ejercicios_resueltos.md`**: 5 ejercicios completamente desarrollados
- **`practice/casos_control_calidad.md`**: Problemas de SPC
- **`practice/hoja_respuestas.md`**: Resultados para verificación

### 🎯 Material Complementario
- **`extras/software_estadistico.md`**: Uso de MATLAB y Excel
- **`extras/graficos_avanzados.md`**: Visualización de datos
- **`extras/casos_industriales.md`**: Ejemplos reales de la industria

## 📊 Criterios de Evaluación

### Conocimientos Básicos (40%)
- Cálculo de medidas descriptivas
- Interpretación de gráficos estadísticos
- Clasificación de variables

### Aplicación de Métodos (35%)
- Análisis de distribuciones de datos
- Construcción de gráficos apropiados
- Interpretación de medidas de dispersión

### Aplicaciones Prácticas (25%)
- Control estadístico de procesos
- Análisis de datos experimentales
- Evaluación de calidad de productos
- Toma de decisiones basada en datos

## 🔗 Conexiones con Otros Temas

### Tema 4 (Cálculo Integral)
- Distribuciones de probabilidad continuas
- Cálculo de percentiles mediante integración
- Valores esperados como integrales

### Tema 6 (Optimización)
- Optimización de parámetros estadísticos
- Minimización de varianza
- Diseño experimental óptimo

### Matemáticas II
- Estadística inferencial
- Pruebas de hipótesis
- Análisis de regresión

### Asignaturas de Ingeniería
- **Experimentación**: Diseño y análisis de experimentos
- **Control de Procesos**: Cartas de control estadístico
- **Calidad**: Sistemas de gestión de calidad

## 📚 Bibliografía Específica

### Principal
- **Douglas C. Montgomery, George C. Runger** - "Probabilidad y estadística aplicadas a la ingeniería" (2ª ed.), Cap. 1-3
- **Jay L. Devore** - "Probabilidad y estadística para ingeniería y ciencias" (8ª ed.), Cap. 1-4

### Complementaria
- **Richard A. Johnson, Dean W. Wichern** - "Applied Multivariate Statistical Analysis" (6ª ed.), Cap. 1-2
- **Douglas C. Montgomery** - "Introduction to Statistical Quality Control" (7ª ed.), Cap. 1-4
- **Sheldon M. Ross** - "Introduction to Probability and Statistics for Engineers and Scientists" (5ª ed.), Cap. 1-3

## 🛠️ Herramientas Computacionales

### MATLAB
```matlab
% Ejemplo: Análisis estadístico de datos de proceso
% Datos de concentración de producto (mg/L)
datos = [98.2, 99.1, 97.8, 100.3, 98.9, 99.7, 98.5, 99.2, 98.8, 99.5, ...
         97.9, 100.1, 98.7, 99.3, 98.4, 99.8, 98.6, 99.0, 98.3, 99.4];

% Medidas de tendencia central
media = mean(datos);
mediana = median(datos);
moda = mode(datos);

% Medidas de dispersión
desv_std = std(datos);
varianza = var(datos);
rango = range(datos);
coef_var = (desv_std/media) * 100;

% Visualización
figure;
subplot(2,2,1);
histogram(datos, 'Normalization', 'probability');
title('Histograma de Concentraciones');
xlabel('Concentración (mg/L)');
ylabel('Probabilidad');

subplot(2,2,2);
boxplot(datos);
title('Diagrama de Caja');
ylabel('Concentración (mg/L)');

subplot(2,2,3);
qqplot(datos);
title('Q-Q Plot (Normalidad)');

subplot(2,2,4);
plot(datos, 'o-');
title('Serie Temporal');
xlabel('Muestra');
ylabel('Concentración (mg/L)');

% Resultados
fprintf('Análisis Estadístico Descriptivo\n');
fprintf('================================\n');
fprintf('Media: %.2f mg/L\n', media);
fprintf('Mediana: %.2f mg/L\n', mediana);
fprintf('Desviación Estándar: %.2f mg/L\n', desv_std);
fprintf('Coeficiente de Variación: %.2f%%\n', coef_var);
```

### Aplicaciones Recomendadas
- **MATLAB**: Análisis estadístico y visualización
- **Excel**: Análisis básico y gráficos
- **R**: Análisis estadístico avanzado
- **Minitab**: Control estadístico de procesos

## ⚠️ Puntos Críticos

### Conceptos Difíciles
1. **Interpretación de medidas**: Significado práctico de estadísticos
2. **Elección de gráficos**: Tipo apropiado según los datos
3. **Variabilidad**: Distinción entre diferentes fuentes de variación
4. **Distribución normal**: Propiedades y aplicaciones

### Errores Comunes
- Confundir media con mediana
- Interpretación incorrecta de la desviación estándar
- Uso inapropiado de gráficos
- No considerar el contexto de los datos

## 🎯 Estrategias de Estudio

### Recomendaciones
1. **Práctica con datos reales**: Usar datos de procesos químicos
2. **Visualización**: Crear múltiples tipos de gráficos
3. **Interpretación**: Conectar estadísticos con significado físico
4. **Software**: Dominar herramientas computacionales

### Tiempo de Estudio Estimado
- **Estudio teórico**: 5 horas
- **Resolución de ejercicios**: 8 horas
- **Práctica con software**: 4 horas
- **Casos industriales**: 2 horas
- **Repaso y síntesis**: 1 hora
- **TOTAL**: 20 horas de trabajo personal

## 🔬 Aplicaciones Específicas en Ingeniería Química

### Control de Calidad de Productos
- **Especificaciones**: Análisis de cumplimiento de estándares
- **Variabilidad del proceso**: Evaluación de consistencia
- **Cartas de control**: Monitoreo estadístico continuo

### Análisis de Materias Primas
- **Caracterización**: Propiedades físicas y químicas
- **Variabilidad de proveedores**: Comparación estadística
- **Criterios de aceptación**: Establecimiento de límites

### Optimización de Procesos
- **Análisis de sensibilidad**: Identificación de variables críticas
- **Reducción de variabilidad**: Mejora de la consistencia
- **Benchmarking**: Comparación de desempeño

### Análisis de Datos Experimentales
- **Diseño de experimentos**: Planificación estadística
- **Análisis de resultados**: Interpretación de datos
- **Validación de modelos**: Evaluación estadística

### Mantenimiento Predictivo
- **Análisis de tendencias**: Detección de patrones
- **Límites de alarma**: Establecimiento estadístico
- **Confiabilidad**: Análisis de tiempos de falla

## 📋 Lista de Verificación

Antes de continuar al siguiente tema, asegúrate de poder:

- [ ] Calcular medidas de tendencia central y dispersión
- [ ] Construir e interpretar histogramas y diagramas de caja
- [ ] Analizar la forma de distribuciones de datos
- [ ] Aplicar la regla empírica para distribuciones normales
- [ ] Interpretar coeficientes de variación
- [ ] Usar software estadístico básico
- [ ] Aplicar conceptos a control de calidad de procesos

## 🌟 Casos de Estudio

### Caso 1: Control de Calidad en Producción de Polímeros
Analizar la variabilidad en el peso molecular promedio de un polímero y establecer límites de control.

### Caso 2: Caracterización de Catalizador
Evaluar la distribución de tamaño de partícula de un catalizador y su impacto en la actividad.

### Caso 3: Análisis de Pureza de Producto Farmacéutico
Determinar si la pureza del producto cumple con especificaciones regulatorias.

### Caso 4: Optimización de Condiciones de Reacción
Analizar la variabilidad en conversión bajo diferentes condiciones operativas.

## 🎓 Competencias Desarrolladas

### Competencias Conceptuales
- Comprensión de conceptos estadísticos fundamentales
- Capacidad de interpretación de datos
- Conocimiento de distribuciones estadísticas

### Competencias Procedimentales
- Habilidad para calcular estadísticos descriptivos
- Destreza en construcción de gráficos
- Competencia en análisis de variabilidad

### Competencias Aplicadas
- Capacidad de control estadístico de procesos
- Habilidad para análisis de calidad
- Competencia en toma de decisiones basada en datos

## 🔄 Integración con Industria 4.0

### Big Data en Procesos Químicos
- **Análisis de grandes volúmenes**: Técnicas estadísticas escalables
- **Minería de datos**: Extracción de patrones
- **Análisis en tiempo real**: Estadísticas dinámicas

### Machine Learning
- **Análisis exploratorio**: Base para algoritmos de ML
- **Preprocesamiento**: Normalización y estandarización
- **Validación**: Métricas estadísticas de desempeño

### IoT y Sensores
- **Análisis de señales**: Caracterización estadística
- **Detección de anomalías**: Métodos estadísticos
- **Fusión de datos**: Combinación estadística de fuentes

---

*Tiempo total estimado: 20 horas de trabajo personal + 4 horas presenciales = 24 horas*

*Este tema proporciona las herramientas estadísticas fundamentales para el análisis de datos experimentales y el control de calidad en procesos químicos.*