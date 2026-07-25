# Requerimiento funcional

## Demo HTML de sistema de gestión para lavandería

## 1. Contexto

Se requiere diseñar una demo HTML de un sistema de gestión operacional para lavanderías, lavasecos y tintorerías.

La solución estará orientada principalmente a los trabajadores del local:

* Recepcionistas.
* Operadores.
* Cajeros.
* Supervisores.
* Administradores.

El sistema permitirá representar visualmente el flujo completo desde que un cliente entrega sus prendas hasta que la orden es pagada, procesada y entregada.

La demo se inspira funcionalmente en plataformas de gestión como EasyLaundry, pero no debe copiar su identidad visual, código, textos, estructura exacta ni elementos propietarios.

---

# 2. Objetivo

Construir una demo navegable que permita validar:

* Ingreso de órdenes de trabajo.
* Registro y consulta de clientes.
* Ingreso detallado de prendas y servicios.
* Aplicación de promociones y descuentos.
* Registro de pagos.
* Seguimiento del estado de las órdenes.
* Comunicación con clientes mediante WhatsApp.
* Gestión básica de retiro y entrega.
* Visualización de indicadores operacionales.

La demo no debe ser productiva. Su propósito es validar la experiencia de usuario y servir como base visual para una futura implementación.

---

# 3. Alcance técnico

La demo deberá construirse utilizando:

* HTML semántico.
* CSS.
* JavaScript vanilla.
* Datos simulados.
* Persistencia opcional mediante `localStorage`.

No se requiere:

* Backend.
* Base de datos.
* Autenticación real.
* Integración real con WhatsApp.
* Integración con medios de pago.
* Integración con impresoras.
* Consumo de APIs externas.
* Geolocalización real.
* Optimización real de rutas.

Debe poder ejecutarse mediante un servidor estático local.

---

# 4. Enfoque de programación agéntica

El proyecto estará preparado para ser implementado y mantenido principalmente mediante agentes de desarrollo.

El agente deberá:

1. Leer este requerimiento completo.
2. Proponer una estructura mínima antes de implementar.
3. Dividir la solución en módulos visuales independientes.
4. Implementar primero los flujos críticos.
5. Utilizar datos simulados centralizados.
6. Validar cada criterio de aceptación.
7. Evitar arquitectura innecesaria.
8. Documentar decisiones no especificadas.
9. Verificar visualmente escritorio y tablet.
10. Recorrer manualmente el flujo completo antes de declarar la tarea terminada.

El agente puede tomar decisiones menores de diseño, pero no modificar las reglas funcionales centrales.

---

# 5. Perfil principal de usuario

## Trabajador de recepción

Persona encargada de:

* Buscar o registrar clientes.
* Crear órdenes de trabajo.
* Registrar las prendas recibidas.
* Seleccionar servicios.
* Registrar observaciones o daños.
* Aplicar promociones.
* Recibir pagos.
* Entregar comprobantes.
* Contactar al cliente.
* Actualizar el estado de la orden.

El flujo debe ser rápido y usable mientras el cliente espera frente al mesón.

---

# 6. Navegación principal

La demo deberá incluir una navegación lateral con las siguientes opciones:

* Inicio.
* Nueva orden.
* Órdenes de trabajo.
* Clientes.
* Servicios y prendas.
* Promociones.
* Caja.
* Retiros y entregas.
* Reportes.
* Configuración.

En la parte superior deberá mostrarse:

* Nombre del local.
* Sucursal seleccionada.
* Usuario activo.
* Fecha actual simulada.
* Acceso a búsqueda global.
* Indicador de caja abierta o cerrada.

---

# 7. Dashboard operacional

La pantalla de inicio deberá mostrar un resumen diario.

## Indicadores principales

* Órdenes ingresadas hoy.
* Órdenes en proceso.
* Órdenes listas.
* Órdenes atrasadas.
* Entregas pendientes.
* Pagos pendientes.
* Ventas del día.
* Caja actual.

## Alertas operacionales

Mostrar una lista con situaciones que requieren atención:

* Órdenes atrasadas.
* Pedidos listos no retirados.
* Pagos pendientes.
* Entregas programadas para hoy.
* Prendas con observaciones especiales.
* Clientes pendientes de notificación.

## Actividad reciente

Mostrar los últimos eventos:

* Orden creada.
* Pago registrado.
* Orden cambiada de estado.
* WhatsApp enviado.
* Orden entregada.
* Descuento aplicado.

