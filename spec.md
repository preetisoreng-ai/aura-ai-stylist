# Aura Minimal Home — Architectural & Design Specification
**Artifact Path**: `minimal-home-2026-09-08/`  
**Creation Date**: `2026-09-08`  
**Design Reference**: `Screenshot 2026-09-08 204541.png`  
**Standard Compliance**: WCAG 2.1/2.2 AA (82/82 contrast pairings passed), Apple HIG Touch Targets (44pt+), Aura UX Design Specification v1.0

---

## 1. Executive Summary & Design Foundation
The **Aura Minimal Home** translates the minimalist visual reference from `Screenshot 2026-09-08 204541.png` into the luxury bespoke occasion-wear paradigm of Aura:
- **Design Principles**:
  1. *Occasion before object*: The home screen never shows product tiles or commercial grids. It opens purely with intent: *"What can I help you with today ?"*
  2. *Minimalist Elegance*: Generous whitespace, focused visual weight on the ethereal Aura Orb, and zero visual clutter.
  3. *Ask, then curate*: The AI front door acts as a conversational query builder, accepting free-text or voice input in English, Hindi, or Hinglish.
- **Design Tokens (Aura Verified)**:
  - **Canvas (surface-0)**: `#FBF8F3` (Ivory, 15.84:1 contrast with Ink)
  - **Surface (surface-1)**: `#FFFFFF` (Pristine White, 16.78:1 contrast with Ink)
  - **Inset (surface-2)**: `#F3EEE4` (Sand, 14.51:1 contrast with Ink)
  - **Primary**: `#3B2A5A` (Deep Royal Plum, 11.91:1 on Ivory)
  - **Accent**: `#C89B3C` (Warm Antique Gold, 5.85:1 for text `#785D24`)
  - **Text Ink**: `#1E1B2E` (Charcoal Plum)
  - **Muted**: `#5A5468` (Warm Ash, 6.83:1 on Ivory)

---

## 2. Component Geometry & Layout Mapping

| Element | Reference Screenshot | Aura Minimal Implementation |
| :--- | :--- | :--- |
| **Top Navigation** | Logo + "NoVa Ai", "Get Pro" pill, Hamburger circle `☰` | **Aura Emblem** (Plum ring + Gold core) + "Aura", **"Stylist Desk"** pill button, and circular menu opening the 5-tab primary IA drawer. |
| **Central Ethereal Orb** | Concentric green/mint glowing glass sphere | **Concentric Aura Orb**: Luminous 3D core in Royal Plum & Antique Gold with specular caustic reflection, concentric wave ripple ring, and ambient breathing bloom. |
| **Headline** | *"What can I help you with today ?"* | **Instrument Serif** display typography (36px, centered, editorial warmth). |
| **Chips** | 2 staggered rows of tech prompts | **Aura Occasion Taxonomy** (2 rows of pill chips with craft icons):<br>• Row 1: `💍 Wedding guest`, `🪔 Diwali festive`, `💃 Sangeet dance`<br>• Row 2: `🥂 Modern reception`, `🏛️ Temple morning`, `🏡 Griha Pravesh` |
| **Floating Bar** | Floating pill with mic icon | Pill container with white card elevation, `"Ask me anything"` placeholder, circular mic button in Sand (`#F3EEE4`) with Plum mic, and iOS home indicator. |

---

## 3. Information Architecture & Navigation
- **Primary IA (5 Tabs via Navigation Drawer)**:
  1. `01 · Home`: Intent-first landing (current minimal view).
  2. `02 · Discover`: Regional provenance, craft heritage, boutique stories.
  3. `03 · Design`: Active conversational workbench & stylist chat.
  4. `04 · Wardrobe`: Owned garments, measurement profiles, family members.
  5. `05 · Orders`: Live artisan production tracking & pre-dispatch approval.
- **Persistent Dual-Geography**:
  - Global Ship-to switchable between `🇺🇸 US $`, `🇬🇧 UK £`, `🇨🇦 CA $`, and `🇮🇳 INR ₹`.
  - Automatically recomputes landed duties, taxes, and feasible artisan lead times.

---

## 4. Accessibility Audit (`/mobile-access`)
- **Contrast**:
  - Normal text on Canvas: `15.84:1` (WCAG AA requires 4.5:1) — **PASS**
  - Muted text on Canvas: `6.83:1` (WCAG AA requires 4.5:1) — **PASS**
  - Interactive elements: All chip and button borders meet or exceed `3.0:1` — **PASS**
- **Touch Targets**:
  - All interactive chips: minimum `44px` height with comfortable tap margins.
  - Mic button: `36×36px` inside `44px` container hit area.
  - Menu button: `38×38px` inside `44px` container hit area.
- **Motion & Semantic Accessibility**:
  - Breathing animation respects `@media (prefers-reduced-motion: reduce)`.
  - All icon-only buttons include descriptive `aria-label` attributes.
