# Taller Sesion 7: Matriz inicial de riesgos de sistemas

**Auditoria de Sistemas (ET0114) - Sesion 7 - Matriz de analisis de riesgos**  
**Docente:** Juan Duque  
**Estudiante:** Steven Henao Garcia  
**Organizacion:** Alquimia Elixir Henao  
**Fecha de entrega:** viernes 9 de octubre de 2026

## 1. Contexto actualizado del caso

Alquimia Elixir Henao es un emprendimiento dedicado a la venta y gestion de productos tipo elixir, con apoyo de herramientas digitales para registrar clientes, pedidos, inventario y pagos.  
En esta entrega se analizara el proceso de gestion de pedidos e informacion de clientes, desde la recepcion del pedido hasta el registro de venta y seguimiento.  
La preocupacion principal es proteger la informacion de clientes, evitar errores en pedidos e inventario y asegurar continuidad del servicio.  
Se mantiene la continuidad del Taller Sesion 3, donde se propuso aplicar ISO/IEC 27001, COBIT e ITIL como marcos de referencia.

## 2. Supuestos declarados

- No se cuenta con acceso directo a sistemas reales de la organizacion; por eso la matriz se construye con supuestos razonables para una pequena empresa o emprendimiento.
- Se asume que la organizacion usa herramientas comunes como correo electronico, hojas de calculo, mensajeria instantanea, almacenamiento en la nube y aplicaciones bancarias o pasarelas de pago.
- Se asume que no existe todavia un sistema formal de gestion de seguridad de la informacion ni politicas documentadas completas.
- Los controles propuestos son verificables mediante evidencias como capturas de configuracion, reportes de acceso, actas de revision, respaldos, registros de cambios y politicas aprobadas.

## 3. Activos y procesos concretos identificados

| No. | Activo o proceso | Descripcion |
|---:|---|---|
| 1 | Base de datos de clientes | Informacion de contacto, historial de compras, direcciones y datos necesarios para atender pedidos. |
| 2 | Proceso de gestion de pedidos | Registro, confirmacion, preparacion, despacho y seguimiento de pedidos. |
| 3 | Inventario de productos | Control de existencias, entradas, salidas y disponibilidad para la venta. |
| 4 | Cuentas de correo y mensajeria | Canales usados para comunicarse con clientes, proveedores y equipo interno. |
| 5 | Almacenamiento en la nube | Repositorio de archivos, evidencias, facturas, listados y documentos operativos. |
| 6 | Proceso de pagos y conciliacion | Validacion de pagos recibidos, soportes, conciliacion y registro de ventas. |

## 4. Escala utilizada

| Valor | Probabilidad | Impacto |
|---:|---|---|
| 1 | Raro | Consecuencia menor y facil de corregir. |
| 2 | Poco probable | Afecta una operacion limitada. |
| 3 | Posible | Afecta un proceso relevante o varios usuarios. |
| 4 | Probable | Interrumpe un servicio importante o expone informacion sensible. |
| 5 | Muy probable | Puede afectar gravemente la operacion, datos criticos o cumplimiento. |

El nivel de riesgo se calcula como: **Probabilidad x Impacto**. La matriz esta ordenada de mayor a menor prioridad.

## 5. Matriz inicial de riesgos priorizada

