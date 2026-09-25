# Blue Laundry — SRS de negocio del sitio de clientes

**Versión:** 1.0

**Fecha:** 25 de septiembre de 2026

**Estado:** Base para revisión de negocio; decisiones pendientes identificadas.

**Alcance:** Exclusivamente la experiencia de clientes (`clients`).

## 1. Propósito del documento

Especificar qué debe comunicar y permitir el sitio de clientes de Blue Laundry, qué reglas comerciales representa actualmente y qué definiciones debe completar el cliente contratante antes de utilizarlo como canal comercial real.

Este SRS está dirigido a quienes toman decisiones comerciales y operacionales. No define arquitectura, programación ni integraciones. En este documento, **cliente contratante** es quien aprueba las condiciones de Blue Laundry; **visitante** o **cliente final** es quien consulta por un servicio de lavandería.

La base es el contenido actual de `clients/index.html`, contrastado con el plan de ajustes del 25 de septiembre de 2026. Los requisitos originales se usan como antecedente, no como descripción de funcionalidades actuales.

### Cómo interpretar los estados

| Estado | Significado |
|---|---|
| Base acordada | El plan reciente registra el acuerdo y el sitio lo refleja. No implica que la demo opere un servicio real. |
| Presente en la demo | El contenido existe, pero no constituye por sí solo una política comercial aprobada. |
| Pendiente de decisión | Falta una definición del cliente contratante. No se asume una respuesta. |
| Fuera de alcance | No forma parte de la experiencia actual ni se incorpora por este documento. |

## 2. Objetivo de negocio

Facilitar que una persona conozca los servicios, revise precios de referencia y sectores de retiro, y comience una conversación por WhatsApp para coordinar la atención.

La propuesta de valor es **«Tu ropa limpia, tu tiempo libre»**: ahorrar traslados y tiempo, con retiro y entrega a domicilio sujetos a coordinación y cuidado de las prendas según el servicio elegido.

El resultado esperado dentro del sitio es que el visitante comprenda la oferta y pueda abrir el contacto. La cotización, la disponibilidad y la coordinación ocurren manualmente fuera del sitio. **Abrir WhatsApp no equivale a enviar un mensaje, reservar un retiro ni confirmar una contratación.**

## 3. Alcance actual y antecedentes

### Incluido

- Presentación de la marca y mensajes comerciales.
- Catálogo de cuatro servicios con precios de referencia y plazo orientativo.
- Explicación del proceso de atención.
- Calendario semanal de retiros por sector.
- Consulta de retiros excepcionales, sujeta a confirmación.
- Acceso a WhatsApp con un mensaje preparado para coordinar o consultar disponibilidad.
- Beneficios, preguntas frecuentes y testimonios identificados como ilustrativos.
- Datos de contacto y nota de uso de la demo.
- Consulta desde teléfono, tableta y computador, con navegación comprensible y accesible.

### Fuera de alcance

- Panel de gestión, caja, inventario y cualquier función de `management`.
- Formulario de contratación, selección de cantidades, carrito y cálculo de un pedido.
- Reserva de fechas o cupos dentro del sitio.
- Registro de clientes, cuentas e historial de pedidos.
- Creación, confirmación o seguimiento de órdenes dentro del sitio.
- Cobros en línea, aplicación automática de descuentos y envío automático de notificaciones.
- Consulta de disponibilidad en tiempo real o gestión de reclamos dentro del sitio.

Los documentos iniciales describían un formulario de cinco pasos y una confirmación ficticia. **Ese flujo no está presente en la versión actual.** El plan reciente registra que «Agenda retiro» debe abrir WhatsApp. Este SRS conserva esa base; recuperar la contratación dentro del sitio sería un cambio de alcance que requeriría una decisión nueva.

## 4. Participantes y responsabilidades

