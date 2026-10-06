# Taller: Elige el marco correcto para tu auditoría

**Auditoría de Sistemas (ET0114) · Sesión 3 · Normas y estándares internacionales**  
**Docente:** Juan Duque  
**Fecha de entrega:** miércoles 16 de septiembre de 2026

## Datos del integrante

**Nombre completo:** Steven Henao García

## 1. Organización o sistema elegido

**Alquimia Elixir Henao** — emprendimiento real colombiano dedicado a la elaboración y comercialización de licores artesanales.

## 2. Contexto

Alquimia Elixir Henao es un emprendimiento de licores artesanales que requiere controlar información relacionada con insumos, producción, lotes, inventario, ventas, clientes y pedidos. Actualmente, parte de estos procesos puede gestionarse de forma manual, lo que genera riesgos de pérdida o inconsistencia de información, errores en inventarios y ventas, dificultades para controlar la producción y problemas para mantener la trazabilidad de los lotes. También es necesario proteger la información de clientes y del negocio, controlar los accesos y asegurar la disponibilidad de la información para la operación.

## 3. Marcos de auditoría elegidos y orden de aplicación

Para este caso se propone aplicar los marcos en el siguiente orden:

1. **ISO/IEC 27001 — primero**
2. **COBIT — segundo**
3. **ITIL — tercero, como referencia complementaria y no como prioridad inicial**

### 3.1. Primer marco: ISO/IEC 27001

ISO/IEC 27001 se prioriza porque el primer riesgo que debe atenderse es la protección de la información que soporta el negocio. Alquimia Elixir Henao maneja datos de clientes, pedidos, ventas, inventarios, producción y trazabilidad de lotes. La pérdida, modificación no autorizada o indisponibilidad de esta información podría afectar directamente la operación.

Aplicar primero este marco permite revisar la forma en que se identifican y tratan los riesgos de seguridad de la información, así como los controles relacionados con acceso, protección, respaldo y disponibilidad. Es más pertinente como punto de partida que ITIL porque el problema principal del caso no es la gestión de una mesa de servicios de TI, sino la protección y control de la información del negocio.

**Evidencia que se solicitaría al equipo de TI:**

- **Matriz o registro de riesgos de seguridad de la información:** permitiría comprobar si están identificados riesgos como pérdida de información, accesos no autorizados, modificación de datos de inventario o ventas y falta de disponibilidad.
- **Políticas y registros de control de acceso y copias de seguridad:** permitirían verificar quién puede acceder a la información, qué permisos tiene cada usuario y si existen respaldos que permitan recuperar los datos ante pérdida o incidente.

### 3.2. Segundo marco: COBIT

Después de revisar la seguridad de la información, se aplicaría COBIT para evaluar la gobernanza y gestión de las tecnologías de información que apoyan los procesos del negocio. En este caso, no basta con proteger los datos: también es necesario determinar si los procesos tecnológicos tienen responsables definidos, controles adecuados y una relación clara con las necesidades de Alquimia Elixir Henao.

COBIT resulta apropiado en segundo lugar porque permite revisar la gestión, los controles, las responsabilidades y la alineación entre TI y los objetivos del negocio. Esto es especialmente importante para procesos como inventario, producción, ventas, clientes, pedidos y reportes.

**Evidencia que se solicitaría al equipo de TI:**

- **Matriz de responsabilidades y controles de los sistemas:** permitiría comprobar quién administra cada proceso o sistema, quién puede modificar información y qué controles existen para evitar errores o cambios no autorizados.
- **Registros o reportes de seguimiento de los procesos tecnológicos:** permitirían verificar si existen controles sobre inventarios, ventas, producción, trazabilidad y disponibilidad de la información, y si se realiza seguimiento a los resultados.

### 3.3. Tercer marco: ITIL

ITIL se utilizaría como referencia complementaria y en una tercera etapa. Su aplicación tendría sentido para revisar la gestión de los servicios tecnológicos que soportan la operación, especialmente si el emprendimiento implementa una solución informática que requiera soporte, mantenimiento, atención de incidentes y control de disponibilidad.

No se considera el primer marco porque la necesidad principal identificada en el caso está relacionada con la seguridad y gobernanza de la información, no con la administración formal de servicios de TI. Por eso, ITIL complementa los dos marcos anteriores en lugar de reemplazarlos.

**Evidencia que se solicitaría al equipo de TI:**

- **Registro de incidentes y solicitudes de soporte:** permitiría revisar problemas ocurridos en los sistemas, tiempos de atención, responsables y acciones realizadas para solucionarlos.
- **Registros o procedimientos de mantenimiento y disponibilidad:** permitirían verificar cómo se realizan las actividades de mantenimiento, cómo se controlan las interrupciones del servicio y qué medidas existen para mantener disponibles los sistemas utilizados por el negocio.

## 4. Justificación de la secuencia

La secuencia **ISO/IEC 27001 → COBIT → ITIL** responde a las necesidades específicas de Alquimia Elixir Henao.

Primero, **ISO/IEC 27001** permite concentrarse en el riesgo más inmediato: proteger la información que sostiene inventarios, producción, ventas, clientes, pedidos y trazabilidad. Antes de evaluar ampliamente la gestión tecnológica, es necesario conocer y controlar los riesgos que pueden comprometer la confidencialidad, integridad y disponibilidad de la información.

Segundo, **COBIT** permite revisar si la tecnología y sus controles están correctamente gobernados y alineados con los objetivos del negocio. Una vez identificados los aspectos de seguridad, se puede evaluar con mayor claridad la asignación de responsabilidades, los procesos de control y la gestión de TI.

Finalmente, **ITIL** permite complementar la auditoría desde la perspectiva de los servicios tecnológicos. Si el sistema de información se convierte en un componente permanente de la operación, será necesario controlar incidentes, solicitudes, mantenimiento y disponibilidad.

Por tanto, la selección no responde a una fórmula general, sino a la situación concreta del emprendimiento: **primero proteger la información, después fortalecer la gobernanza y los controles de TI y finalmente mejorar la gestión de los servicios tecnológicos.**

## 5. Conclusión

Para la auditoría de Alquimia Elixir Henao se considera más adecuado comenzar con ISO/IEC 27001, continuar con COBIT y utilizar ITIL como referencia complementaria. Esta combinación permite abordar los principales riesgos identificados: pérdida o acceso no autorizado a la información, errores en inventarios y ventas, falta de control sobre procesos tecnológicos, problemas de trazabilidad y posibles interrupciones de los servicios. Las evidencias propuestas permitirían sustentar la auditoría con documentos y registros concretos en lugar de limitarla a una revisión teórica de los marcos.
