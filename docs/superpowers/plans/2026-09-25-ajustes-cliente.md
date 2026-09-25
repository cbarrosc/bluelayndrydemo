# Ajustes de la demo Blue Laundry — Plan de implementación

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans para implementar este plan por tareas en esta sesión. Los pasos usan casillas para registrar avance. No comenzar hasta que el usuario apruebe el plan completo.

**Goal:** Ajustar la landing de clientes con el mensaje comercial, precios, plazos y calendario acordados, y facilitar la coordinación de retiros por WhatsApp.

**Architecture:** Conservar la landing estática y autónoma en `clients/index.html`, con CSS y JavaScript embebidos. Actualizar el contenido, `DATA.services`, `DATA.deliverySchedule` y sus renderizadores; conservar la identidad visual azul, el carrusel, las secciones y la navegación existente.

**Tech Stack:** HTML, CSS y JavaScript vanilla, sin dependencias nuevas.

**Spec:** Acuerdos de esta conversación, consolidados en la sección «Contenido y comportamiento acordados» de este documento. Este plan no autoriza por sí mismo la implementación.

## Alcance y restricciones

- Implementar todos los cambios aprobados en una rama separada: `feat/ajustes-demo-cliente`.
- No agregar backend, base de datos, autenticación, pagos ni APIs externas.
- Mantener funcionamiento mediante `file://` y servidor estático local.
- Mantener marca Blue Laundry, paleta azul, diseño responsive, foco visible y navegación por teclado.
- Mantener una indicación visible de demo, sin atribuir reservas, disponibilidad en tiempo real ni integraciones inexistentes.
- Conservar HTML, CSS y JS en el archivo autónomo existente.
- No modificar el hub ni la demo de gestión: el alcance acordado es la landing de clientes.
- Usar español neutro y precios en pesos chilenos.
- No enviar mensajes por WhatsApp durante las pruebas.
- Preparar el PR al terminar; no fusionarlo.

## Evidencia del estado actual

- Rama observada: `master`, sin cambios locales antes de escribir este plan.
- La landing usa enlaces directos a `web.whatsapp.com` con el teléfono `56941990328`.
- El carrusel muestra una promoción del 20% con código `BIENVENIDA20`.
- Los precios y plazos están en `DATA.services` y se imprimen mediante `renderServices()`.
- El calendario está en `DATA.deliverySchedule`; `renderDeliverySchedule()` actualmente distingue solo entre ruta activa y «Sin servicio».
- `AGENTS.md`, `PRODUCT.md` y `DESIGN.md` describen un wizard anterior. La implementación actual dirige a WhatsApp. Para estos ajustes prevalece la instrucción explícita del usuario: «Agenda retiro» abre WhatsApp. No reconstruir el wizard ni actualizar documentación histórica fuera del alcance.
- El cargador de contexto de Impeccable no pudo ejecutarse por ausencia de su motor y permisos de instalación; se leyeron directamente los documentos del proyecto. Esto no bloquea la planificación ni exige instalar herramientas.

## Contenido y comportamiento acordados

### Mensaje principal y promoción

- Lema principal: **«Tu ropa limpia, tu tiempo libre»**.
- Promoción: **«15% de descuento en tu primer pedido»**.
- Eliminar el código promocional y las referencias a códigos ficticios.
- Aclaración de promoción: **«Sin código de descuento. Pago presencial»**.
- Reemplazar las etiquetas «Solicitar lavandería» por **«Agenda retiro»**; el destino es WhatsApp.
- Conservar el carrusel y aprovechar su tercer mensaje para orientar al visitante hacia el proceso y el calendario: **«Revisa cómo funciona, consulta nuestro calendario y envíanos un WhatsApp»**.
- Mantener «Agenda retiro» como acción principal y los enlaces a proceso y calendario como acciones secundarias, sin competir visualmente con el contacto.

### Proceso

- Introducción de «Cómo funciona»: **«Lavamos, secamos, planchamos y doblamos»**, sin puntos suspensivos.
- Los pasos inferiores explicarán: consultar calendario, coordinar retiro por WhatsApp, cuidado de las prendas y coordinación de entrega.
- Copy propuesto para los pasos:
  1. **Consulta el calendario:** «Revisa los días de retiro programados para tu sector».
  2. **Agenda tu retiro:** «Envíanos un WhatsApp para coordinar los detalles. Retiros de martes a viernes hasta las 16:00».
  3. **Cuidamos tus prendas:** «Lavamos, secamos, planchamos y doblamos según el servicio que elijas».
  4. **Coordinamos la entrega:** «Entrega desde 48 horas, según demanda. Confirma los detalles por WhatsApp».