| Participante | Necesidad o responsabilidad |
|---|---|
| Visitante / cliente final | Entender la oferta, consultar cobertura y precios, y contactar a Blue Laundry. |
| Atención de Blue Laundry | Recibir consultas y confirmar manualmente condiciones, disponibilidad y coordinación. La persona responsable y sus horarios están pendientes. |
| Cliente contratante | Aprobar catálogo, reglas de precio, promoción, cobertura, condiciones de atención y contenido público. |

La operación posterior al contacto solo se describe para aclarar las expectativas que genera el sitio; no se especifica aquí una herramienta para gestionarla.

## 5. Recorrido de negocio

1. **Conocer la propuesta.** El visitante identifica Blue Laundry y entiende el beneficio del servicio.
2. **Revisar servicios y referencias de precio.** Consulta qué incluye cada alternativa y cuáles requieren una cotización final.
3. **Consultar retiros.** Revisa días y sectores; puede consultar una excepción si su sector no aparece.
4. **Iniciar el contacto.** Selecciona «Agenda retiro» o la consulta de disponibilidad y abre WhatsApp con un mensaje preparado.
5. **Coordinar fuera del sitio.** El visitante decide enviar el mensaje. Blue Laundry debe confirmar manualmente las condiciones aplicables antes de asumir un compromiso. Los datos requeridos y el criterio de confirmación deben definirse en D-10.

No existe una pantalla de éxito comercial ni un número de orden generado por el sitio. Si el visitante no continúa en WhatsApp, la página no registra una solicitud.

## 6. Oferta comercial de referencia

### 6.1 Servicios

Los siguientes nombres y precios corresponden a la base acordada para la demo. Los importes se expresan en pesos chilenos.

| Servicio | Precio publicado | Alcance comunicado | Definición pendiente |
|---|---|---|---|
| Lavado por kilo | $3.690/kg | Lavado, secado y doblado de ropa cotidiana. | Mínimo, pesaje, redondeo, prendas admitidas y posibles recargos. |
| Lavado y planchado | Desde $15.000 | Lavado y planchado; valor final según cantidad y tipo de prendas, confirmado por WhatsApp. | Base de cobro y contenido del precio inicial. La descripción es provisional. |
| Planchado | Desde $12.000 | Planchado; valor final según cantidad y tipo de prendas, confirmado por WhatsApp. | Base de cobro y contenido del precio inicial. La descripción es provisional. |
| Lavado de ropa de cama | $5.590 por juego | Lavado de sábanas, quilt y artículos similares. | Qué incluye un juego y variaciones por tamaño, material o tipo de artículo. |

Los precios «desde» no tienen una unidad comercial definida. No deben interpretarse como valores por kilo, por prenda o por una cantidad determinada sin aprobación del cliente contratante.

### 6.2 Promoción y pago

- **Base acordada:** 15% de descuento en el primer pedido, sin código promocional.
- **Base acordada:** pago presencial; el sitio no realiza cobros.
- **Pendiente:** vigencia, elegibilidad, servicios incluidos, límites, acumulación y tratamiento de gastos de traslado.
- **Pendiente:** medios aceptados, momento y lugar del pago, y comunicación del importe final.

La demo comunica el descuento, pero no verifica si una persona es cliente nuevo ni calcula o aplica el beneficio.

### 6.3 Calendario de retiros

| Día | Atención o sectores publicados |
|---|---|
| Lunes | Atención en local. |
| Martes | Piedra Roja y Chicureo Centro. |
| Miércoles | La Reserva, Chamisero y El Umbral. |
| Jueves | Piedra Roja y Chicureo Centro. |
| Viernes | El Umbral, Chicauma, El Algarrobal y Santa Cecilia. |
| Sábado | Atención en local. |

- Los retiros se comunican de martes a viernes, hasta las 16:00.
- La Reserva y Chamisero son sectores separados.
- El calendario informa retiros programados; no reserva cupos ni garantiza disponibilidad.
- Se puede consultar excepcionalmente un retiro en otro sector, sujeto a confirmación.
- El calendario no define los días de entrega a domicilio.
- No se publican horario de inicio de retiros, dirección y horarios del local, ni condiciones para domingos o festivos. Su ausencia no significa apertura o cierre.