---

# 8. Módulo de clientes

## 8.1 Listado de clientes

La pantalla deberá permitir:

* Buscar por nombre.
* Buscar por teléfono.
* Buscar por correo.
* Buscar por RUT o identificador.
* Filtrar clientes frecuentes.
* Filtrar clientes con deuda.
* Crear un nuevo cliente.
* Abrir la ficha del cliente.

Cada registro deberá mostrar:

* Nombre.
* Teléfono.
* Correo.
* Cantidad de órdenes.
* Última visita.
* Total acumulado.
* Estado de deuda.
* Acceso directo a WhatsApp.

## 8.2 Registro de cliente

El formulario deberá incluir:

* Nombre.
* Apellido.
* Teléfono.
* Correo electrónico.
* RUT o identificador.
* Dirección.
* Comuna.
* Preferencia de contacto.
* Observaciones.
* Permiso para recibir promociones.

El teléfono será obligatorio porque se utilizará como canal principal de contacto.

## 8.3 Ficha de cliente

La ficha deberá mostrar:

* Datos personales.
* Direcciones registradas.
* Historial de órdenes.
* Órdenes activas.
* Pagos pendientes.
* Promociones utilizadas.
* Preferencias.
* Observaciones internas.
* Botón `Contactar por WhatsApp`.
* Botón `Crear nueva orden`.

---

# 9. Nueva orden de trabajo

La creación de una OT será el flujo principal de la demo.

Deberá implementarse como una pantalla única dividida en secciones o como un proceso paso a paso.

## Paso 1: Seleccionar cliente

El trabajador podrá:

* Buscar un cliente existente.
* Seleccionar un resultado.
* Crear un cliente sin abandonar el flujo.
* Continuar como cliente ocasional.

Al seleccionar el cliente se mostrará:

* Nombre.
* Teléfono.
* Deuda pendiente.
* Últimas órdenes.
* Promociones disponibles.
* Observaciones relevantes.

---

## Paso 2: Ingresar prendas

El trabajador deberá poder agregar una o más prendas.

Cada ítem deberá incluir:

* Tipo de prenda.
* Categoría.
* Cantidad.
* Servicio solicitado.
* Precio unitario.
* Recargo.
* Descuento.
* Subtotal.
* Fecha estimada de entrega.
* Observaciones.

Ejemplos de prendas:

* Camisa.
* Pantalón.
* Chaqueta.
* Vestido.
* Abrigo.
* Terno.
* Falda.
* Edredón.
* Frazada.
* Cortina.
* Alfombra.
* Zapatillas.

## Categorías sugeridas

* Ropa diaria.
* Ropa formal.
* Ropa delicada.
* Ropa de cama.
* Hogar.
* Calzado.
* Alfombras.
* Otros.

## Servicios sugeridos

* Lavado.
* Lavado en seco.
* Planchado.
* Lavado y planchado.
* Desmanchado.
* Sanitizado.
* Secado.
* Reparación menor.
* Servicio express.

---

## Paso 3: Detalle físico de la prenda

Cada prenda podrá registrar:

* Color.
* Marca.
* Material.
* Talla.
* Estado de recepción.
* Mancha visible.
* Daño previo.
* Botón faltante.
* Cierre dañado.
* Desgaste.
* Decoloración.
* Instrucción especial.

Las observaciones deberán ser visibles durante todo el procesamiento de la orden.

Ejemplo:

> Chaqueta azul recibida con desgaste en manga derecha y botón inferior faltante.

La demo deberá permitir marcar visualmente una prenda como:

* Normal.
* Delicada.
* Con daño previo.
* Con tratamiento especial.

---

## Paso 4: Fotografías simuladas

La interfaz deberá incluir un control para representar la carga de fotografías de recepción.

No será necesario almacenar archivos reales.

La demo podrá mostrar miniaturas estáticas simulando:

* Vista general de la prenda.
* Mancha.
* Daño previo.
* Etiqueta de cuidado.

Las fotografías deberán quedar asociadas visualmente a la prenda correspondiente.

---

## Paso 5: Promociones y descuentos

El sistema deberá sugerir promociones compatibles con la orden.

Ejemplos:

* 10% de descuento en primera compra.
* 20% en lavado de camisas.
* Quinta prenda sin costo.
* Descuento para clientes frecuentes.
* Promoción por monto mínimo.
* Descuento manual autorizado.
* Cupón promocional.
* Precio especial por convenio.

