# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Primary users are individuals who need laundry service without visiting a physical location. They expect to understand the service quickly, know available wash types, estimate cost, coordinate pickup and delivery, and complete a request in few steps. They prioritize trust in garment care and convenience.

## Product Purpose

A navigable HTML demo of a laundry pickup-and-delivery platform, built to validate UX, visual hierarchy, and the booking flow via a frontend prototype. It is not a production application.

## Positioning

Inspirado funcionalmente en EasyLaundry, pero con identidad visual propia. La demo permite recorrer el flujo completo de contratación de un servicio de lavandería a domicilio: desde la landing hasta la confirmación de la orden, con datos simulados y sin backend.

## Operating Context

The demo runs entirely as a static site — HTML, CSS, and vanilla JavaScript — opened directly in a browser or served via a local static server. No backend, database, authentication, payments, or external APIs are involved. The user navigates a multi-step flow on a single page or across multiple pages. All data (services, prices, communes, testimonials, FAQs, order number) are mocked. The experience must work on desktop, tablet, and mobile without horizontal scroll.

## Capabilities and Constraints

**Confirmed capabilities:**
- Landing page with header, hero, services overview, how-it-works, benefits, testimonials, FAQs, and footer
- Service selection from four options: Lavado por kilo, Lavado delicado, Planchado, Lavado de ropa de cama
- Pickup scheduling (address, commune, date, time window, delivery estimate, instructions)
- Customer data form (name, email, phone, address, optional notes)
- Order summary with review and edit capability
- Simulated confirmation with fictional order number and basic tracking
- Frontend form validation (required fields, email format, service selected, date/time selected, quantity > 0, terms acceptance)
- Responsive design (desktop, tablet, mobile)
- Keyboard navigation, focus states, labeled form fields, accessible headings, alt text on images, sufficient contrast
- Simulated loading states, hover states, selected states, focus states, error states, disabled states, empty states

**Confirmed constraints:**
- No real backend, database, authentication, payments, or external APIs
- No Google Maps, geolocation, real routing, real courier availability
- No notifications, admin panel, logistics management, GPS tracking
- No WhatsApp integration, real photo upload, claims management
- No integration with any actual laundry business
- No copying EasyLaundry's logo, text, photos, typefaces, or graphic identity
- No frameworks without necessity
- Demo must be explicitly labelled as a demo, not a real service

## Brand Commitments

- Product name: Blue Laundry
- Visual direction communicates cleanliness, trust, speed, simplicity, and garment care
- Light background, generous whitespace, soft card borders, sans-serif typography, simple iconography
- Blue-based color palette as primary; emphasis color for calls-to-action
- Modern but not overly corporate aesthetic
- Palette, typography, spacing, iconography, exact card layout, commercial copy, class naming, animation decisions, and stock imagery are agent decisions within the above guidelines

## Evidence on Hand

- `REQUIREMENTS.md` at project root contains the full functional specification, acceptance criteria, visual guidelines, and data structure examples
- No real testimonials, case studies, customer data, brand assets, or design files exist
- The demo must clearly indicate it is a demonstrative prototype, not a real service

## Product Principles

1. **Flow completeness over polish.** Every step from landing to confirmation must work end-to-end; visual refinement comes after the functional chain is verified.
2. **One clear conversion path.** The interface steers the user toward requesting service without distractions or unnecessary choices.
3. **Trust through transparency.** Pricing, process, and service details are surfaced early; no hidden information.
4. **Simplicity as respect.** No feature, field, or step that the primary user's real job does not need. The demo exists to validate, not to impress with complexity.
5. **Resilient defaults.** Every mock data set, empty state, and error message is designed and present before the demo is shown — nothing is left to a blank screen or a broken flow.

## Accessibility & Inclusion

Implementation must include: `<label>` elements associated with form controls, keyboard-navigable interface, visible focus states, alt text on images, legible contrast, correct heading hierarchy, real `<button>` elements for actions, understandable error messages, and limited justified ARIA use.