- No presentar el envío de un mensaje como una reserva confirmada.

### Servicios, precios y plazos

| Servicio | Precio visible | Descripción |
|---|---|---|
| Lavado por kilo | $3.690/kg | Lavado, secado y doblado de ropa cotidiana. |
| Lavado y planchado | Desde $15.000 | Lavado y planchado de tus prendas. El valor final depende de la cantidad y el tipo de prendas; se confirma por WhatsApp. |
| Planchado | Desde $12.000 | Planchado de tus prendas. El valor final depende de la cantidad y el tipo de prendas; se confirma por WhatsApp. |
| Lavado de ropa de cama | $5.590 por juego | Lavado de sábanas, quilt y similares. |

- Los cuatro servicios mostrarán **«Entrega desde 48 horas, según demanda»**.
- Sustituir el servicio actual «Lavado delicado» por «Lavado y planchado» en el catálogo de cuatro tarjetas.
- Las descripciones de lavado y planchado y de planchado son provisionales, autorizadas por el usuario. La base comercial de cobro queda pendiente de su validación posterior; no inventar kilo, cantidad de prendas ni tamaño de pedido.
- Corregir textos contradictorios en beneficios y FAQ: no prometer entrega en 24 horas, dentro de 48 horas ni una fecha garantizada.
- El express existe y tiene costo adicional, pero no se destacará en esta iteración. No añadir banner, tarjeta, CTA ni promoción express. Si ya hubiera una mención que deba conservarse, aclarar su recargo.

### Calendario

| Día | Atención / sectores |
|---|---|
| Lunes | Solo atención en el local |
| Martes | Piedra Roja, Chicureo Centro |
| Miércoles | La Reserva, Chamisero, El Umbral |
| Jueves | Piedra Roja, Chicureo Centro |
| Viernes | El Umbral, Chicauma, El Algarrobal, Santa Cecilia |
| Sábado | Solo atención en el local |

- La Reserva y Chamisero son sectores separados, confirmado por el usuario.
- Mostrar seis días, de lunes a sábado; retirar la tarjeta de domingo. No inferir horarios de atención del local ni su apertura o cierre el domingo.
- Texto visible: **«Retiros de martes a viernes hasta las 16:00. Si no tenemos un delivery programado, podemos coordinar excepcionalmente un retiro en otro sector. Consulta disponibilidad por WhatsApp»**.
- El lunes y el sábado deben decir «Atención en local», nunca «Sin servicio» ni «Retiro y entrega».
- Las rutas deben describirse como retiros programados; no prometer que todas las entregas ocurren en esos mismos días.
- La excepción requiere coordinación; no equivale a cobertura automática ni anula el límite de horario comunicado.

### WhatsApp

- Conservar el número existente `56941990328`, pues no se solicitó cambiarlo.
- Mensaje propuesto para los CTA de retiro: **«Hola, quiero coordinar un retiro con Blue Laundry»**.
- Objetivo: abrir WhatsApp móvil, ofrecer la aplicación de escritorio cuando esté disponible y permitir continuar en WhatsApp Web.
- Antes de implementar, verificar la documentación oficial vigente de enlaces de WhatsApp. Usar el enlace HTTPS oficial apropiado; candidato: `https://wa.me/56941990328?text=Hola%2C%20quiero%20coordinar%20un%20retiro%20con%20Blue%20Laundry`.
- No prometer detección automática infalible de aplicaciones instaladas. Registrar qué navegación controla el sitio y cuál resuelven WhatsApp, el navegador y el sistema operativo.
- Si el enlace oficial no ofrece una alternativa web suficientemente clara, añadir un enlace secundario explícito «Abrir WhatsApp Web». Evitar redirecciones temporizadas que puedan abrir dos destinos.
- Revisar todos los enlaces de WhatsApp de la landing, incluidos encabezado, carrusel y pie de página.

## Archivos e interfaces

