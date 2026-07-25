# Requerimiento: Demo HTML de plataforma de lavandería

## 1. Objetivo

Construir una demo navegable en HTML de una plataforma digital de lavandería a domicilio, inspirada funcionalmente en EasyLaundry.

La demo debe permitir visualizar el flujo principal de un cliente que:

1. Selecciona un servicio de lavandería.
2. Define retiro y entrega.
3. Ingresa sus datos de contacto.
4. Revisa el resumen de su solicitud.
5. Simula la confirmación de una orden.

El objetivo no es implementar una aplicación productiva, sino validar la experiencia de usuario, la jerarquía visual y el flujo de contratación mediante un prototipo frontend.

---

## 2. Alcance

La solución deberá desarrollarse como un sitio estático compuesto por:

* HTML semántico.
* CSS.
* JavaScript vanilla opcional para interacciones simples.
* Datos simulados.
* Sin backend.
* Sin base de datos.
* Sin autenticación real.
* Sin integración de pagos.
* Sin consumo de APIs externas.

La demo debe poder ejecutarse abriendo directamente el archivo `index.html` o mediante un servidor estático local.

---

## 3. Enfoque de programación agéntica

El proyecto debe estar diseñado para ser implementado principalmente por agentes de desarrollo.

Para facilitar este enfoque:

* Cada sección debe tener responsabilidades claramente delimitadas.
* Los componentes visuales deben ser independientes y reutilizables.
* El contenido debe mantenerse separado de la estructura cuando sea razonable.
* Las decisiones visuales deben documentarse en un archivo breve.
* Los criterios de aceptación deben ser verificables visualmente.
* No se deben incorporar dependencias innecesarias.
* Los agentes pueden tomar decisiones menores de diseño siempre que respeten los requerimientos funcionales y visuales.

El agente deberá privilegiar una implementación simple, clara y fácil de modificar por sobre una arquitectura sobredimensionada.

---

## 4. Usuario objetivo

Persona que necesita enviar ropa a una lavandería sin trasladarse físicamente al local.

El usuario espera:

* Entender rápidamente cómo funciona el servicio.
* Conocer los tipos de lavado disponibles.
* Estimar el costo.
* Coordinar retiro y entrega.
* Completar la solicitud con pocos pasos.
* Sentir confianza respecto al cuidado de sus prendas.

---

## 5. Flujo principal

### Paso 1: Landing page

El usuario ingresa al sitio y visualiza:

* Encabezado con logotipo ficticio.
* Navegación principal.
* Mensaje comercial.
* Botón principal: `Solicitar lavandería`.
* Imagen o ilustración relacionada con ropa limpia o retiro a domicilio.
* Resumen visual del funcionamiento del servicio.

La llamada principal a la acción debe llevar al formulario de solicitud.

---

### Paso 2: Selección de servicio

El usuario debe poder seleccionar uno de los siguientes servicios simulados:

#### Lavado por kilo

Incluye lavado, secado y doblado de ropa cotidiana.

#### Lavado delicado

Para prendas que requieren cuidados especiales.

#### Planchado

Servicio de planchado por prenda.

#### Lavado de ropa de cama

Para sábanas, fundas, cubrecamas y artículos similares.

Cada tarjeta de servicio debe mostrar:

* Nombre.
* Descripción breve.
* Precio referencial.
* Tiempo estimado.
* Botón o selector.

Los precios son únicamente demostrativos.

---

### Paso 3: Programación de retiro

El usuario debe ingresar o seleccionar:

* Dirección.
* Comuna.
* Fecha de retiro.
* Franja horaria.
* Fecha estimada de entrega.
* Instrucciones adicionales.

No es necesario validar cobertura real.

Las comunas pueden presentarse como una lista simulada.

---

### Paso 4: Datos del cliente

El formulario debe solicitar:

* Nombre.
* Apellido.
* Correo electrónico.
* Teléfono.
* Dirección.
* Observaciones opcionales.