### 6.4 Plazo de entrega

La referencia común es **«Entrega desde 48 horas, según demanda»**. No equivale a entrega garantizada dentro de 48 horas. Falta definir desde qué momento se cuenta el plazo, si se consideran días hábiles y cómo se acuerda una fecha concreta.

El plan reciente menciona un servicio express con costo adicional, pero lo excluye de la promoción de esta versión. No forma parte del catálogo visible de cuatro servicios de este SRS.

## 7. Requisitos de negocio y aceptación

Estos criterios sirven para revisar el alcance con el cliente contratante. Su inclusión no certifica que se haya realizado una prueba de navegación en todos los dispositivos.

| ID | Requisito | Criterio de aceptación de negocio | Estado |
|---|---|---|---|
| RN-01 | Comunicar la propuesta de Blue Laundry y orientar hacia el contacto. | El visitante identifica la marca, el beneficio principal y la acción «Agenda retiro». | Base acordada. |
| RN-02 | Mostrar los cuatro servicios y distinguir precios por unidad de precios «desde». | Cada servicio presenta nombre, descripción, precio y plazo; los dos precios «desde» indican que el valor final se confirma por WhatsApp. | Base acordada; reglas de cobro pendientes. |
| RN-03 | Explicar el proceso sin presentar una consulta como reserva. | Se describen consulta del calendario, coordinación del retiro, cuidado de prendas y coordinación de entrega. | Base acordada. |
| RN-04 | Mostrar el calendario de retiros por sector. | Se presentan los seis días de la tabla, la atención en local y el límite de las 16:00, sin prometer entregas en esos mismos días. | Base acordada. |
| RN-05 | Permitir consultar cobertura excepcional. | La consulta por otro sector está disponible y se explica que requiere confirmación. | Base acordada; condiciones pendientes. |
| RN-06 | Facilitar el contacto para coordinar un retiro. | «Agenda retiro» dirige a WhatsApp con el mensaje «Hola, quiero coordinar un retiro con Blue Laundry»; no comunica una orden confirmada. | Base acordada. |
| RN-07 | Comunicar la promoción de bienvenida. | Se muestran 15% en el primer pedido, ausencia de código y pago presencial. Para uso comercial deben incorporarse las condiciones aprobadas en D-04. | Base acordada; condiciones pendientes. |
| RN-08 | Informar un plazo orientativo consistente. | Servicios, proceso y preguntas frecuentes expresan «desde 48 horas, según demanda» y remiten a la confirmación del plazo. | Base acordada. |
| RN-09 | Resolver dudas antes del contacto. | Se pueden consultar respuestas sobre plazo, precios, prendas, cambios de coordinación y cuidado especial. | Presente en la demo. |
| RN-10 | Presentar beneficios sin atribuir capacidades inexistentes. | El contenido no promete reservas, seguimiento o atención automática desde la página. | Presente en la demo. |
| RN-11 | Distinguir ejemplos de testimonios reales. | Los tres testimonios y sus valoraciones se identifican como ilustrativos; su uso comercial requiere D-13. | Presente en la demo. |
| RN-12 | Mostrar contacto y límites de la demostración. | El teléfono, correo, referencia geográfica y nota de demo son consultables; se aclara que no hay contratación ni pagos dentro del sitio. | Presente en la demo; datos por validar. |
| RN-13 | Facilitar el uso en distintos dispositivos y formas de navegación. | Se puede leer, navegar y acceder al contacto desde móvil, tableta y computador; los controles son comprensibles, utilizables con teclado y los mensajes rotativos pueden pausarse. | Criterio de aceptación pendiente de revisión práctica. |

## 8. Decisiones pendientes del cliente contratante

**Todas las decisiones siguientes permanecen abiertas en este SRS.** Se distingue lo expresamente pendiente en el plan de lo que no está definido en los materiales revisados. Los roles indicados son responsables sugeridos; el cliente contratante debe asignar a la persona que aprueba.

