# 📐 Geometría Analítica en el Plano

## 🎯 Introducción y Motivación

La geometría analítica en el plano constituye una herramienta fundamental para el análisis y diseño de procesos químicos bidimensionales. En ingeniería química, muchos problemas se pueden simplificar a análisis en el plano, como:

- **Diagramas de fases binarios**: Representación de equilibrios líquido-vapor
- **Perfiles de concentración**: Análisis en reactores de lecho fijo
- **Optimización de procesos**: Representación gráfica de restricciones
- **Diseño de equipos**: Secciones transversales de intercambiadores de calor
- **Control de procesos**: Diagramas de estabilidad en el plano de fases

## 📊 Sistemas de Coordenadas en el Plano

### Sistema de Coordenadas Cartesianas

**Definición**: El sistema de coordenadas cartesianas en ℝ² está definido por dos ejes perpendiculares que se intersectan en el origen O(0,0).

Todo punto P en el plano se representa como:
$$P = (x, y)$$

donde:
- $x$: coordenada horizontal (abscisa)
- $y$: coordenada vertical (ordenada)

**Propiedades fundamentales**:
- **Distancia entre dos puntos**: $d(P_1, P_2) = \sqrt{(x_2-x_1)^2 + (y_2-y_1)^2}$
- **Punto medio**: $M = \left(\frac{x_1+x_2}{2}, \frac{y_1+y_2}{2}\right)$

### Sistema de Coordenadas Polares

**Definición**: Un punto P se representa mediante:
$$P = (r, \theta)$$

donde:
- $r \geq 0$: distancia desde el origen (radio)
- $\theta$: ángulo medido desde el eje x positivo (argumento)

**Transformaciones entre sistemas**:

**Cartesianas → Polares**:
$$r = \sqrt{x^2 + y^2}$$
$$\theta = \arctan\left(\frac{y}{x}\right) \quad \text{(con ajustes por cuadrante)}$$

**Polares → Cartesianas**:
$$x = r\cos(\theta)$$
$$y = r\sin(\theta)$$

### Aplicación en Ingeniería Química: Reactor Radial

En un reactor radial con flujo desde el centro hacia la periferia:
- **Coordenadas cartesianas**: Útiles para análisis de simetría
- **Coordenadas polares**: Naturales para el flujo radial

La concentración puede expresarse como $C(r, \theta)$ donde $r$ es la distancia radial.

## 📏 Vectores en el Plano

### Definición y Operaciones

**Vector en el plano**: $\vec{v} = (v_x, v_y) = v_x\vec{i} + v_y\vec{j}$

**Operaciones fundamentales**:
- **Suma**: $\vec{u} + \vec{v} = (u_x + v_x, u_y + v_y)$
- **Producto por escalar**: $\alpha\vec{v} = (\alpha v_x, \alpha v_y)$
- **Producto escalar**: $\vec{u} \cdot \vec{v} = u_x v_x + u_y v_y$
- **Módulo**: $|\vec{v}| = \sqrt{v_x^2 + v_y^2}$

### Ángulo entre Vectores

$$\cos(\theta) = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}||\vec{v}|}$$

**Casos especiales**:
- $\vec{u} \perp \vec{v} \Leftrightarrow \vec{u} \cdot \vec{v} = 0$
- $\vec{u} \parallel \vec{v} \Leftrightarrow \vec{u} \times \vec{v} = 0$

### Aplicación: Análisis de Flujos

En un intercambiador de calor de placas, los vectores velocidad de los fluidos caliente y frío forman ángulos específicos que determinan la eficiencia de transferencia de calor.

## 📐 Rectas en el Plano

### Formas de la Ecuación de una Recta

#### 1. Forma Punto-Pendiente
$$y - y_0 = m(x - x_0)$$

donde $(x_0, y_0)$ es un punto conocido y $m$ es la pendiente.

#### 2. Forma Pendiente-Ordenada
$$y = mx + b$$

donde $m$ es la pendiente y $b$ es la ordenada al origen.

#### 3. Forma General
$$Ax + By + C = 0$$

donde $A$, $B$, $C$ son constantes con $A^2 + B^2 \neq 0$.

#### 4. Forma Paramétrica
$$\begin{cases}
x = x_0 + at \\
y = y_0 + bt
\end{cases}$$

donde $(x_0, y_0)$ es un punto de la recta, $(a, b)$ es el vector director, y $t \in \mathbb{R}$ es el parámetro.

#### 5. Forma Vectorial
$$\vec{r}(t) = \vec{r_0} + t\vec{d}$$

donde $\vec{r_0} = (x_0, y_0)$ es el vector posición de un punto conocido y $\vec{d} = (a, b)$ es el vector director.

### Relaciones entre Rectas

#### Paralelismo
Dos rectas $L_1: y = m_1x + b_1$ y $L_2: y = m_2x + b_2$ son paralelas si y solo si:
$$m_1 = m_2 \quad \text{y} \quad b_1 \neq b_2$$