Los campos obligatorios deben indicarse visualmente.

---

### Paso 5: Resumen de la orden

Antes de confirmar, el usuario debe visualizar:

* Servicio seleccionado.
* Cantidad o peso estimado.
* Precio referencial.
* Dirección de retiro.
* Fecha y horario.
* Datos de contacto.
* Observaciones.
* Total estimado.

El usuario debe poder volver a modificar la información.

---

### Paso 6: Confirmación simulada

Al confirmar la solicitud se debe mostrar una pantalla de éxito con:

* Mensaje de confirmación.
* Número de orden ficticio.
* Fecha de retiro.
* Resumen breve.
* Botón para volver al inicio.
* Botón para simular el seguimiento de la orden.

No se debe enviar información a ningún servidor.

---

## 6. Secciones de la landing page

La página principal deberá incluir las siguientes secciones.

### Encabezado

* Logo ficticio.
* Inicio.
* Servicios.
* Cómo funciona.
* Preguntas frecuentes.
* Botón `Solicitar retiro`.

### Hero

* Título comercial.
* Texto explicativo.
* Llamada principal a la acción.
* Llamada secundaria para conocer el proceso.
* Ilustración o composición visual.

Ejemplo de mensaje:

> Tu ropa limpia, seca y doblada sin salir de casa.

### Cómo funciona

Mostrar el proceso en tres o cuatro pasos:

1. Agenda el retiro.
2. Entrega tu ropa.
3. Procesamos tus prendas.
4. Recíbela limpia en tu domicilio.

### Servicios

Mostrar tarjetas para los servicios disponibles.

### Beneficios

Incluir beneficios como:

* Retiro y entrega a domicilio.
* Cuidado especializado.
* Precios transparentes.
* Seguimiento del pedido.
* Atención personalizada.

### Testimonios

Mostrar entre dos y tres testimonios ficticios.

Estos deben estar claramente tratados como contenido demostrativo.

### Preguntas frecuentes

Incluir preguntas como:

* ¿Cuánto demora el servicio?
* ¿Cómo se calcula el precio?
* ¿Qué prendas no se reciben?
* ¿Puedo modificar el horario?
* ¿Qué ocurre si una prenda requiere cuidado especial?

### Footer

Incluir:

* Enlaces de navegación.
* Información de contacto ficticia.
* Redes sociales ficticias.
* Términos y condiciones.
* Política de privacidad.
* Indicación de que se trata de una demo.

---

## 7. Estados visuales requeridos

La demo debe contemplar:

* Estado inicial.
* Hover de botones y tarjetas.
* Servicio seleccionado.
* Campo enfocado.
* Campo con error.
* Botón deshabilitado.
* Carga simulada.
* Orden confirmada.
* Vista vacía o sin selección.
* Mensaje de validación.

---

## 8. Diseño visual

El diseño debe comunicar:

* Limpieza.
* Confianza.
* Rapidez.
* Simplicidad.
* Cuidado de las prendas.

### Lineamientos sugeridos

* Fondo principalmente claro.
* Espacios amplios.
* Tarjetas con bordes suaves.
* Tipografía sans serif.
* Iconografía sencilla.
* Un color principal asociado a limpieza o frescura.
* Un color de énfasis para las llamadas a la acción.
* Contraste suficiente para lectura.
* Diseño moderno, pero no excesivamente corporativo.

No se debe replicar exactamente el logotipo, textos, fotografías, tipografías ni identidad gráfica de EasyLaundry.

---

## 9. Diseño responsive

La demo debe funcionar correctamente en:

* Escritorio.
* Tablet.
* Dispositivo móvil.

En dispositivos móviles:

* La navegación puede transformarse en menú desplegable.
* Las tarjetas deben mostrarse en una columna.
* Los botones principales deben ocupar el ancho disponible.
* El formulario debe mantener campos legibles y utilizables.
* No debe existir desplazamiento horizontal.

