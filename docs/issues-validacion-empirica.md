# Issues identificados en la validación empírica de PADIS 2.0

Este documento recopila los issues surgidos durante las fases de validación con docentes y estudiantes, organizados por origen y clasificados según su estado. Su propósito es servir como referencia para el mantenimiento y evolución futura de la plataforma.

## Docentes FIS (Fase 3: Revalidación)

| #   | Issue                                                                                | Estado    |
| --- | ------------------------------------------------------------------------------------ | --------- |
| 1   | Update HTML guide to include `exclude_args` parameter description                    | Pendiente |
| 2   | Improve `form-control` and `form-label` check output to show missing `for` attribute | Pendiente |
| 3   | Show total exercise check count in summary, not just current section count           | Pendiente |
| 4   | Add flag to force display of all check groups regardless of completion               | Resuelto  |
| 5   | Fix guide layout to keep function name and description together                      | Pendiente |
| 6   | Add `count` example to specific HTML tag check in guide                              | Pendiente |
| 7   | Fix outdated command reference in guide (`checkpadis` instead of `padis check`)      | Resuelto  |

**Descripción general:** La revalidación con docentes confirmó la viabilidad del flujo de creación de checks, pero identificó la necesidad de actualizar la documentación para reflejar las capacidades incorporadas durante la evolución (como `exclude_args` y `count`), mejorar la claridad de los mensajes de salida en checks vinculados a formularios y ofrecer mayor flexibilidad en la visualización de resultados. El issue #4 (flag para forzar visualización completa) y el #7 (corrección de comando obsoleto en la guía) fueron resueltos durante el período de validación.

## Estudiantes FIS (Fase 3: Revalidación)

| #   | Issue                                                                           | Estado    |
| --- | ------------------------------------------------------------------------------- | --------- |
| 8   | Improve visual distinction between skipped and passed check states              | Pendiente |
| 9   | Review naming of "omitted" check state for clarity                              | Pendiente |
| 10  | Add completion message when all checks pass                                     | Pendiente |
| 11  | Investigate Codespace opening behavior closing repository tab                   | Pendiente |
| 12  | Investigate live preview not working in Codespace built-in browser              | Pendiente |
| 13  | Investigate page auto-refresh differences between local and cloud modes         | Pendiente |
| 14  | Add brief help command explaining check states and result meanings              | Pendiente |
| 15  | Explore git hook or alias to suggest running `padis check` before commit/push   | Pendiente |
| 16  | Handle case-insensitive comparison for issue titles                             | Pendiente |
| 17  | Explore AI-based feedback for more specific guidance without revealing solution | Pendiente |

**Descripción general:** La revalidación con estudiantes reafirmó el valor de PADIS como guía de progreso y verificación adicional. Los issues identificados se concentran en tres áreas. En presentación de resultados (#8, #9, #10), se observó que la codificación por color y la terminología del estado "omitida" generaban confusión, y se sugirió un mensaje explícito de finalización. En aspectos del entorno (#11, #12, #13), se registraron comportamientos de navegación, previsualización y refresco de página que afectan el flujo aunque no dependen directamente de PADIS. En experiencia de uso (#14, #15, #16, #17), se propuso incorporar una ayuda breve sobre los estados, recordatorios para ejecutar checks en momentos habituales del flujo, comparación insensible a mayúsculas en títulos de issues y la exploración de retroalimentación asistida por IA sin revelar la solución.

## Docentes DA1 (Fase 4: Extensión)

| #   | Issue                                                                              | Estado    |
| --- | ---------------------------------------------------------------------------------- | --------- |
| 18  | Add case-insensitive string comparison option for checks                           | Pendiente |
| 19  | Explore runtime reflection to verify class instantiation and method invocation     | Pendiente |
| 20  | Explore cross-layer interaction validation (controller → service → repository)     | Pendiente |
| 21  | Add clean code checks (function length, unnecessary comments, poor variable names) | Pendiente |
| 22  | Explore AI assistance for teachers building check files                            | Resuelto  |
| 23  | Generalize checks to detect patterns without depending on specific entity names    | Pendiente |

**Descripción general:** La validación con docentes de DA1 identificó requisitos específicos para la adopción de PADIS en esa asignatura. En verificaciones de comportamiento (#19, #20), se propuso comprobar en tiempo de ejecución la instanciación de clases, la invocación de métodos y la interacción entre capas, posiblemente mediante reflection de .NET. En calidad de código (#21), se sugirió ampliar los checks hacia criterios como tamaño de funciones, comentarios innecesarios y nombres poco claros. En flexibilidad (#18, #23), se destacó la conveniencia de comparaciones insensibles a mayúsculas y de generalizar checks para reconocer patrones de diseño sin depender de nombres específicos. El issue #22 (asistencia de IA para la construcción de archivos de checks) fue abordado en el Estudio 3 del capítulo de experimentos con IA, mediante el enfoque SDD.

## Resumen cuantitativo

| Origen          | Total  | Resueltos | Pendientes |
| --------------- | ------ | --------- | ---------- |
| Docentes FIS    | 7      | 2         | 5          |
| Estudiantes FIS | 10     | 0         | 10         |
| Docentes DA1    | 6      | 1         | 5          |
| **Total**       | **23** | **3**     | **20**     |