**Prioridad A:** resolver antes de presentar la oferta como un servicio comercial definitivo. **Prioridad B:** resolver para completar la atención y evaluación del canal. Estas prioridades son una propuesta de revisión, no nuevos acuerdos.

| ID / prioridad | Decisión que debe tomar el cliente | Situación actual y respuesta requerida | Responsable sugerido |
|---|---|---|---|
| D-01 / A | Base de cobro de lavado y planchado y de planchado. | Pendiente explícito del plan. Definir qué obtiene el cliente por $15.000 y $12.000, unidad o paquete, mínimos, exclusiones y cómo varía el total. | Comercial. |
| D-02 / A | Reglas de kilo y juego. | No definidas. Aprobar mínimo de kilos, pesaje y redondeo; composición del juego de cama y tarifas por tamaño o artículo. | Comercial y operación. |
| D-03 / A | Costo completo del servicio. | No se informa si retiro y entrega tienen costo o están incluidos. Definir cargos por zona, mínimos, recargos e inclusión de impuestos en los precios publicados. No asumir traslado gratuito. | Comercial. |
| D-04 / A | Condiciones de la promoción del 15%. | El porcentaje y la ausencia de código están acordados. Definir vigencia, qué significa primer pedido, servicios elegibles, monto máximo o mínimo, acumulación y base sobre la cual se descuenta. | Comercial. |
| D-05 / A | Condiciones del pago presencial. | Modalidad general acordada. Definir efectivo, tarjeta u otros medios, lugar, momento, comprobante y aceptación del valor final por el cliente. | Comercial y operación. |
| D-06 / A | Límites de cobertura y excepciones. | Días y sectores acordados. Definir límites territoriales, direcciones atendibles, criterios y recargos de excepciones y quién puede confirmarlas. | Operación. |
| D-07 / A | Reglas para agendar retiros. | Se publica «hasta las 16:00». Aclarar si es fin de los retiros o corte de solicitudes; definir hora de inicio, anticipación, ventanas de atención, cupos y festivos. | Operación. |
| D-08 / A | Compromiso de entrega. | Se publica «desde 48 horas, según demanda». Definir inicio del cómputo, días hábiles o corridos, entrega a domicilio o retiro en local, ventanas y comunicación de atrasos. | Operación. |
| D-09 / A | Admisión y cuidado de prendas. | No hay listado completo de exclusiones. Definir prendas y materiales aceptados, revisión de estado, manchas, tratamientos especiales y autorización de cargos adicionales. | Operación. |
| D-10 / A | Atención y confirmación por WhatsApp. | El canal está acordado. Definir responsable, horario y tiempo objetivo de respuesta, datos que se solicitan, quién confirma precio y retiro y qué mensaje deja constancia del acuerdo. | Atención y operación. |
| D-11 / A | Cambios, cancelaciones e incidencias. | La demo remite a una conversación manual. Definir anticipación para cambios, retiros fallidos, ausencia del cliente, reclamos, daños, pérdidas, repetición del servicio y devoluciones cuando correspondan. | Dirección y operación. |
| D-12 / A | Identidad, contactos y atención local. | Se muestran +56 9 4199 0328, hola@bluelaundry.cl y Santiago, Chile. Validar titularidad y uso comercial, dirección del local y horarios, especialmente lunes y sábado. | Cliente contratante. |
| D-13 / A | Contenido y documentos para uso comercial. | La nota de demo no sustituye condiciones del servicio; la política de privacidad no está disponible y los testimonios son ficticios. Aprobar textos comerciales, tratamiento de datos del contacto y testimonios reales autorizados, o retirar estos últimos. | Cliente contratante, con los asesores que determine. |
| D-14 / B | Alternativa para quienes no usan WhatsApp. | El correo y teléfono se muestran como contacto, pero no se define un proceso alternativo. Decidir si se aceptan solicitudes por llamada o correo y quién las atiende. | Atención. |
| D-15 / B | Evaluación y mantenimiento del canal. | No hay metas ni responsables definidos. Elegir indicadores, metas, frecuencia de revisión y responsable de mantener precios, promoción, calendario y preguntas frecuentes. | Comercial. |

