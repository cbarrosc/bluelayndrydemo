# Blue Laundry — Design Brief

<!-- impeccable:design-schema 1 -->

## Visitor Mode

Landing → Persuade · Order flow → Operate

## Job and Audience

End consumers arrive at the site needing laundry service without going to a physical location. They are likely busy, at home, or at work, and want to understand the service, estimate cost, and complete a request quickly and confidently. Trust in garment care is a key emotional requirement.

## Outcome and Proof

The visitor completes a full laundry service request — from landing to confirmed order — and walks away with a clear sense of how the service works, what it costs, and that their garments will be well cared for. Success is a visible confirmation screen with an order number.

## Selected Direction

**Visual authority:** Blue palette as primary — communicates cleanliness, freshness, and trust. White/light background, generous whitespace, soft card borders, sans-serif typography. Modern but not overly corporate.

**Structure:** Single-page site with dynamic sections. The landing page (hero, how-it-works, services, benefits, testimonials, FAQs, footer) scrolls vertically. The order flow uses a stepper/wizard with numbered steps: (1) select service, (2) schedule pickup, (3) contact info, (4) review & confirm, (5) success screen. The stepper replaces the main content area when active.

**Sequence:** Landing → CTA triggers order flow → step through wizard → confirmation screen → option to return to landing or view simulated tracking.

**Focal moments:**
- Hero headline and primary CTA ("Solicitar lavandería")
- Service selection cards with price visibility
- Order summary before final confirmation
- Confirmation screen with order number + next steps

## Scope and Boundaries

- Fidelity: Fully styled, responsive HTML/CSS demo with vanilla JS interactions
- Breadth: Full flow from landing through confirmation
- Interactivity: Form validation, step navigation, simulated loading, state persistence during session
- One HTML file with embedded CSS and JS, or a minimal file structure (index.html + styles/ + scripts/) — agent decision
- Must explicitly state it is a demo
- No backend, auth, payments, APIs, frameworks, or real data

## States and Ranges

- Services: 4 items (wash-fold, delicate, ironing, bedding) with mock prices in CLP
- Communes: mock list of ~10 Santiago communes
- Time windows: morning, afternoon, evening
- Weight input range: 1–20 kg for per-kilo service
- Order number: fictional format (BL-XXXXXX)
- Tracking: simulated 4-status progress

## Interaction and Layout

- **Hierarchy:** Landing hero is the strongest visual entry point. Stepper steps are clearly numbered with current step highlighted. Summary is read-only with edit affordance.
- **Topology:** Wizard replaces landing content. Sticky header with light branding persists. Footer visible after flow completes.
- **Responsiveness:** Stack cards/fields to single column on mobile. Stepper compresses to numbered dots. Full-width touch targets on small screens.
- **Affordances:** Buttons are clearly buttons (background, padding, hover). Selected service has a distinct border/check. Form fields have visible labels and focus rings.
- **Feedback:** Simulated loading spinner on "confirm." Inline validation errors. Smooth step transitions. Success state is celebratory but not overdone.
- **Animations:** Subtle — card hover scale, fade between wizard steps, smooth scroll to sections. No gratuitous motion.

## Constraints and Open Decisions

- Platform: web (static, vanilla)
- Accessibility: per WCAG minimum — labels, keyboard nav, focus states, alt text, contrast, headings
- No external fonts unless loaded from CDN (Google Fonts is acceptable)
- Decisions the builder may make: exact blue hex values, font-family stack, icon style (inline SVG or simple unicode/emoji), card layout, spacing scale, animation timing, mock testimonial copy
- The brand name "Blue Laundry" must appear in the header
- "EasyLaundry" must not appear in copy or visual identity
