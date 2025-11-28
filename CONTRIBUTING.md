# Guía de Contribución - Material de Repaso USC

## 🎯 Bienvenido/a

¡Gracias por tu interés en contribuir al Material de Repaso para el Grado en Matemáticas de la USC! Este proyecto busca crear recursos de estudio de alta calidad para la comunidad académica.

---

## 📋 Tipos de Contribuciones

### 🔧 Correcciones y Mejoras
- **Errores matemáticos**: Corrección de fórmulas, demostraciones o cálculos
- **Errores tipográficos**: Ortografía, gramática, formato
- **Mejoras de claridad**: Explicaciones más claras o ejemplos adicionales
- **Optimización de estructura**: Reorganización de contenido para mejor comprensión

### ➕ Nuevo Contenido
- **Completar semanas faltantes**: Desarrollar contenido para las 27 semanas restantes
- **Ejercicios adicionales**: Añadir más problemas resueltos o para resolver
- **Recursos extras**: Notebooks, visualizaciones, aplicaciones prácticas
- **Traducciones**: Versiones en gallego o inglés

### 🛠️ Mejoras Técnicas
- **Herramientas computacionales**: Notebooks de Python/MATLAB/Mathematica
- **Visualizaciones**: Gráficos, diagramas, animaciones
- **Automatización**: Scripts para generar contenido o verificar formato
- **Documentación**: Mejoras en guías y documentación técnica

---

## 🚀 Cómo Contribuir

### 1. Preparación del Entorno

```bash
# Clonar el repositorio
git clone https://github.com/SaulALP/Material_Repaso_USC.git
cd Material_Repaso_USC

# Crear una nueva rama para tu contribución
git checkout -b feature/nombre-descriptivo
# Ejemplos:
# git checkout -b fix/error-semana-03
# git checkout -b content/semana-05-mate2
# git checkout -b enhancement/visualizaciones-3d
```

### 2. Estructura de Trabajo

#### Para Nuevo Contenido de Semanas:
```bash
# Usar las plantillas existentes
cp templates/README_semana.md Mate-X/Semana_XX_Titulo/README.md
cp templates/ejercicio_resuelto.md Mate-X/Semana_XX_Titulo/practice/ejercicios_resueltos.md
# ... etc
```

#### Para Correcciones:
- Identifica el archivo específico a corregir
- Realiza cambios mínimos y precisos
- Documenta la razón del cambio en el commit

### 3. Estándares de Calidad

#### Contenido Matemático:
- **Rigor**: Todas las afirmaciones deben ser matemáticamente correctas
- **Claridad**: Explicaciones accesibles para el nivel universitario
- **Completitud**: Demostraciones completas o referencias apropiadas
- **Notación**: Usar LaTeX para matemáticas: `$...$` inline, `$$...$$` display