Cada promoción deberá indicar:

* Nombre.
* Descripción.
* Vigencia.
* Condiciones.
* Beneficio aplicado.
* Compatibilidad con otras promociones.

El sistema deberá distinguir entre:

* Promoción automática.
* Cupón.
* Descuento manual.
* Descuento por convenio.

Cuando se aplique un descuento manual, deberá solicitar:

* Porcentaje o monto.
* Motivo.
* Usuario que autoriza.

---

## Paso 6: Retiro y entrega

La orden deberá permitir seleccionar:

* Recepción en local.
* Retiro a domicilio.

Y para la entrega:

* Retiro por el cliente.
* Entrega a domicilio.

Cuando corresponda, deberán registrarse:

* Dirección.
* Comuna.
* Fecha.
* Franja horaria.
* Conductor simulado.
* Costo de despacho.
* Instrucciones de entrega.

No se implementará una ruta real, pero la interfaz deberá representar la planificación.

---

## Paso 7: Resumen económico

Mostrar:

* Subtotal de prendas.
* Recargos.
* Servicio express.
* Retiro.
* Despacho.
* Descuentos.
* Promociones.
* Impuestos si correspondiera.
* Total.
* Monto pagado.
* Saldo pendiente.

El total deberá actualizarse automáticamente cuando se agreguen prendas, servicios o descuentos.

---

## Paso 8: Pago

La orden deberá permitir:

* Sin pago inicial.
* Abono.
* Pago total.

Medios de pago simulados:

* Efectivo.
* Débito.
* Crédito.
* Transferencia.
* Pago en línea.
* Otro.

Al registrar un pago deberá mostrarse:

* Monto.
* Medio de pago.
* Fecha.
* Usuario.
* Saldo restante.

---

## Paso 9: Confirmar orden

Antes de guardar se deberá mostrar un resumen con:

* Cliente.
* Teléfono.
* Prendas.
* Servicios.
* Observaciones.
* Fecha comprometida.
* Tipo de entrega.
* Descuentos.
* Total.
* Monto pagado.
* Saldo.

Al confirmar se deberá generar:

* Número de OT ficticio.
* Código corto de seguimiento.
* Estado inicial.
* Comprobante visual.
* Botón de impresión simulada.
* Botón de envío por WhatsApp.
* Botón de envío por correo simulado.

---

# 10. Estados de la orden

Cada orden deberá tener un estado principal.

Estados sugeridos:

1. Ingresada.
2. Pendiente de retiro.
3. Recibida.
4. En clasificación.
5. En lavado.
6. En secado.
7. En planchado.
8. En control de calidad.
9. Lista.
10. En ruta.
11. Entregada.
12. Cancelada.

El sistema deberá mostrar:

* Estado actual.
* Fecha del último cambio.
* Usuario que realizó el cambio.
* Historial de estados.
* Próxima acción esperada.

No todas las órdenes deberán recorrer todos los estados.

Por ejemplo, una orden solo de planchado podrá omitir lavado y secado.

---

# 11. Listado de órdenes de trabajo

La pantalla deberá mostrar una tabla con:

* Número de OT.
* Cliente.
* Teléfono.
* Fecha de ingreso.
* Fecha comprometida.
* Estado.
* Total.
* Saldo.
* Tipo de entrega.
* Sucursal.
* Acciones.

## Filtros

* Número de OT.
* Cliente.
* Estado.
* Fecha de ingreso.
* Fecha de entrega.
* Con saldo pendiente.
* Atrasadas.
* Express.
* Retiro en local.
* Entrega a domicilio.
* Sucursal.

## Acciones rápidas

* Abrir orden.
* Cambiar estado.
* Registrar pago.
* Imprimir comprobante.
* Contactar por WhatsApp.
* Marcar como entregada.
* Cancelar.

Las órdenes atrasadas deberán destacarse visualmente.

---

# 12. Detalle de la orden

La pantalla de detalle deberá mostrar:

## Encabezado

* Número de OT.
* Estado.
* Cliente.
* Teléfono.
* Fecha de ingreso.
* Fecha comprometida.
* Sucursal.
* Trabajador responsable.

## Prendas

Listado completo con:

* Tipo.
* Servicio.
* Cantidad.
* Observaciones.
* Estado individual.
* Precio.
* Fotografías simuladas.

## Línea de tiempo

Mostrar cronológicamente:

* Creación de la orden.
* Pagos.
* Cambios de estado.
* Mensajes enviados.
* Observaciones agregadas.
* Entrega.

