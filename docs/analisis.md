# Análisis de la práctica

## 1. Preguntas de análisis

**1. ¿Por qué las metodologías tradicionales tienen dificultades en proyectos de innovación?**
Las metodologías tradicionales se fundamentan en un enfoque predictivo, asumiendo que los requisitos del usuario pueden conocerse en su totalidad y congelarse antes de empezar a construir. En los proyectos de innovación existe una alta incertidumbre tecnológica y comercial; el mercado cambia rápido y frecuentemente el cliente no sabe lo que quiere hasta que interactúa con el producto. Un proceso rígido y lineal dificulta y encarece la incorporación de cambios una vez superada la fase de diseño, asfixiando la experimentación, el ensayo-error y la adaptación, elementos cruciales para innovar con éxito.

**2. ¿Cuál de los 4 valores del Manifiesto consideras más difícil de aplicar y por qué?**
Generalmente, "Colaboración con el cliente sobre negociación contractual" resulta ser el más difícil de llevar a la práctica. En el mundo corporativo, las empresas (especialmente sus áreas legales y financieras) exigen contratos cerrados con alcances, presupuestos y fechas límite fijas para mitigar el riesgo monetario. Lograr que un cliente participe continuamente, confíe en el equipo sin exigir todo por escrito desde el inicio y acepte la variabilidad del alcance, implica un profundo cambio de cultura organizacional y de confianza que va mucho más allá de un tema puramente técnico.

**3. ¿Significa ser ágil que se prescinde totalmente de la documentación? Argumenta.**
No en absoluto. Ser ágil no es sinónimo de desorden o ausencia de documentación. El valor del Manifiesto Ágil dicta: "Software funcionando *sobre* documentación exhaustiva", lo que implica priorizar el producto tangible por encima de trámites burocráticos excesivos, pero no eliminar la documentación. El agilismo defiende crear documentación "ágil": debe ser concisa, directamente útil, actualizada y limitada a lo estrictamente necesario para el mantenimiento del sistema y la comunicación del equipo, evitando redactar documentos enormes que nadie leerá o que quedarán obsoletos rápidamente.

**4. ¿En qué escenario seguirías eligiendo una metodología tradicional?**
La metodología tradicional sigue siendo la elección correcta en escenarios de alta criticidad, donde el entorno es estable, los requerimientos son estáticos y conocidos, y la exposición al riesgo (de seguridad, legal o vital) es extrema. Ejemplos clásicos son el software médico para quirófanos, sistemas aeroespaciales o software bancario central. En estos proyectos, el costo humano o financiero de un fallo en producción es inaceptablemente alto, lo que justifica de sobra invertir tiempo extenso en planificación detallada, documentación rigurosa y pruebas formales antes de escribir código.

## 2. Actividad complementaria

# Marcos ágiles adicionales

### Kanban
- **Qué es:** Es un marco de trabajo ágil originado en los sistemas de fabricación lean de Toyota, enfocado en visualizar el trabajo y optimizar su paso a través del sistema.
- **Característica principal:** El uso de un tablero visual (físico o virtual) y la imposición de límites estrictos al Trabajo en Progreso (WIP - *Work In Progress*). Esto garantiza que el equipo no empiece nuevas tareas hasta haber terminado las actuales, evitando cuellos de botella.
- **En qué situaciones convendría utilizarlo:** Es altamente recomendado para equipos de soporte técnico, mantenimiento de software o equipos de operaciones donde el trabajo llega de forma impredecible y continua (como la resolución de tickets de soporte), haciendo poco práctico planificar iteraciones cerradas (sprints).

### XP (Extreme Programming)
- **Qué es:** Es un marco de trabajo ágil centrado casi exclusivamente en la ingeniería de software y la excelencia técnica para mejorar la calidad del producto y la capacidad de respuesta ante cambios.
- **Característica principal:** Sus prácticas técnicas obligatorias altamente disciplinadas, destacando la programación en parejas (dos personas en una pantalla), el desarrollo guiado por pruebas (TDD - escribir la prueba antes que el código), refactorización continua e integración continua.
- **En qué situaciones convendría utilizarlo:** Es ideal para proyectos de alto riesgo técnico o que enfrentan requerimientos que cambian radicalmente. Funciona mejor con equipos medianos conformados por desarrolladores senior altamente disciplinados que buscan maximizar la robustez del código.

### ScrumBan
- **Qué es:** Es una metodología híbrida que combina la estructura y roles definidos de Scrum con la flexibilidad continua y visualización orientada al flujo de Kanban.
- **Característica principal:** Utiliza los eventos de Scrum (como planificaciones, revisiones o retrospectivas) pero reemplaza las iteraciones estrictas (sprints de tiempo fijo) por el flujo continuo de trabajo y los límites WIP de Kanban, planificando solo cuando el tablero requiere nuevas tareas (planificación bajo demanda).
- **En qué situaciones convendría utilizarlo:** Es excelente para equipos de Scrum maduros que sufren interrupciones urgentes constantemente que rompen sus Sprints, o equipos que desean migrar progresivamente de la rigidez de Scrum hacia la fluidez de Kanban sin perder ceremonias importantes.

### Tabla comparativa

| Criterio | Kanban | XP (Extreme Programming) | ScrumBan |
| :--- | :--- | :--- | :--- |
| **Enfoque principal** | Flujo continuo de trabajo. | Excelencia en ingeniería técnica. | Combinación de roles y flujo continuo. |
| **Organización de tiempo**| Flujo continuo (sin iteraciones). | Iteraciones muy cortas (1-2 semanas). | Flujo continuo con ceremonias bajo demanda. |
| **Roles prescritos** | No impone roles obligatorios. | Cliente, Programadores, Tracker, Coach. | Flexible, usualmente mantiene los de Scrum. |
| **Práctica fundamental** | Límite del Trabajo en Progreso (WIP). | Pair Programming y Test-Driven Development (TDD). | Límite WIP con tablero y eventos de Scrum. |

## 3. Conclusión general

La comprensión de las diferencias entre metodologías tradicionales y ágiles revela una evolución necesaria en la ingeniería de software. Mientras que el paradigma tradicional aporta estructura y control absoluto —indispensable para sistemas críticos y estables— su rigidez lo vuelve vulnerable ante la incertidumbre comercial. El Manifiesto Ágil surge como respuesta, proponiendo un cambio de mentalidad donde el éxito no se mide por seguir un plan a la perfección, sino por entregar software funcional que responda a las necesidades reales y cambiantes del cliente. La exploración de marcos específicos como Kanban, XP y ScrumBan confirma que la agilidad no impone un modelo único universal, sino un conjunto de valores adaptables; las organizaciones pueden elegir o combinar prácticas orientadas al flujo, a la ingeniería técnica o a la gestión de iteraciones, logrando así optimizar su eficiencia operativa según las demandas específicas de cada proyecto.
