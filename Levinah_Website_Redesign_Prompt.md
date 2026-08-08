# Agent Prompt — Redesign index.html for Levinah Unisex Salon & Makeup Studio

Redesign the existing `index.html` for **Levinah Unisex Salon & Makeup Studio**.
This is **NOT** a rebuild from scratch — restyle and restructure the current
file's proven layout, sections, and functionality to fit Levinah's brand
instead of the current "Stuwie's Salon & Spa" branding.

---

## Reference Files

- `assets/images/Levinah_Menu_Extracted.md` — full service list, prices (UGX),
  and brand colors. Use this as the single source of truth for all service
  categories, service names, pricing, and the color palette.
- `assets/images/` — contains the Levinah logo and other brand images. Use
  these images throughout the site (hero, about, service sections) instead
  of the current placeholder/Stuwie images. Do not invent image paths — only
  reference files that actually exist in `assets/images`.

---

## Branding Changes

- Replace all "Stuwie's Salon & Spa" text, meta tags, alt text, and page
  title with "Levinah Unisex Salon & Makeup Studio."
- Replace the blue/warm color scheme (`--blue`, `--blue-bright`, `--warm`,
  etc.) with Levinah's palette from the `.md` file (deep magenta/berry,
  maroon/wine, blush pink background, gold highlight accent).
- Swap the favicon/logo references to the Levinah logo in `assets/images`.
- Update the address/contact section to Bunamwaya, Sseguku, Wakiso District,
  WhatsApp 0703 878 921, call 0787 444 791.
- Rebuild the services section(s) to match the categories and structure in
  the `.md` file: Ladies Hair Services, Makeup Services, Bridal Packages,
  Nail Services, Barber Services, Kids Services, Beauty Services, Additional
  Services. Keep prices exactly as listed (ranges where given).

---

## Features to Remove

- Full booking system internals: booking cart, date/time picker, GPS
  location capture, form submission to Google Apps Script/webhook, and
  confirmation modal JS — replace the underlying flow with a direct WhatsApp
  link (see "WhatsApp Booking" below).
- Testimonials section.
- Google Reviews integration/section.
- Shop section/page/link — Levinah does not sell products online through
  this site.
- `services.html` link/page — do not reference or link to a separate
  services page; all services should live within `index.html` only.

---

## WhatsApp Booking (Keep This)

- Keep booking as a **WhatsApp-based flow** — button label and general
  UX can stay "Book via WhatsApp" or similar.
- Point it at Levinah's WhatsApp number (0703 878 921) with a pre-filled
  message including the selected service name.
- No in-site booking form, backend, or webhook is needed — this is a
  simple `wa.me` link with a pre-filled message per service/category.

---

## Features to Keep / Preserve

- Overall modern layout structure, responsive design, scroll animations,
  and header behavior (transparent-to-solid on scroll).
- SEO: keep meta description, title tags, semantic HTML, and update all
  copy/keywords to reflect Levinah's services and Wakiso/Nansana-area
  local SEO instead of Stuwie's.
- Add a **Professional Training Programs** section from the `.md` file,
  since it doesn't exist in the current template (new layout needed, not
  a restyle of an existing section).
- Add the **Important Notes** section (bring-your-own-braids policy,
  bridal booking advance notice, weekend/holiday booking notice).

---

## Deliverable

A single self-contained `index.html` (inline CSS/JS as in the original)
reflecting Levinah's brand, services, and pricing, with the booking system
internals, testimonials, Google Reviews, Shop, and `services.html` link
stripped out, and a WhatsApp-based booking flow in their place.

---

## Open Item to Confirm Before Build

- The service menu has a duplicate entry numbered **#27** ("Retouch with
  Hair Gel Styling" appears twice — once at 70,000 and once at
  80,000–120,000 with extensions). Confirm the correct service names with
  Levinah before the agent bakes this into the site's service-select logic.