## Acciones

* Editar.
* Cambiar estado.
* Registrar pago.
* Agregar observación.
* Contactar cliente.
* Reimprimir comprobante.
* Marcar como lista.
* Marcar como entregada.
* Cancelar.

---

# 13. Comunicación por WhatsApp

La demo no se integrará realmente con WhatsApp.

Deberá simular la generación de mensajes mediante enlaces `wa.me` o una ventana modal.

## Plantillas sugeridas

### Orden recibida

> Hola, {{nombre}}. Recibimos tu orden {{numeroOrden}}. La fecha estimada de entrega es {{fechaEntrega}}.

### Orden lista

> Hola, {{nombre}}. Tu orden {{numeroOrden}} ya está lista para retiro.

### Entrega en camino

> Hola, {{nombre}}. Tu pedido {{numeroOrden}} se encuentra en camino.

### Pago pendiente

> Hola, {{nombre}}. Tu orden {{numeroOrden}} tiene un saldo pendiente de {{saldo}}.

### Orden atrasada

> Hola, {{nombre}}. Te informamos que tu orden {{numeroOrden}} presenta una demora. La nueva fecha estimada es {{fechaEntrega}}.

### Promoción

> Hola, {{nombre}}. Tenemos una promoción disponible para tu próxima visita: {{promocion}}.

Antes de abrir WhatsApp, el trabajador deberá poder:

* Seleccionar una plantilla.
* Revisar el mensaje.
* Editar el contenido.
* Confirmar el envío simulado.

El historial de la orden deberá registrar que el contacto fue iniciado.

---

# 14. Gestión de servicios y precios

La pantalla deberá permitir visualizar un catálogo de servicios.

Cada servicio deberá incluir:

* Nombre.
* Categoría.
* Tipo de prenda.
* Precio.
* Unidad de cobro.
* Duración estimada.
* Estado activo o inactivo.
* Permite express.
* Recargo express.
* Observaciones.

Unidades posibles:

* Por prenda.
* Por kilogramo.
* Por metro cuadrado.
* Por par.
* Precio fijo.

La demo deberá permitir simular:

* Crear servicio.
* Editar precio.
* Activar o desactivar.
* Buscar.
* Filtrar por categoría.

---

# 15. Gestión de promociones

La pantalla deberá mostrar:

* Promociones activas.
* Promociones futuras.
* Promociones vencidas.
* Cantidad de usos.
* Ventas asociadas.
* Estado.

Cada promoción deberá incluir:

* Nombre.
* Código.
* Descripción.
* Fecha de inicio.
* Fecha de término.
* Tipo de descuento.
* Valor.
* Servicios aplicables.
* Prendas aplicables.
* Monto mínimo.
* Segmento de clientes.
* Máximo de usos.
* Combinable con otras promociones.
* Estado.

Tipos de promoción:

* Porcentaje.
* Monto fijo.
* Precio especial.
* Producto o servicio gratis.
* Cantidad mínima.
* Cliente frecuente.
* Primera compra.
* Convenio.

---

# 16. Caja diaria

La demo deberá incluir una pantalla de caja con:

* Estado de caja.
* Monto de apertura.
* Ingresos.
* Egresos.
* Pagos por medio.
* Pagos pendientes.
* Total esperado.
* Total contado.
* Diferencia.

## Movimientos

Cada movimiento deberá mostrar:

* Fecha y hora.
* Tipo.
* OT asociada.
* Concepto.
* Medio de pago.
* Monto.
* Usuario.

Acciones simuladas:

* Abrir caja.
* Registrar ingreso.
* Registrar egreso.
* Cerrar caja.
* Ver resumen.
* Imprimir cierre.

---

# 17. Retiros y entregas

La pantalla deberá mostrar una agenda diaria.

Cada visita deberá incluir:

* Tipo: retiro o entrega.
* Cliente.
* Dirección.
* Franja horaria.
* OT.
* Conductor.
* Estado.
* Teléfono.
* Instrucciones.

Estados sugeridos:

* Pendiente.
* Confirmada.
* Asignada.
* En camino.
* Completada.
* No realizada.

La demo deberá permitir:

* Filtrar por fecha.
* Filtrar por conductor.
* Asignar conductor.
* Cambiar estado.
* Contactar al cliente.
* Visualizar una ruta ficticia.

---

# 18. Reportes

La demo deberá incluir indicadores visuales básicos.