| Prioridad | Activo o proceso afectado | Amenaza | Vulnerabilidad | Riesgo como situacion y consecuencia | P | I | Nivel | Control actual o evidencia de que no existe | Control propuesto verificable | Justificacion breve de prioridad |
|---:|---|---|---|---|---:|---:|---:|---|---|---|
| 1 | Base de datos de clientes | Acceso no autorizado por terceros o personas internas sin necesidad de uso | Archivos con datos de clientes compartidos sin permisos definidos, sin revision periodica de accesos y posiblemente sin autenticacion multifactor | Si una persona no autorizada accede a la base de clientes, podria copiar, modificar o divulgar datos personales, afectando la confianza del cliente y generando posibles reclamos | 4 | 5 | 20 | No se evidencia una matriz de permisos ni registros periodicos de revision de accesos | Configurar permisos por rol, activar autenticacion multifactor, revisar mensualmente usuarios con acceso y conservar evidencia de la revision en una lista firmada o aprobada | Es el riesgo mas critico porque involucra informacion sensible y puede afectar reputacion, servicio y cumplimiento |
| 2 | Proceso de gestion de pedidos | Error humano, perdida de mensajes o manipulacion de informacion del pedido | Pedidos recibidos por varios canales sin formato unico, sin consecutivo y sin validacion antes del despacho | Si un pedido se registra incompleto o incorrecto, podria enviarse un producto equivocado, perderse una venta o generar reclamos por incumplimiento | 4 | 4 | 16 | Puede existir registro manual, pero no se evidencia formulario estandar ni control de consecutivos | Implementar formato unico de pedido con numero consecutivo, estado del pedido, responsable y validacion antes del despacho; revisar semanalmente pedidos cerrados contra entregas | La probabilidad es alta porque el proceso depende de registros manuales y varios canales de comunicacion |
| 3 | Proceso de pagos y conciliacion | Fraude, suplantacion de comprobantes o registro incorrecto de pagos | Confirmacion de pagos sin conciliacion formal contra extractos, pasarela o cuenta bancaria | Si se acepta un soporte falso o se omite una conciliacion, podria entregarse producto sin pago real o registrarse mal el ingreso de ventas | 3 | 5 | 15 | No se evidencia conciliacion documentada ni separacion clara entre quien confirma pago y quien despacha | Realizar conciliacion diaria o semanal contra extractos, registrar evidencia del pago validado y exigir aprobacion antes de cambiar el pedido a estado pagado | El impacto es alto porque afecta directamente los ingresos y la confiabilidad del proceso financiero |
| 4 | Almacenamiento en la nube | Eliminacion accidental, falla de cuenta o perdida de archivos | Ausencia de politica de respaldos, versionamiento y recuperacion probada | Si se eliminan facturas, listados o soportes de venta, la organizacion podria perder trazabilidad, retrasar entregas y no contar con evidencia ante reclamos | 3 | 4 | 12 | No se evidencia plan de copias de seguridad ni prueba de restauracion | Activar versionamiento, realizar respaldo semanal en una ubicacion separada y ejecutar una prueba mensual de restauracion documentada | Es prioritario porque sostiene evidencias del negocio y permite recuperacion ante errores o fallas |
| 5 | Inventario de productos | Descuadres, errores de registro o uso no autorizado de existencias | Inventario actualizado manualmente, sin conteos periodicos ni registro obligatorio de entradas y salidas | Si el inventario no refleja las existencias reales, podria venderse producto no disponible o no detectarse perdida de mercancia | 3 | 4 | 12 | Puede existir hoja de calculo, pero no se evidencia conteo fisico periodico ni responsable formal | Definir responsable de inventario, registrar entradas y salidas con fecha y soporte, y realizar conteo fisico quincenal comparado contra el registro | Tiene impacto operativo porque afecta ventas, entregas y confianza del cliente |
| 6 | Cuentas de correo y mensajeria | Phishing o suplantacion de identidad | Contraseñas debiles o reutilizadas, falta de doble factor y ausencia de capacitacion basica | Si una cuenta de correo o mensajeria es comprometida, un atacante podria contactar clientes, solicitar pagos falsos o acceder a informacion comercial | 3 | 4 | 12 | No se evidencia politica de contrasenas, doble factor ni registro de capacitacion | Activar doble factor, usar contrasenas unicas, documentar recuperacion de cuentas y realizar una capacitacion corta con evidencia de asistencia | La prioridad es media-alta porque el canal de comunicacion puede convertirse en entrada para fraude o fuga de informacion |

## 6. Relacion con los marcos seleccionados en el Taller Sesion 3

| Marco | Aplicacion en esta matriz |
|---|---|
| ISO/IEC 27001 | Sirve como referencia principal para proteger confidencialidad, integridad y disponibilidad de la informacion, especialmente datos de clientes, accesos, respaldos y controles documentados. |
| COBIT | Apoya el gobierno y control de los procesos de TI, permitiendo asignar responsables, evidencias, revisiones periodicas y trazabilidad en pedidos, pagos e inventario. |
| ITIL | Complementa la gestion operativa del servicio, especialmente en continuidad, atencion de incidentes, gestion de cambios y recuperacion ante fallas o reclamos. |

## 7. Conclusion

La matriz inicial muestra que los riesgos mas importantes para Alquimia Elixir Henao se concentran en la informacion de clientes, la gestion de pedidos y la validacion de pagos. La prioridad mas alta corresponde al acceso no autorizado a datos de clientes, porque combina probabilidad alta con impacto critico. Los controles propuestos son concretos y verificables, ya que pueden comprobarse mediante configuraciones, registros, respaldos, revisiones periodicas y evidencias documentadas.
