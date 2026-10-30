# Plan de auditoría de accesos a datos de clientes

**Organización:** Alquimia Elixir Henao  
**Asignatura:** Auditoría de Sistemas (ET0114)  
**Estudiante:** Steven Henao García  
**Versión:** Propuesta para exposición del 30 de octubre de 2026  
**Riesgo de referencia:** Matriz de riesgos, Sesión 7, prioridad 1

> Este documento propone una auditoría. No es un informe de resultados ni afirma que los controles existan, funcionen o hayan sido probados.

## 1. Contexto y continuidad

Se conserva el caso de Alquimia Elixir Henao trabajado en las entregas anteriores: un emprendimiento colombiano de elaboración y comercialización de licores artesanales. Los trabajos del curso describen procesos que usan información de clientes, pedidos, ventas, inventario y producción. La matriz de la Sesión 7 enfoca este plan en la base de datos de clientes y en el acceso a esa información.

La propia matriz aclara que el equipo no tiene acceso directo a los sistemas reales y que algunas condiciones se plantearon como supuestos razonables. Por eso, las herramientas que usa hoy la empresa, sus permisos y sus políticas deben confirmarse antes de ejecutar pruebas. El marco principal para esta revisión será ISO/IEC 27001:2022, porque el tema es la gestión del riesgo de seguridad de la información. COBIT puede ayudar a organizar responsabilidades y seguimiento si resulta pertinente; ITIL no se desarrollará porque el alcance no es la gestión de servicios de TI.

## 2. Riesgo seleccionado y justificación

Se mantiene el riesgo de prioridad 1 de la matriz de la Sesión 7. Como la matriz no asignó un código al riesgo, se usa **R-01** en este plan como referencia de trazabilidad; no reemplaza ni altera la fila original.

| Elemento de la matriz | Riesgo seleccionado |
|---|---|
| Activo o proceso | Base de datos de clientes |
| Amenaza | Acceso no autorizado de personas externas o internas que no necesitan usar la información |
| Vulnerabilidad | Archivos con datos de clientes sin permisos definidos, sin revisión periódica de accesos y posiblemente sin autenticación multifactor |
| Consecuencia posible | Copia, modificación o divulgación de datos personales; pérdida de confianza y posibles reclamos |
| Valoración de la matriz | Probabilidad 4 × impacto 5 = nivel 20 |
| Control existente | La matriz indica que no se evidenció una matriz de permisos ni registros periódicos de revisión. Esto significa que no se presentó evidencia en el trabajo; no prueba por sí solo que el control no exista. |
| Tratamiento propuesto en la matriz | Permisos por rol, autenticación multifactor y revisión mensual documentada de usuarios con acceso |

La elección se justifica por el tipo de activo y por la consecuencia posible: el acceso indebido puede afectar la reserva y confiabilidad de la información de clientes y repercutir en pedidos y atención. Además, las medidas descritas en la matriz pueden examinarse con documentos, configuraciones y registros. El puntaje 20 orienta la prioridad, pero la razón de la auditoría es también la importancia del proceso y la posibilidad de contrastar controles con evidencia.

## 3. Objetivo de auditoría

**Determinar si, durante el periodo del 1 de julio al 30 de septiembre de 2026, el acceso a la información de clientes en los sistemas que la organización identifique estuvo limitado a usuarios autorizados y a permisos acordes con sus funciones, y si los controles definidos para autenticación, revisión y retiro de accesos operaron conforme a criterios internos vigentes o, cuando estos no existan, a criterios aprobados por la administración antes de las pruebas.**

El objetivo podrá responderse con evidencia de usuarios, permisos, autorizaciones, configuraciones y eventos de acceso. El periodo indicado es una propuesta de auditoría que comprende un trimestre completo; debe confirmarse según la disponibilidad de registros y la fecha real de ejecución.

## 4. Alcance funcional