- Modificar: `clients/index.html`: contenido, estilos acotados, datos y renderizadores de la landing.
- Mantener este plan actualizado con casillas y resultados de validación.
- `DATA.services` conservará `id`, `name`, `desc`, `price`, `unit`, `time` e `icon`; añadirá `priceFrom: boolean` y `unitPrefix?: string` para distinguir valores «desde» y unidades que se imprimen como «por juego». `unit` será vacío en los servicios sin unidad confirmada.
- `renderServices()` imprimirá el prefijo «Desde» cuando corresponda y omitirá la unidad si está vacía; usará `unitPrefix: 'por'` en ropa de cama para mostrar «por juego».
- `DATA.deliverySchedule` añadirá `label: string`; `renderDeliverySchedule()` imprimirá esa etiqueta en vez de deducirla de `active`. El lunes y el sábado no tendrán ruta activa, pero sí atención en local.
- No crear módulos, componentes compartidos ni un sistema de precios nuevo para estos cambios.

## Foco de revisión

1. Teléfono o escritorio sin aplicación instalada: el visitante conserva una vía utilizable hacia WhatsApp, sin bucles ni pestañas duplicadas.
2. Pantalla de 320–375 px: precios, plazos largos y cuatro sectores del viernes no se recortan ni provocan scroll horizontal.
3. Navegación por teclado y movimiento reducido: CTA accesibles, carrusel controlable y enlaces de diapositivas ocultas fuera del recorrido de foco.
4. Lunes y sábado: mostrar atención en local sin confundirla con retiro ni seguir anunciando rutas sabatinas.
5. Precios sin unidad confirmada y plazos: no aparece «/prenda», una barra vacía ni una promesa de entrega garantizada en 48 horas.

## Tareas de implementación

### 1. Preparar rama y actualizar mensaje comercial

**Archivo:** `clients/index.html`, encabezado, carrusel y sección `#how`.

- [ ] Revisar estado Git y conservar cualquier cambio ajeno. Crear la rama `feat/ajustes-demo-cliente` antes de tocar la aplicación; conservar este plan en ella.
- [ ] Leer `superpowers:executing-plans` y, justo antes de editar UI, `impeccable/reference/craft-floor.md`. Consultar el playbook de copy `reference/clarify.md`.
- [ ] Revisar la landing actual en escritorio y móvil como referencia visual.
- [ ] Aplicar lema, promoción del 15%, pago presencial, CTA «Agenda retiro» y copy del proceso definidos arriba.
- [ ] Mantener una nota visible de demo y sustituir «ofertas y códigos ficticios» por «Contenido demostrativo».
- [ ] Comprobar carrusel, enlaces a `#how` y `#delivery`, foco, pausa y comportamiento con movimiento reducido.
- [ ] Verificar que no quedan referencias comerciales al 20% ni a `BIENVENIDA20` en la landing.

### 2. Actualizar catálogo y plazos

**Archivo:** `clients/index.html`, `DATA.services`, `renderServices()`, beneficios y `DATA.faqs`.

- [ ] Aplicar las cuatro filas de la tabla acordada y el plazo común.
- [ ] Introducir `priceFrom` y unidades opcionales, manteniendo `price` numérico y formato `es-CL`.
- [ ] Adaptar el renderizador para mostrar exactamente `$3.690/kg`, `Desde $15.000`, `Desde $12.000` y `$5.590 por juego`.
- [ ] Actualizar la FAQ de tiempos: «Las entregas son desde 48 horas, según la demanda. Confirma el plazo de tu pedido por WhatsApp».
- [ ] Actualizar la FAQ de precios: «El pago es presencial. Los servicios con precio desde requieren confirmar el valor final por WhatsApp según la cantidad y el tipo de prendas».
- [ ] Revisar que ninguna tarjeta ni beneficio contradiga esos precios, unidades o plazos; comprobar ajuste de texto a 320–375 px.
- [ ] Mantener el express fuera de las llamadas promocionales.

### 3. Ajustar calendario y disponibilidad excepcional

**Archivo:** `clients/index.html`, `DATA.deliverySchedule`, `renderDeliverySchedule()`, `.delivery-grid` y `.delivery-note`.