#### Perpendicularidad
Dos rectas son perpendiculares si y solo si:
$$m_1 \cdot m_2 = -1$$

#### Intersección
Para encontrar la intersección de dos rectas, resolvemos el sistema:
$$\begin{cases}
A_1x + B_1y + C_1 = 0 \\
A_2x + B_2y + C_2 = 0
\end{cases}$$

### Distancias

#### Distancia de un Punto a una Recta
La distancia del punto $P_0(x_0, y_0)$ a la recta $Ax + By + C = 0$ es:
$$d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$$

#### Distancia entre Rectas Paralelas
Para rectas paralelas $L_1: Ax + By + C_1 = 0$ y $L_2: Ax + By + C_2 = 0$:
$$d = \frac{|C_2 - C_1|}{\sqrt{A^2 + B^2}}$$

### Aplicación: Líneas de Operación en Destilación

En una columna de destilación, las líneas de operación se representan como rectas en el diagrama x-y:

**Línea de operación de enriquecimiento**:
$$y = \frac{R}{R+1}x + \frac{x_D}{R+1}$$

donde $R$ es la relación de reflujo y $x_D$ es la fracción molar del destilado.

## ⭕ Circunferencias

### Ecuación de la Circunferencia

#### Forma Estándar
Circunferencia con centro $(h, k)$ y radio $r$:
$$(x - h)^2 + (y - k)^2 = r^2$$

#### Forma General
$$x^2 + y^2 + Dx + Ey + F = 0$$

donde el centro es $\left(-\frac{D}{2}, -\frac{E}{2}\right)$ y el radio es $r = \frac{1}{2}\sqrt{D^2 + E^2 - 4F}$.

### Posiciones Relativas

#### Recta y Circunferencia
Para la recta $Ax + By + C = 0$ y la circunferencia $(x-h)^2 + (y-k)^2 = r^2$:

- **Secante**: $d < r$ (dos puntos de intersección)
- **Tangente**: $d = r$ (un punto de intersección)
- **Exterior**: $d > r$ (sin intersección)

donde $d$ es la distancia del centro a la recta.

#### Dos Circunferencias
Para circunferencias con centros $C_1$, $C_2$ y radios $r_1$, $r_2$:

- **Exteriores**: $d > r_1 + r_2$
- **Tangentes exteriores**: $d = r_1 + r_2$
- **Secantes**: $|r_1 - r_2| < d < r_1 + r_2$
- **Tangentes interiores**: $d = |r_1 - r_2|$
- **Una interior a la otra**: $d < |r_1 - r_2|$

### Aplicación: Diseño de Tanques Cilíndricos

En el diseño de tanques de almacenamiento, las secciones transversales circulares permiten:
- **Optimización del volumen**: Máximo volumen para perímetro dado
- **Análisis de esfuerzos**: Distribución uniforme de tensiones
- **Cálculo de niveles**: Relación entre altura y volumen

## 📈 Secciones Cónicas

### Definición General

Las secciones cónicas son curvas obtenidas por la intersección de un cono circular recto con un plano. Se clasifican en:

1. **Elipse** (incluyendo la circunferencia como caso especial)
2. **Parábola**
3. **Hipérbola**

### Elipse

#### Definición
Lugar geométrico de puntos cuya suma de distancias a dos puntos fijos (focos) es constante.

#### Ecuación Estándar
Con centro en el origen y focos en el eje x:
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$

donde:
- $a$: semieje mayor
- $b$: semieje menor
- $c$: distancia del centro a cada foco, con $c^2 = a^2 - b^2$

#### Propiedades
- **Excentricidad**: $e = \frac{c}{a}$ con $0 \leq e < 1$
- **Focos**: $(\pm c, 0)$
- **Vértices**: $(\pm a, 0)$ y $(0, \pm b)$

### Parábola

#### Definición
Lugar geométrico de puntos equidistantes de un punto fijo (foco) y una recta fija (directriz).

#### Ecuación Estándar
Con vértice en el origen y foco en $(p, 0)$:
$$y^2 = 4px$$

#### Propiedades
- **Foco**: $(p, 0)$
- **Directriz**: $x = -p$
- **Excentricidad**: $e = 1$

### Hipérbola

#### Definición
Lugar geométrico de puntos cuya diferencia de distancias a dos puntos fijos (focos) es constante.

#### Ecuación Estándar
Con centro en el origen y focos en el eje x:
$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$

#### Propiedades
- **Focos**: $(\pm c, 0)$ donde $c^2 = a^2 + b^2$
- **Vértices**: $(\pm a, 0)$
- **Asíntotas**: $y = \pm\frac{b}{a}x$
- **Excentricidad**: $e = \frac{c}{a}$ con $e > 1$

### Aplicaciones en Ingeniería Química

#### Elipses en Intercambiadores de Calor
Las secciones transversales elípticas en intercambiadores proporcionan:
- **Mejor distribución de flujo** comparado con secciones circulares
- **Reducción de caída de presión** en ciertas configuraciones