| Delimitación | Propuesta |
|---|---|
| Proceso | Administración de usuarios y permisos para consultar, exportar, modificar o compartir información de clientes: solicitud, aprobación, alta, cambio, revisión y retiro de accesos. |
| Sistemas y componentes | Las aplicaciones, cuentas de almacenamiento, hojas de cálculo o repositorios que la empresa identifique como lugares donde guarda o trata datos de clientes. Se identificarán en el recorrido inicial; no se presupone una plataforma específica. |
| Población | Usuarios y cuentas con acceso a datos de clientes; altas, cambios y retiros de acceso; revisiones de permisos; y configuración de autenticación del periodo. El tamaño real se solicitará y no se inventará. |
| Periodo | 1 de julio a 30 de septiembre de 2026, sujeto a confirmar que existan registros completos. |
| Áreas o responsables | Administración o dueño del proceso, responsable de la información de clientes y persona que administre las aplicaciones o el almacenamiento. Los nombres se definirán con la organización. |
| Incluye | Permisos, necesidad de acceso, aprobación, cuentas compartidas o privilegiadas, autenticación multifactor cuando esté definida o sea compatible, revisiones periódicas y retiro de accesos. |
| Excluye | Pruebas de penetración, análisis de seguridad de toda la infraestructura, revisión integral de pagos, inventario o producción, y evaluación legal completa de privacidad. Estas exclusiones mantienen el plan acotado; no permiten concluir sobre la seguridad total de la empresa ni sobre todos sus deberes de protección de datos. |

Si el recorrido inicial encuentra datos de clientes en dispositivos personales, servicios externos o canales de mensajería, se registrará ese hecho y se acordará con la organización si es necesario ampliar el alcance. No se revisará contenido personal ajeno al objetivo.

## 5. Criterios de evaluación

Los criterios se aplicarán en este orden: requisitos legales que resulten aplicables, políticas y procedimientos vigentes de la organización y controles propuestos que la administración apruebe como condición para esta revisión. La política interna, las herramientas usadas y la aplicación jurídica deben confirmarse durante la preparación.

| Criterio | Condición que se contrastaría | Fuente y estado |
|---|---|---|
| C-01. Autorización y necesidad | Cada cuenta identificada debe corresponder a una persona autorizada y tener permisos justificados por su función; las altas o cambios deben contar con aprobación definida. | Política o procedimiento vigente de accesos, matriz de roles y aprobaciones. **Por solicitar y confirmar.** |
| C-02. Seguridad y confidencialidad de datos personales | Si se confirma que el tratamiento y la organización están sujetos a la Ley 1581 de 2012, se considerarán los principios de seguridad y confidencialidad del artículo 4, incluidos los riesgos de acceso no autorizado. | Ley 1581 de 2012, artículo 4, literales g y h. La aplicabilidad, el rol de la empresa y las obligaciones específicas deben confirmarse con la organización; este plan no determina cumplimiento legal. |
| C-03. Autenticación | Las cuentas deberán usar los mecanismos de autenticación definidos en la política vigente. La matriz propone evaluar autenticación multifactor; su obligatoriedad para este caso debe ser aprobada y validada según las plataformas. | Estándar de autenticación y configuración de las aplicaciones. **Por solicitar; MFA es una propuesta de control, no un hecho comprobado ni un plazo legal atribuido.** |
| C-04. Revisión y retiro | La organización debe revisar los permisos con la frecuencia definida y retirar o modificar accesos cuando cambie la necesidad o termine el vínculo, dentro del plazo aprobado. | Procedimiento interno vigente. La matriz propone revisión mensual; los tiempos de retiro están **por confirmar** y no se asignará un plazo inventado. |

ISO/IEC 27001:2022 se emplea como marco de referencia para orientar una gestión de seguridad basada en riesgos; no se tomará la frase «cumplir ISO» como criterio suficiente ni se afirmará que la empresa está certificada. El criterio operativo será una condición verificable, con fuente, alcance y vigencia confirmados. Si no existe política interna, la administración tendrá que aprobar la condición antes de medir la operación; si no se logra, el plan dejará esa limitación explícita.

## 6. Programa de trabajo propuesto