- [ ] Sustituir los datos por los seis días acordados y sus sectores exactos.
- [ ] Añadir etiquetas explícitas «Atención en local» y «Retiros programados», evitando inferir «Sin servicio» para el lunes y el sábado.
- [ ] Añadir horario hasta las 16:00 y explicación de cobertura excepcional, con enlace para consultar por WhatsApp.
- [ ] Ajustar la grilla de seis días siguiendo los estilos existentes; usar una columna en pantallas estrechas si las listas no caben cómodamente.
- [ ] Comprobar visualmente el lunes, el viernes y el sábado, los nombres separados de La Reserva y Chamisero y la ausencia de rutas de fin de semana.

### 4. Unificar destinos de WhatsApp

**Archivo:** `clients/index.html`, todos los enlaces de WhatsApp.

- [ ] Verificar la documentación oficial vigente y registrar el enlace elegido y sus límites de apertura de aplicaciones.
- [ ] Aplicar el destino HTTPS adecuado, número existente y mensaje de retiro codificado, conservando enlaces HTML funcionales sin depender de JavaScript.
- [ ] Verificar que todos los CTA «Agenda retiro» y los enlaces de contacto tienen un destino válido; mantener nombres accesibles en enlaces con iconos.
- [ ] Probar desde el navegador disponible hasta la pantalla de apertura o selección de WhatsApp, sin enviar mensajes.
- [ ] Comprobar la alternativa web y que no existen temporizadores ni intentos repetidos de apertura.
- [ ] Registrar por separado los entornos realmente probados: la emulación móvil valida el layout, pero no demuestra apertura de una app nativa en un teléfono real.

### 5. Verificación integrada y PR

**Archivos:** cambios finales en `clients/index.html` y este plan.

- [ ] Realizar una pasada conjunta en escritorio y móvil: 1440 px, 768 px y 320–375 px. Verificar textos, precios, calendario, CTA, menú móvil, carrusel y FAQ.
- [ ] Comprobar teclado, foco visible, ausencia de scroll horizontal y errores de consola, tanto con servidor estático como abriendo el HTML directamente.
- [ ] Corregir en una sola tanda los defectos encontrados y hacer una segunda pasada de confirmación como máximo, según Impeccable.
- [ ] No añadir una infraestructura de tests para cambios de copy. Si la implementación exige lógica de navegación adicional, cubrir sus ramas con pruebas de comportamiento antes de darla por terminada.
- [ ] Ejecutar `git diff --check` y revisar el diff para descartar modificaciones al hub, gestión o contenido fuera de alcance.
- [ ] Registrar resultados y limitaciones reales de las pruebas, especialmente la apertura de aplicaciones nativas.
- [ ] Hacer commit de los cambios revisados, publicar la rama y crear un PR contra la rama base del repositorio, confirmándola antes de crearlo.
- [ ] Describir en el PR el problema, resultado, validaciones y la base de cobro aún pendiente para los dos precios «desde». Adjuntar el PR a esta tarea y entregar su enlace. No hacer merge.

## Criterio de finalización

El plan queda cumplido cuando la landing refleja el contenido acordado, los enlaces permiten iniciar la coordinación por WhatsApp, la revisión responsive y funcional pasa, y el PR está preparado con evidencia de validación. La aprobación posterior de las bases de cobro comerciales no bloquea los textos provisionales autorizados.

## Registro de implementación

- Rama creada: `feat/ajustes-demo-cliente`.
- Implementado: lema y CTA, promoción, textos del proceso, cuatro servicios y precios, plazos, FAQ, calendario de lunes a sábado y todos los destinos de WhatsApp.
- WhatsApp: la ayuda oficial confirma que `wa.me` admite mensajes precargados y funciona en teléfonos y WhatsApp Web. El navegador determina si continúa en la aplicación disponible. [Ayuda oficial de WhatsApp](https://faq.whatsapp.com/5913398998672934).
- Comprobaciones ejecutadas: `git diff --check` pasó; `node --check` sobre el script embebido pasó; la búsqueda no encontró los textos antiguos de promoción, precios ni enlaces directos a WhatsApp Web.
- Límite pendiente de validación: la política de seguridad del navegador de esta sesión rechazó abrir `file:///.../clients/index.html`. No se inspeccionaron capturas de escritorio o móvil, la consola del navegador ni la apertura real de WhatsApp en teléfono o aplicación de escritorio. No se intentó eludir el bloqueo. La revisión visual y de comportamiento manual debe completarse en un navegador del usuario antes de fusionar.
- Aún pendiente de validación comercial: base de cobro para «Lavado y planchado desde $15.000» y «Planchado desde $12.000».