#### Parábolas en Concentradores Solares
Los reflectores parabólicos concentran la radiación solar en el foco:
- **Concentración máxima de energía**
- **Aplicación en calentamiento de fluidos de proceso**

#### Hipérbolas en Torres de Enfriamiento
El perfil hiperbólico optimiza:
- **Flujo de aire natural** por efecto chimenea
- **Resistencia estructural** a cargas de viento

## 🔄 Transformaciones en el Plano

### Traslaciones

Una traslación por el vector $\vec{v} = (h, k)$ transforma el punto $(x, y)$ en:
$$(x', y') = (x + h, y + k)$$

**Forma matricial**:
$$\begin{pmatrix} x' \\ y' \\ 1 \end{pmatrix} = \begin{pmatrix} 1 & 0 & h \\ 0 & 1 & k \\ 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ 1 \end{pmatrix}$$

### Rotaciones

Una rotación de ángulo $\theta$ alrededor del origen transforma:
$$\begin{pmatrix} x' \\ y' \end{pmatrix} = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}$$

### Reflexiones

#### Reflexión respecto al eje x
$$(x, y) \mapsto (x, -y)$$

#### Reflexión respecto al eje y
$$(x, y) \mapsto (-x, y)$$

#### Reflexión respecto a la recta $y = x$
$$(x, y) \mapsto (y, x)$$

### Escalamientos

Un escalamiento con factores $s_x$ y $s_y$:
$$\begin{pmatrix} x' \\ y' \end{pmatrix} = \begin{pmatrix} s_x & 0 \\ 0 & s_y \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}$$

### Aplicación: Optimización de Layout de Planta

En el diseño de plantas químicas, las transformaciones geométricas permiten:
- **Rotación de equipos** para optimizar conexiones
- **Traslación de unidades** para minimizar longitudes de tuberías
- **Escalamiento** para ajustar capacidades de producción

## 📊 Aplicaciones Integradas en Procesos Químicos

### Ejemplo 1: Diagrama de McCabe-Thiele

En destilación, el diagrama x-y utiliza:
- **Línea de 45°**: $y = x$ (equilibrio ideal)
- **Curva de equilibrio**: Relación no lineal entre fracciones vapor-líquido
- **Líneas de operación**: Rectas que representan balances de materia

### Ejemplo 2: Diagramas de Fases Binarios

Los diagramas P-T para sistemas binarios emplean:
- **Curvas de saturación**: Fronteras entre fases
- **Puntos críticos**: Intersecciones de curvas
- **Regiones de coexistencia**: Áreas entre curvas

### Ejemplo 3: Perfiles de Concentración en Reactores

En reactores tubulares:
- **Coordenada axial**: Posición a lo largo del reactor
- **Concentración**: Variable dependiente
- **Perfil exponencial**: $C(z) = C_0 e^{-kz/v}$ para reacciones de primer orden

## 🎯 Ejercicios de Aplicación

### Ejercicio 1: Intersección de Líneas de Operación
En una columna de destilación, determinar el punto de intersección entre las líneas de operación de enriquecimiento y agotamiento.

### Ejercicio 2: Optimización Geométrica de Tanques
Diseñar un tanque cilíndrico que minimice el área superficial para un volumen dado, considerando restricciones geométricas del sitio.

### Ejercicio 3: Trayectorias de Partículas en Ciclones
Analizar las trayectorias parabólicas de partículas en un separador ciclónico para optimizar la eficiencia de separación.

## 🔗 Conexiones con Temas Avanzados

### Hacia Cálculo Diferencial
- **Derivadas como pendientes** de rectas tangentes
- **Optimización geométrica** usando cálculo
- **Curvas paramétricas** y sus derivadas

### Hacia Geometría del Espacio
- **Extensión a tres dimensiones** de conceptos planos
- **Superficies de revolución** generadas por curvas planas
- **Proyecciones** de objetos 3D al plano

### Hacia Análisis Vectorial
- **Campos vectoriales** en el plano
- **Circulación e integración** a lo largo de curvas
- **Teorema de Green** en regiones planas

---

## 🏆 Resumen de Competencias

Al completar este tema, el estudiante habrá desarrollado:

### Competencias Conceptuales
- [x] Dominio de sistemas de coordenadas en el plano
- [x] Comprensión profunda de elementos geométricos fundamentales
- [x] Conocimiento de transformaciones geométricas

### Competencias Procedimentales
- [x] Habilidad para resolver problemas de intersecciones y distancias
- [x] Destreza en el manejo de ecuaciones de curvas
- [x] Competencia en transformaciones de coordenadas

### Competencias Aplicadas
- [x] Capacidad de modelado geométrico de procesos químicos
- [x] Habilidad para optimización geométrica de equipos
- [x] Competencia en análisis espacial de sistemas industriales

---

*Este desarrollo proporciona las herramientas geométricas fundamentales para el análisis bidimensional de procesos y equipos en ingeniería química.*