| Paso | Qué haría el auditor | Población o muestra | Evidencia que solicitaría y conservaría | Posible excepción |
|---|---|---|---|---|
| 1. Comprender el diseño | Reunirse con los responsables, recorrer el flujo de datos y documentar dónde se guarda la información, quién solicita, aprueba, concede, revisa y retira accesos. Confirmar criterios y vigencia de políticas. | Sistemas identificados por la empresa y responsables del proceso. | Política aprobada, flujo de altas/cambios/bajas, matriz de roles, lista de repositorios y acta breve del recorrido. | No hay responsable definido, política vigente o criterio autorizado para comparar. |
| 2. Evaluar permisos actuales | Obtener el listado completo de cuentas y permisos; reconciliarlo con la lista de personas autorizadas que proporcione el responsable; revisar necesidad de acceso, aprobación y privilegios. Priorizar el 100 % de las cuentas privilegiadas, externas o compartidas. Para el resto, definir una muestra basada en el tamaño de la población y el riesgo, una vez recibida la lista. | Todas las cuentas para comprobar integridad del listado; revisión detallada según muestreo documentado. Si la población es pequeña, se revisará completa. | Exportación de usuarios y roles, aprobaciones, evidencia de vínculo o función sin datos innecesarios y registro de la muestra. | Cuenta sin usuario identificable, permisos mayores a los aprobados, falta de aprobación o diferencias entre listados. |
| 3. Probar altas, cambios y retiros | Seleccionar eventos del periodo y rastrear cada uno desde la solicitud hasta la aprobación, configuración y evidencia del cambio. Para retiros, comparar los eventos de finalización o cambio de función con la fecha de desactivación y el plazo interno vigente. | Eventos de alta, cambio y retiro identificados en julio-septiembre. Incluir todos los casos de alto privilegio y una muestra de los restantes; el número se determina después de conocer la población. | Solicitudes, aprobaciones, registros de actividad, historial de cambios y listados de usuarios antes/después, con datos personales minimizados. | Acceso sin aprobación, retiro pendiente después del plazo definido o ausencia de registro para reconstruir la secuencia. |
| 4. Revisar autenticación y revisión periódica | Inspeccionar la configuración de autenticación y comprobar, si el criterio aprobado lo exige, qué cuentas tienen MFA activo. Examinar las revisiones de permisos del periodo y verificar quién las realizó, qué población cubrieron y cómo se cerraron las diferencias. | Configuración de cuentas en alcance; revisiones previstas para cada mes del periodo y acciones derivadas. | Capturas o exportaciones de configuración sin secretos, actas/listas de revisión y evidencia de corrección de excepciones. | MFA esperado pero desactivado, revisión omitida, población incompleta, revisión sin responsable o excepción sin seguimiento. |
| 5. Validar excepciones y cerrar | Confirmar con el responsable los hechos observados, solicitar evidencia adicional y separar error de registro, control ausente y falta de evidencia. Documentar desacuerdos y límites de acceso. | Todas las excepciones identificadas. | Cédula de prueba, referencia cruzada a evidencia y respuesta del responsable. | La respuesta no tiene soporte verificable, o la evidencia no permite llegar a una conclusión. |

Una entrevista sirve para conocer el proceso, pero no será la única evidencia de operación. Cada explicación se corroborará, cuando sea posible, con registros, configuración o aprobaciones. La evidencia de clientes se minimizará: se preferirán listados de cuentas y metadatos; si se necesita una muestra de registros, se anonimizará o enmascarará antes de compartirla.

## 7. Trazabilidad del riesgo

| Referencia | Control a evaluar | Criterio y fuente | Procedimiento | Población o muestra | Evidencia esperada |
|---|---|---|---|---|---|
| R-01 / Matriz Sesión 7, prioridad 1 | Permisos por rol y aprobación | C-01: política y matriz de roles vigentes, por solicitar | Reconciliar cuentas con usuarios autorizados y rastrear permisos a función y aprobación | Censo de cuentas para integridad; revisión de privilegiadas y muestra basada en población | Exportación de cuentas/roles, aprobaciones y listado autorizado |
| R-01 / Matriz Sesión 7, prioridad 1 | Autenticación multifactor | C-03: política/configuración vigente; obligación por confirmar | Inspeccionar ajustes de autenticación y comparar su estado con el criterio aprobado | Cuentas en alcance, priorizando privilegios y acceso externo | Configuración o reporte de autenticación sin credenciales |
| R-01 / Matriz Sesión 7, prioridad 1 | Revisión mensual de accesos y retiro oportuno | C-04: procedimiento vigente; frecuencia mensual propuesta en la matriz; plazo de retiro por confirmar | Revisar las verificaciones mensuales y rastrear cambios/bajas a los registros de acceso | Revisiones del trimestre y eventos de alta, cambio y retiro seleccionados por riesgo | Listas firmadas/aprobadas, solicitudes, logs e historial de cambios |

## 8. Ejecución, responsables y recursos

La duración propuesta es de **seis días hábiles**, contados desde la aprobación del acceso y la recepción de la información. Es una estimación para organizar el trabajo; puede cambiar según la disponibilidad de registros.