La aprobación de este SRS no completa automáticamente estas decisiones. Cada respuesta debe quedar registrada con su responsable y fecha, y reflejarse en el contenido cuando corresponda.

## 9. Escenarios que requieren una respuesta comercial

| Situación del visitante | Respuesta prevista en el alcance actual | Decisión relacionada |
|---|---|---|
| Su sector no aparece en el calendario. | Puede consultar una excepción; no se le garantiza atención. | D-06. |
| Necesita una fecha o retiro inmediato. | Debe consultar disponibilidad; el calendario no asegura un cupo. | D-07 y D-08. |
| Quiere saber el total de un servicio «desde». | Debe recibir una cotización manual según las reglas que apruebe Blue Laundry. | D-01 a D-03. |
| Solicita el descuento del primer pedido. | La página informa el beneficio; la elegibilidad y aplicación se resuelven fuera del sitio. | D-04. |
| Desea cambiar o cancelar un retiro coordinado. | Debe contactar manualmente; la página no modifica reservas. | D-10 y D-11. |
| Tiene una prenda especial o un reclamo. | Requiere evaluación y atención manual, sin promesa de tratamiento o compensación en la demo. | D-09 y D-11. |
| No puede continuar en WhatsApp. | Puede consultar los datos de contacto visibles; falta acordar el canal alternativo de atención. | D-14. |

## 10. Indicadores propuestos para validar el negocio

Los siguientes indicadores son propuestas sujetas a D-15. No se afirma que el sitio los mida actualmente.

- Consultas recibidas que provienen del sitio.
- Proporción de consultas que terminan en un retiro confirmado manualmente.
- Tiempo de respuesta durante el horario de atención acordado.
- Consultas rechazadas por cobertura o falta de disponibilidad.
- Dudas recurrentes sobre precio, descuento, retiro y entrega.

El cliente debe definir metas y una forma de registrar los resultados. Un clic de contacto, un mensaje recibido y un servicio confirmado son eventos distintos y deben evaluarse por separado.

## 11. Criterios para aprobar el documento

El cliente contratante podrá aprobar este SRS como base del alcance cuando:

1. Reconozca que la experiencia actual es informativa y deriva a coordinación manual por WhatsApp.
2. Valide la oferta y el calendario descritos como base acordada.
3. Identifique a los responsables y las fechas para resolver D-01 a D-15.
4. Distinga la aprobación de la demo de la autorización para publicar condiciones comerciales definitivas.
5. Acepte que nuevas funciones de contratación, pago o seguimiento requieren ampliar el alcance.

| Registro de aprobación | Por completar |
|---|---|
| Nombre y rol de quien aprueba | Pendiente. |
| Fecha de revisión | Pendiente. |
| Resultado | Pendiente: aprobado / aprobado con observaciones / requiere ajustes. |
| Decisiones resueltas y observaciones | Registrar IDs, respuesta y fecha. |

## 12. Fuentes y límite de la revisión

- **Fuente principal:** `clients/index.html`, versión local revisada el 25 de septiembre de 2026.
- **Acuerdos recientes:** `docs/superpowers/plans/2026-09-25-ajustes-cliente.md`, especialmente contenido acordado y validación comercial pendiente.
- **Antecedentes:** `PRODUCT.md`, `REQUIREMENTS.md`, `DESIGN.md` y `AGENTS.md`. Sus referencias al formulario de contratación no describen la experiencia actual.

El documento se elaboró mediante revisión de los archivos y del contenido declarado. No confirma capacidad operacional, propiedad de los contactos, vigencia comercial de las condiciones ni resultados de pruebas de navegación. No se modificó la demo para elaborar este SRS.