## Reportes sugeridos

* Ventas por día.
* Ventas por período.
* Órdenes por estado.
* Órdenes atrasadas.
* Pagos pendientes.
* Servicios más vendidos.
* Prendas más frecuentes.
* Clientes con mayor facturación.
* Promociones más utilizadas.
* Ventas por medio de pago.
* Ventas por sucursal.

Los gráficos pueden utilizar datos estáticos y no requieren librerías externas.

---

# 19. Búsqueda global

La cabecera deberá incluir una búsqueda que permita encontrar:

* Órdenes por número.
* Clientes por nombre.
* Clientes por teléfono.
* Servicios.
* Promociones.

Los resultados deberán agruparse por tipo.

---

# 20. Diseño visual

La interfaz debe parecer un software de trabajo, no una landing comercial.

Debe priorizar:

* Rapidez.
* Legibilidad.
* Densidad moderada de información.
* Acciones frecuentes visibles.
* Estados reconocibles.
* Tablas fáciles de escanear.
* Uso eficiente en pantallas de escritorio.
* Navegación usable en tablet.

## Lineamientos

* Menú lateral persistente.
* Cabecera superior.
* Fondo neutro.
* Tarjetas para indicadores.
* Tablas para operación.
* Modales para acciones rápidas.
* Formularios compactos.
* Colores de estado consistentes.
* Botón primario claramente identificable.
* Mensajes de éxito y error visibles.
* No depender únicamente del color.

---

# 21. Pantallas mínimas de la demo

La demo deberá incluir al menos:

1. Dashboard.
2. Listado de órdenes.
3. Nueva orden.
4. Detalle de orden.
5. Listado de clientes.
6. Ficha de cliente.
7. Servicios y precios.
8. Promociones.
9. Caja diaria.
10. Retiros y entregas.
11. Reportes.

No todas las pantallas necesitan lógica completa, pero deben ser navegables y visualmente coherentes.

---

# 22. Datos demo obligatorios

La demo deberá incluir:

* Al menos 15 clientes.
* Al menos 20 órdenes.
* Al menos 15 tipos de prenda.
* Al menos 10 servicios.
* Al menos 5 promociones.
* Al menos 4 medios de pago.
* Órdenes en diferentes estados.
* Órdenes atrasadas.
* Clientes con saldo pendiente.
* Clientes frecuentes.
* Retiros y entregas programados.
* Historiales de estados y comunicaciones.

---

# 23. Estructura sugerida

```text
laundry-management-demo/
├── index.html
├── pages/
│   ├── dashboard.html
│   ├── orders.html
│   ├── order-create.html
│   ├── order-detail.html
│   ├── customers.html
│   ├── customer-detail.html
│   ├── services.html
│   ├── promotions.html
│   ├── cash-register.html
│   ├── deliveries.html
│   └── reports.html
├── styles/
│   ├── variables.css
│   ├── layout.css
│   ├── components.css
│   ├── forms.css
│   ├── tables.css
│   └── styles.css
├── scripts/
│   ├── app.js
│   ├── router.js
│   ├── store.js
│   ├── orders.js
│   ├── customers.js
│   ├── promotions.js
│   ├── whatsapp.js
│   └── mock-data.js
├── assets/
│   ├── icons/
│   └── images/
├── README.md
└── AGENTS.md
```

Una implementación tipo SPA sin framework también es válida.

---

# 24. Archivo `AGENTS.md`

Debe incluir:

* Objetivo del producto.
* Usuarios.
* Flujos críticos.
* Reglas de negocio.
* Estructura del repositorio.
* Convenciones HTML, CSS y JavaScript.
* Modelo de datos simulado.
* Estados válidos de una orden.
* Criterios de aceptación.
* Instrucciones de ejecución.
* Checklist visual.
* Prohibición de introducir backend.
* Prohibición de cambiar reglas sin documentarlo.
* Obligación de mantener datos mock centralizados.
* Obligación de revisar consola y navegación.

---

# 25. Criterios de aceptación

## CA-01: Crear orden

**Dado** un trabajador en la pantalla de nueva orden
**Cuando** selecciona un cliente, agrega prendas y confirma
**Entonces** se debe generar una OT ficticia con número, total y estado inicial.

## CA-02: Agregar varias prendas

**Dado** que se está creando una orden
**Cuando** el trabajador agrega diferentes prendas
**Entonces** cada una debe mantener servicio, precio y observaciones independientes.

## CA-03: Registrar daño previo