| Fase | Tiempo estimado | Actividades y responsables |
|---|---:|---|
| Preparación | Día 1 | Auditor: reunión de apertura, confirmación de alcance, sistemas, criterios, contactos y forma segura de compartir evidencia. Administración: designar responsables. |
| Solicitud y recorrido | Día 2 | Auditor: solicitar políticas y listados, recorrer el ciclo de vida de accesos. Responsable del proceso y administrador: explicar y entregar evidencia de solo lectura. |
| Pruebas | Días 3 y 4 | Auditor: reconciliar cuentas, seleccionar muestra y ejecutar pruebas de permisos, cambios, retiros, MFA y revisiones. Administrador: aclarar registros sin modificar configuraciones. |
| Validación | Día 5 | Auditor y responsables: confirmar hechos, completar evidencia y registrar limitaciones. |
| Cierre | Día 6 | Auditor: resumir alcance realizado, excepciones soportadas y limitaciones; presentar conclusiones solo si la auditoría se ejecuta. Administración: validar exactitud factual y definir responsables de respuesta. |

**Roles propuestos:** Steven Henao García prepara y explica el plan académico; durante una auditoría real, la persona auditora debe mantener independencia de quienes administran accesos. La administración de Alquimia debe designar un dueño del proceso, un custodio de los datos y un administrador de las plataformas. No se asignan nombres porque no aparecen en los trabajos previos.

**Recursos y dependencias:** acceso de solo lectura a exportaciones y configuraciones, políticas vigentes, listados de personas y eventos de alta/cambio/retiro, tiempo de los responsables y un canal seguro para entregar evidencia. Si no se conceden accesos o los registros no están disponibles, se documentará la limitación y se reducirá el alcance de la conclusión.

## 9. Supuestos, hechos por confirmar y límites

| Categoría | Declaración |
|---|---|
| Información documentada en trabajos anteriores | La organización del caso se identifica como Alquimia Elixir Henao; la matriz de la Sesión 7 registra como prioridad 1 el acceso no autorizado a datos de clientes, con P=4, I=5 y nivel 20. Estas son referencias del trabajo académico, no verificaciones independientes de la operación real. |
| Supuesto de la matriz | Pueden usarse correo, hojas de cálculo, mensajería, almacenamiento en nube y aplicaciones comunes; no se conoce el inventario real. Se debe validar en el recorrido inicial. |
| Propuesta del equipo | Revisar permisos por rol, autenticación multifactor y accesos mensualmente; usar julio-septiembre de 2026 como periodo; muestrear por riesgo después de conocer la población. |
| Información por solicitar | Política de accesos, matriz de roles, listado de sistemas y cuentas, registros de altas/cambios/retiros, evidencia de revisiones, configuración de autenticación y confirmación de aplicabilidad de la Ley 1581. |
| Limitación académica | No se cuenta con acceso a sistemas ni políticas reales. No se ejecutaron procedimientos y no hay evidencia obtenida. |

Por lo anterior, este documento no presenta hallazgos, porcentajes de cumplimiento ni una conclusión sobre la eficacia real de los controles. La exposición explica una propuesta de auditoría que deberá ajustarse si la empresa confirma una plataforma distinta, una población distinta, una política específica o si el docente recomienda cambios.

## 10. Fuentes

1. Steven Henao García, [Taller Sesión 7: Matriz inicial de riesgos de sistemas]  (https://github.com/stevenhenao534-byte/Auditor-a-de-Sistemas/blob/main/Taller-Sesion7-Matriz-Riesgos-Alquimia-Elixir-Henao.md), referencia de R-01.
2. Steven Henao García, [Taller Sesión 3: marcos de auditoría para Alquimia Elixir Henao](https://github.com/stevenhenao534-byte/Auditor-a-de-Sistemas/blob/main/Taller-Sesion3-Alquimia-Elixir-Henao.md), continuidad del caso y selección de marcos.
3. Juan Duque, [Taller: del riesgo priorizado al plan de auditoría](https://github.com/juanduque-ipb/et0114-auditoria-de-sistema/blob/main/taller/Taller-Plan-Auditoria-Segundo-Entregable.md), instrucciones del segundo entregable.
4. Colombia, [Ley 1581 de 2012, Gestor Normativo de Función Pública](https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=49981), artículo 4, literales g y h. Aplicación por confirmar para la organización y tratamiento concretos.
5. ISO, [ISO/IEC 27001:2022](https://www.iso.org/standard/27001), referencia sobre sistemas de gestión de seguridad de la información basada en riesgos. No implica certificación ni una evaluación de conformidad.