---

## 10. Accesibilidad mínima

La implementación debe incluir:

* Etiquetas `label` asociadas a los campos.
* Navegación mediante teclado.
* Estados de foco visibles.
* Textos alternativos en imágenes.
* Contraste legible.
* Uso correcto de encabezados.
* Botones reales para acciones.
* Mensajes de error comprensibles.
* Uso limitado y justificado de atributos ARIA.

---

## 11. Estructura sugerida del proyecto

```text
easy-laundry-demo/
├── index.html
├── order.html
├── confirmation.html
├── styles/
│   ├── reset.css
│   ├── variables.css
│   ├── components.css
│   └── styles.css
├── scripts/
│   ├── app.js
│   ├── order-form.js
│   └── mock-data.js
├── assets/
│   ├── images/
│   └── icons/
├── README.md
└── AGENTS.md
```

La separación en múltiples páginas es sugerida. También se permite una única página con secciones dinámicas si la implementación resulta más simple.

---

## 12. Archivo `AGENTS.md`

El proyecto deberá incluir un archivo `AGENTS.md` con instrucciones para futuros agentes.

Debe contener como mínimo:

* Objetivo del proyecto.
* Alcance y restricciones.
* Estructura de archivos.
* Convenciones de nombres.
* Cómo ejecutar la demo.
* Qué partes pueden modificarse libremente.
* Qué decisiones deben conservarse.
* Checklist de validación.
* Prohibición de agregar backend o dependencias sin justificación.
* Instrucción de revisar visualmente escritorio y móvil antes de finalizar.

---

## 13. Decisiones permitidas al agente

El agente podrá decidir:

* Paleta de colores.
* Tipografía.
* Espaciados.
* Iconografía.
* Distribución exacta de las tarjetas.
* Contenido comercial ficticio.
* Nombres de clases CSS.
* Uso de una o varias páginas.
* Uso moderado de animaciones.
* Ilustraciones o imágenes de stock libres.

El agente no podrá:

* Eliminar pasos del flujo principal.
* Incorporar autenticación real.
* Incorporar pagos reales.
* Incorporar un backend.
* Copiar la identidad visual de EasyLaundry.
* Introducir frameworks sin necesidad.
* Ocultar errores de formulario.
* Declarar integraciones que no existen.

---

## 14. Datos simulados

El sistema debe utilizar datos estáticos para:

* Servicios.
* Precios.
* Comunas.
* Horarios disponibles.
* Testimonios.
* Preguntas frecuentes.
* Número de orden.
* Estado de seguimiento.

Ejemplo de servicios:

```javascript
const services = [
  {
    id: "wash-fold",
    name: "Lavado por kilo",
    description: "Lavado, secado y doblado de ropa cotidiana.",
    price: 4990,
    unit: "kg",
    estimatedTime: "48 horas"
  },
  {
    id: "delicate",
    name: "Lavado delicado",
    description: "Cuidado especial para prendas sensibles.",
    price: 7990,
    unit: "prenda",
    estimatedTime: "72 horas"
  }
];
```

---

## 15. Validaciones mínimas

El formulario debe validar:

* Nombre obligatorio.
* Correo con formato válido.
* Teléfono obligatorio.
* Dirección obligatoria.
* Servicio seleccionado.
* Fecha de retiro seleccionada.
* Horario seleccionado.
* Cantidad o peso mayor que cero.
* Aceptación de términos antes de confirmar.

Las validaciones deben ejecutarse en el frontend.

---

## 16. Criterios de aceptación

### CA-01: Visualización de landing

**Dado** que el usuario abre `index.html`
**Cuando** la página termina de cargar
**Entonces** debe visualizar el encabezado, hero, servicios, proceso, beneficios, preguntas frecuentes y footer.

### CA-02: Navegación hacia la solicitud