**Dado** que una prenda presenta un daño
**Cuando** el trabajador lo registra
**Entonces** la observación debe aparecer en el resumen y detalle de la orden.

## CA-04: Aplicar promoción

**Dado** que una orden cumple las condiciones de una promoción
**Cuando** el trabajador la aplica
**Entonces** el descuento debe reflejarse en el total.

## CA-05: Registrar abono

**Dado** que el cliente paga parcialmente
**Cuando** se registra el abono
**Entonces** la orden debe mostrar el monto pagado y saldo pendiente.

## CA-06: Cambiar estado

**Dado** una orden existente
**Cuando** el trabajador cambia su estado
**Entonces** el nuevo estado debe verse en el listado y registrarse en el historial.

## CA-07: Contactar por WhatsApp

**Dado** una orden con teléfono válido
**Cuando** el trabajador selecciona una plantilla
**Entonces** debe mostrarse un mensaje editable antes de abrir el enlace simulado.

## CA-08: Detectar atraso

**Dado** una orden cuya fecha comprometida ya pasó
**Cuando** se visualiza el listado
**Entonces** debe marcarse como atrasada.

## CA-09: Consultar cliente

**Dado** un cliente registrado
**Cuando** se abre su ficha
**Entonces** deben mostrarse sus datos, historial, órdenes activas y saldo.

## CA-10: Cerrar caja

**Dado** que la caja está abierta
**Cuando** el trabajador registra el monto contado
**Entonces** debe mostrarse la diferencia respecto al monto esperado.

## CA-11: Persistir la demo

**Dado** que el trabajador crea o modifica datos
**Cuando** recarga el navegador
**Entonces** la información deberá conservarse si se utiliza `localStorage`.

## CA-12: Navegación completa

**Dado** cualquier módulo principal
**Cuando** el trabajador utiliza el menú lateral
**Entonces** debe poder acceder al resto de las pantallas sin enlaces rotos.

---

# 26. Fuera de alcance

No se implementará:

* Backend.
* Autenticación.
* Roles reales.
* Facturación electrónica.
* Integración Transbank.
* Integración bancaria.
* WhatsApp Business API.
* Notificaciones push.
* GPS.
* Optimización matemática de rutas.
* Aplicación móvil.
* Impresión física.
* Control de inventario real.
* Gestión de maquinaria.
* Firma electrónica.
* Integración tributaria.
* Multiempresa real.
* Sincronización cloud.
* Procesamiento de fotografías.
* Portal real del cliente.

---

# 27. Definition of Done

La demo se considera terminada cuando:

* El trabajador puede crear una OT completa.
* Se pueden agregar varias prendas.
* Se pueden registrar daños y observaciones.
* Los precios se calculan automáticamente.
* Se puede aplicar una promoción.
* Se puede registrar un abono o pago.
* Se puede cambiar el estado de una orden.
* Existe historial de la orden.
* Se puede generar un mensaje de WhatsApp.
* Se pueden consultar clientes.
* Se puede visualizar caja y reportes.
* Todas las pantallas mínimas son navegables.
* El diseño funciona en escritorio y tablet.
* No existen errores visibles en consola.
* No hay enlaces principales rotos.
* Existe `README.md`.
* Existe `AGENTS.md`.
* Los datos simulados están centralizados.
* Se recorrió manualmente el flujo de creación, procesamiento, pago y entrega.

---

# 28. Prompt inicial para el agente

Construye una demo HTML navegable para la gestión interna de una lavandería siguiendo estrictamente el requerimiento del repositorio.

La prioridad es el flujo operacional del trabajador:

1. Buscar o registrar un cliente.
2. Crear una orden de trabajo.
3. Agregar prendas y servicios.
4. Registrar daños u observaciones.
5. Aplicar promociones.
6. Registrar pagos.
7. Actualizar el estado.
8. Contactar al cliente por WhatsApp.
9. Entregar la orden.

Antes de implementar:

* Revisa todo el requerimiento.
* Define el modelo de datos mock.
* Propón la estructura de navegación.
* Identifica componentes reutilizables.
* Implementa primero el flujo completo de una OT.
* Implementa luego los módulos complementarios.
* No agregues backend.
* No agregues frameworks sin justificación.
* No copies la identidad visual de EasyLaundry.
* No declares la tarea completa sin probar el flujo de punta a punta.

Ante decisiones visuales no especificadas, prioriza velocidad operativa, claridad y baja cantidad de clics.

