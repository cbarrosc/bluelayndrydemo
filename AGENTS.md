# Blue Laundry — Agentes

## Objetivo

Demo HTML navegable de una plataforma de lavandería a domicilio. Validar UX, jerarquía visual y flujo de contratación mediante un prototipo frontend.

## Alcance y restricciones

- Sitio estático: HTML + CSS + JavaScript vanilla
- Sin backend, base de datos, autenticación, pagos ni APIs externas
- Sin frameworks ni dependencias externas (salvo Google Fonts)
- Datos simulados (servicios, precios, comunas, horarios, testimonios, FAQs)
- Debe ejecutarse abriendo `index.html` directamente o con servidor estático local
- Debe indicar explícitamente que es una demo

## Estructura

```
blue_laundry/
  index.html      # Única página con todo el contenido y lógica
  PRODUCT.md      # Contexto de producto
  DESIGN.md       # Brief de diseño
  AGENTS.md       # Este archivo
```

## Convenciones

- CSS: variables en `:root`, clases BEM-lite, una sola hoja embebida en `<style>`
- JS: vanilla sin módulos, todo en un solo `<script>` al final del body
- Estado de la orden: objeto global `state` con persistencia en sesión
- Responsive: media queries en 1024px, 768px, 480px
- Colores: paleta azul definida en variables CSS (`--blue-*`)

## Cómo ejecutar

Abrir `index.html` en cualquier navegador moderno. También funciona con cualquier servidor estático (python -m http.server, npx serve, etc.)

## Partes modificables libremente

- Contenido comercial ficticio (testimonios, textos del hero, descripciones)
- Paleta exacta de azules (variables `--blue-*` en CSS)
- Íconos (emojis actuales, pueden cambiarse por SVG)
- Animaciones y transiciones

## Decisiones que deben conservarse

- Flujo completo: landing → wizard de 5 pasos → confirmación
- Estructura de una sola página con secciones dinámicas
- Stepper/wizard con pasos numerados
- Validación de formulario en cada paso
- Estado persistente durante la sesión
- Diseño responsivo
- Marca "Blue Laundry" en el header
- Los colores azules como primarios

## Checklist de validación

- [ ] Landing visible con header, hero, servicios, proceso, beneficios, FAQ, footer
- [ ] Botón "Solicitar lavandería" abre el wizard
- [ ] Servicios seleccionables con estado visual
- [ ] Validación de campos obligatorios con mensajes de error
- [ ] Resumen de orden con datos correctos
- [ ] Edición regresa al paso manteniendo datos
- [ ] Confirmación con número de orden ficticio
- [ ] Diseño funciona en móvil (sin scroll horizontal)
- [ ] Funciona abriendo index.html directamente
- [ ] Sin errores en consola del navegador
- [ ] Navegación por teclado funcional
- [ ] Contraste suficiente y estados de foco visibles
- [ ] Indicación visible de que es una demo

## Prohibiciones

- No agregar backend, base de datos, autenticación ni pagos
- No agregar frameworks sin justificación
- No copiar identidad visual de EasyLaundry
- No declarar integraciones que no existen