**Dado** que el usuario se encuentra en la landing
**Cuando** presiona `Solicitar lavandería`
**Entonces** debe visualizar el flujo de creación de una orden.

### CA-03: Selección de servicio

**Dado** que el usuario visualiza los servicios
**Cuando** selecciona una tarjeta
**Entonces** la tarjeta debe mostrar un estado visual seleccionado y actualizar el resumen.

### CA-04: Validación del formulario

**Dado** que existen campos obligatorios incompletos
**Cuando** el usuario intenta continuar
**Entonces** deben mostrarse mensajes de error junto a los campos correspondientes.

### CA-05: Resumen de la orden

**Dado** que el usuario completó los datos mínimos
**Cuando** avanza al resumen
**Entonces** debe visualizar correctamente el servicio, fechas, dirección y total estimado.

### CA-06: Edición de información

**Dado** que el usuario está en el resumen
**Cuando** selecciona la opción para modificar los datos
**Entonces** debe regresar al formulario manteniendo la información previamente ingresada.

### CA-07: Confirmación simulada

**Dado** que el usuario acepta el resumen
**Cuando** confirma la solicitud
**Entonces** debe mostrarse una pantalla de éxito con un número de orden ficticio.

### CA-08: Persistencia temporal

**Dado** que el usuario avanza entre pasos
**Cuando** vuelve a una etapa anterior
**Entonces** la información ingresada debe conservarse durante la sesión actual del navegador.

### CA-09: Diseño responsive

**Dado** que la página se visualiza en una pantalla móvil
**Cuando** el ancho disponible sea reducido
**Entonces** el contenido debe adaptarse sin producir desplazamiento horizontal.

### CA-10: Ejecución local

**Dado** que el repositorio fue descargado
**Cuando** el usuario abre `index.html` o levanta un servidor estático
**Entonces** la demo debe funcionar sin instalaciones adicionales obligatorias.

---

## 17. Definition of Done

El requerimiento se considera completado cuando:

* El flujo completo puede recorrerse desde la landing hasta la confirmación.
* Los datos utilizados son simulados.
* El formulario valida los campos obligatorios.
* El diseño funciona en escritorio y móvil.
* No existen errores visibles en la consola.
* No existe desplazamiento horizontal.
* Los botones y enlaces principales funcionan.
* El código está organizado y es legible.
* Existe un `README.md`.
* Existe un `AGENTS.md`.
* Se incluyen instrucciones para ejecutar la demo.
* Se ejecutó una revisión visual de todas las páginas.
* Se comprobó navegación mediante teclado.
* Se dejó explícito que el proyecto es una demo y no un servicio real.

---

## 18. Fuera de alcance

No se implementarán:

* Registro o inicio de sesión.
* Integración con Google Maps.
* Geolocalización.
* Cálculo real de rutas.
* Disponibilidad real de repartidores.
* Pagos.
* Facturación.
* Notificaciones.
* Panel administrativo.
* Gestión logística.
* Seguimiento GPS.
* Base de datos.
* Backend.
* Integración con WhatsApp.
* Carga real de fotografías.
* Gestión de reclamos.
* Integración con una lavandería existente.

---

## 19. Instrucción inicial sugerida para el agente

Implementa una demo HTML responsive de una plataforma de lavandería a domicilio siguiendo el requerimiento del repositorio.

Antes de escribir código:

1. Revisa completamente el requerimiento.
2. Propón una estructura simple de páginas y componentes.
3. Identifica las decisiones visuales que tomarás.
4. Implementa primero el flujo funcional.
5. Agrega luego los estilos y estados visuales.
6. Verifica todos los criterios de aceptación.
7. No agregues backend, autenticación, pagos ni frameworks innecesarios.
8. Documenta cualquier decisión que no esté definida explícitamente.
9. Revisa el resultado tanto en escritorio como en móvil.
10. No declares la tarea terminada hasta recorrer manualmente el flujo completo.