#### Estructura de Archivos:
- **README.md**: Objetivos, prerrequisitos, tiempo estimado, estructura
- **theory/**: Contenido teórico con demostraciones
- **practice/**: Ejercicios graduados en dificultad
- **extras/**: Recursos adicionales opcionales

#### Formato y Estilo:
- **Markdown**: Seguir sintaxis estándar
- **Títulos**: Usar jerarquía clara (##, ###, ####)
- **Listas**: Usar viñetas consistentes
- **Código**: Usar bloques de código para algoritmos

### 4. Proceso de Revisión

```bash
# Verificar cambios
git status
git diff

# Añadir archivos modificados
git add .

# Commit descriptivo
git commit -m "tipo: descripción breve

Explicación más detallada si es necesario.
- Cambio específico 1
- Cambio específico 2

Fixes #issue-number (si aplica)"

# Ejemplos de commits:
# git commit -m "fix: corregir error en demostración del teorema fundamental"
# git commit -m "content: añadir Semana 05 de Mate-2 con ejercicios completos"
# git commit -m "docs: mejorar explicación de derivadas parciales"
```

---

## 📝 Estándares Específicos

### Ejercicios Resueltos

Cada ejercicio resuelto debe incluir:

```markdown
## Ejercicio Resuelto X: Título Descriptivo

### 📋 Enunciado
[Enunciado claro y completo]

### 🔍 Análisis Previo
**Conceptos involucrados**: [Lista de conceptos]
**Estrategia de resolución**: [Enfoque general]

### ✏️ Resolución Paso a Paso
[Desarrollo detallado con justificaciones]

### 🎯 Resultado Final
[Respuesta clara y verificación si es posible]

### 💡 Comentario Conceptual
[Explicación del significado y conexiones]
```

### Ejercicios para Resolver

```markdown
## Ejercicio X: Título

**Dificultad**: ⭐⭐⭐☆☆ (3/5)
**Tiempo estimado**: XX minutos
**Conceptos**: [Lista de conceptos principales]

### Enunciado
[Problema claro y completo]

### Ayuda
> **💡 Pista**: [Sugerencia útil sin dar la solución]
```

### Teoría

```markdown
# Título del Tema

## 1. Introducción
[Motivación y contexto]

## 2. Definiciones
[Definiciones precisas con notación LaTeX]

## 3. Teoremas Principales
[Enunciados y demostraciones]

## 4. Ejemplos
[Ejemplos ilustrativos]

## 5. Aplicaciones
[Conexiones con otros temas]
```

---

## 🔍 Lista de Verificación

Antes de enviar tu contribución, verifica:

### ✅ Contenido
- [ ] Matemáticas correctas y verificadas
- [ ] Explicaciones claras y completas
- [ ] Notación LaTeX apropiada
- [ ] Ejemplos relevantes incluidos
- [ ] Referencias a prerrequisitos cuando sea necesario

### ✅ Formato
- [ ] Markdown válido y bien estructurado
- [ ] Títulos jerárquicos apropiados
- [ ] Listas y tablas bien formateadas
- [ ] Enlaces internos funcionando
- [ ] Imágenes optimizadas (si las hay)

### ✅ Estructura
- [ ] Archivos en las carpetas correctas
- [ ] Nombres de archivo consistentes
- [ ] README.md actualizado si es necesario
- [ ] Plantillas seguidas apropiadamente

### ✅ Git
- [ ] Commits descriptivos y atómicos
- [ ] Rama con nombre apropiado
- [ ] Sin archivos innecesarios incluidos
- [ ] .gitignore respetado

---

## 🐛 Reportar Problemas

### Errores Matemáticos
```markdown
**Ubicación**: Mate-X/Semana_XX/archivo.md, línea XX
**Error encontrado**: [Descripción específica]
**Corrección sugerida**: [Si tienes una propuesta]
**Impacto**: [Crítico/Moderado/Menor]
```

### Problemas de Formato
```markdown
**Archivo**: [Ruta específica]
**Problema**: [Descripción del problema de formato]
**Navegador/Visor**: [Si es relevante]
```

### Sugerencias de Mejora
```markdown
**Área**: [Semana específica o tema general]
**Sugerencia**: [Descripción detallada]
**Justificación**: [Por qué sería una mejora]
**Prioridad**: [Alta/Media/Baja]
```

---

## 🎓 Reconocimientos

### Tipos de Contribución Reconocidas
- **Autores principales**: Creación de contenido completo de semanas
- **Revisores**: Corrección de errores y mejoras de calidad
- **Colaboradores técnicos**: Herramientas, visualizaciones, automatización
- **Traductores**: Versiones en otros idiomas

### Cómo se Reconoce
- Mención en archivos de créditos
- Atribución en commits y pull requests
- Reconocimiento en documentación del proyecto

---

## 📞 Contacto y Soporte

### Canales de Comunicación
- **Issues de GitHub**: Para reportar problemas o sugerir mejoras
- **Pull Requests**: Para contribuciones de código/contenido
- **Discussions**: Para preguntas generales o discusiones

### Tiempo de Respuesta Esperado
- **Errores críticos**: 24-48 horas
- **Mejoras y nuevas características**: 1-2 semanas
- **Preguntas generales**: 3-5 días

---

## 📚 Recursos Adicionales

### Herramientas Recomendadas
- **Editor Markdown**: Typora, Mark Text, o VS Code con extensiones
- **LaTeX**: Para verificar fórmulas matemáticas
- **Git GUI**: GitKraken, SourceTree, o GitHub Desktop
- **Visualización**: GeoGebra, Desmos, Python/Matplotlib

### Referencias Académicas
- Consultar siempre fuentes oficiales de la USC
- Verificar contenido con bibliografía reconocida
- Mantener coherencia con el plan de estudios oficial

---

## 🔄 Proceso de Revisión

### Revisión Automática
- Verificación de formato Markdown
- Validación de enlaces internos
- Comprobación de estructura de archivos

### Revisión Manual
- Corrección matemática del contenido
- Claridad y coherencia de explicaciones
- Adherencia a estándares de calidad

### Criterios de Aceptación
- **Corrección matemática**: Sin errores en contenido matemático
- **Calidad pedagógica**: Explicaciones claras y progresivas
- **Consistencia**: Adherencia a plantillas y estándares
- **Completitud**: Contenido completo según plantillas

---

**¡Gracias por contribuir a la educación matemática!** 🎓

Tu aporte ayuda a crear mejores recursos de aprendizaje para toda la comunidad académica.

---

**Última actualización**: 2024-11-28  
**Versión**: 1.0