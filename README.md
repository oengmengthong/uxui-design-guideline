# 🚀 Universal Project Design Generator (Mobile + Web)

**Apple HIG + Material Design 3 Compliant**

A comprehensive design system guide following Apple Human Interface Guidelines and Material Design 3 standards. Use this every time you start a new project to ensure consistency, accessibility, and platform compliance.

**📖 View the interactive guide:** Open `design.html` in your browser for the full visual guide with live examples.

---

## 1️⃣ Project Design Setup (Mandatory)

Before design starts, always define:

*   **Project Type:** (Admin / Consumer App / Landing / SaaS)
*   **Platforms:** Android / iOS / Web
*   **Primary Users:** (Admin / Staff / Customer)
*   **Theme Style:** Clean / Modern / Corporate / Playful
*   **Primary Action:** (e.g. Create, Book, Pay, Track)
*   **Accessibility Target:** WCAG 2.1 AA (minimum)

👉 **No UI work until this is filled.**

---

## 2️⃣ Design Tokens (Global – must be reused)

### 🎨 Color System (Material Design 3 + iOS)

**Primary Colors:**
*   Primary (brand color)
*   Primary Container (light background)
*   Secondary (accent)
*   Secondary Container
*   Tertiary (optional accent)
*   Tertiary Container

**Surface & Background:**
*   Background (page background)
*   Surface (card background)
*   Surface Variant (subtle backgrounds)
*   Surface Dim / Bright (dark mode variants)

**Text & Icons:**
*   Text Primary (body text)
*   Text Secondary (supporting text)
*   Text Tertiary (disabled text)
*   Text Disabled (38% opacity)

**Semantic:**
*   Success / Success Container
*   Warning / Warning Container
*   Error / Error Container
*   Info / Info Container

**Rules:**
*   Background = neutral (white / light gray)
*   Primary color = actions only
*   Error/Success ONLY for status
*   Support light AND dark mode

### 🔤 Typography Scale

**Material Design 3:**
*   Display: Large (57px), Medium (45px), Small (36px)
*   Headline: Large (32px), Medium (28px), Small (24px)
*   Title: Large (22px), Medium (16px), Small (14px)
*   Body: Large (16px), Medium (14px), Small (12px)
*   Label: Large (14px), Medium (12px), Small (11px)

**iOS Reference:**
*   Large Title: 34pt
*   Title 1: 28pt → Maps to Headline Medium
*   Title 2: 22pt → Maps to Title Large
*   Body: 17pt → Maps to Body Large
*   Callout: 16pt
*   Subheadline: 15pt → Maps to Body Medium
*   Footnote: 13pt
*   Caption: 12pt/11pt → Maps to Label sizes

**Fonts:**
*   iOS: SF Pro Display/Text
*   Android: Roboto
*   Web: Inter, system-ui, sans-serif

### 📐 Spacing System (8pt Grid)

**All spacing MUST be multiples of 4px:**

`4 (XXS) / 8 (XS) / 12 (SM) / 16 (MD) / 24 (LG) / 32 (XL) / 48 (2XL) / 64 (3XL)`

❌ No random spacing • ❌ No odd numbers (except 4)

### 🔲 Border Radius Scale

*   XS: 4px (chips, tags)
*   Small: 8px (buttons, inputs)
*   Medium: 12px (cards)
*   Large: 16px (modals)
*   XL: 24px (hero cards)
*   Full: 9999px (pills, avatars, FAB)

**Rule:** Pick 2-3 sizes max per project (typically SM, MD, Full)

### 🔼 Elevation System (Material Design 3)

*   Level 0: No shadow (flat surface)
*   Level 1: Cards, search bars
*   Level 2: App bars, raised buttons
*   Level 3: FAB, snackbars
*   Level 4: Navigation drawer
*   Level 5: Dialogs, modals

**iOS:** Use lighter shadows, prefer borders over heavy elevation

---

## 3️⃣ Screen Structure Generator

Every screen must follow this structure:

```text
Safe Area (iOS: Status bar + Dynamic Island)
└── App Bar / Navigation Bar
    └── Height: 56dp (Android) / 44pt (iOS)
└── Content Area (Scrollable)
    └── Sections (24dp spacing)
        └── Cards / Lists / Forms
        └── Z-Index: 0 (base layer)
└── Primary Action (FAB or Button)
    └── Z-Index: 1200
└── Feedback Layer
    └── Loading: Skeleton or spinner (>400ms)
    └── Error: Inline or toast
    └── Empty: Illustration + text + action
└── Safe Area Inset Bottom (iOS: 34pt)
```

**iOS Safe Areas:**
*   Status bar: 44pt (47pt with Dynamic Island)
*   Bottom indicator: 34pt
*   Use `env(safe-area-inset-*)` in CSS

**Z-Index Scale:**
*   Base: 0
*   Dropdown: 1000
*   Sticky: 1100
*   Modal Backdrop: 1300
*   Modal: 1400
*   Tooltip: 1600

❌ No floating random elements • ❌ No overlapping interactive areas

---

## 4️⃣ Required Screens (Minimum Set)

Every project MUST include:

**Core**
*   Splash / Launch
*   Login / Auth (if required)
*   Main List / Dashboard
*   Detail Screen
*   Create / Edit Screen

**States**
*   Loading (Skeleton)
*   Empty State
*   Error State
*   Success Feedback

---

## 5️⃣ Component Library (Reusable)

Before designing screens, create these components with ALL states:

**Buttons (48dp height)**
*   Primary (filled, elevated)
*   Secondary (outlined)
*   Text (no background)
*   Danger (destructive actions)
*   FAB (56dp diameter)
*   Icon button (48dp touch target)
*   States: Default, Hover, Focus, Pressed, Disabled, Loading

**Inputs (48dp min height)**
*   Text field (outlined/filled)
*   Password (with show/hide)
*   Number, Email, Phone
*   Dropdown / Select
*   Search (with clear button)
*   Date picker
*   Checkbox, Radio, Switch
*   States: Default, Focus, Filled, Error, Success, Disabled

**Navigation**
*   Tab bar (56dp height, 3-5 items max)
*   Bottom navigation (Android)
*   Navigation drawer (256dp wide)
*   Navigation rail (80dp wide)
*   Breadcrumbs (web)

**Data Display**
*   Card (12-16dp radius, elevation 1)
*   List item (56dp single, 72dp two-line, 88dp three-line)
*   Data table (desktop only)
*   Chip (32dp height)
*   Badge (16-20dp)
*   Avatar (24/32/40/48dp)

**Feedback**
*   Dialog / Alert (280dp wide)
*   Bottom sheet (iOS modal sheets)
*   Toast / Snackbar (4-6s duration)
*   Progress bar (linear/circular)
*   Skeleton loader
*   Empty state

**Rule:** No custom component allowed unless approved by design lead

---

## 6️⃣ Iconography System

**Standard Icon Sizes:**
*   16px: XS (inline icons)
*   20px: Small
*   24px: **Default** (most common)
*   32px: Large
*   48px: Hero

**Guidelines:**
*   Icon buttons: 24px icon + 48×48dp touch target
*   Stroke weight: 1.5-2px
*   Design on 24×24 grid
*   Single color for system icons

**Platform-Specific:**
*   iOS: SF Symbols (filled style)
*   Android: Material Symbols (outlined style)
*   Web: Consistent with target platform

---

## 7️⃣ Animation & Motion

**Duration Standards:**
*   50-100ms: Instant (toggle, checkbox)
*   150-200ms: Short (button press, focus)
*   250-300ms: Medium (modal, drawer)
*   400-500ms: Long (page transition)
*   **Max: 500ms** (anything longer feels sluggish)

**Easing Curves:**
*   Standard: `cubic-bezier(0.4, 0.0, 0.2, 1)`
*   Emphasized: `cubic-bezier(0.2, 0.0, 0, 1)`
*   Decelerate: `cubic-bezier(0.0, 0.0, 0.2, 1)`

**Accessibility:**
*   Support `prefers-reduced-motion`
*   Provide non-animated alternatives

---

## 8️⃣ Interactive States & Feedback

**State Layer Opacity (Material Design 3):**
*   Hover: 8%
*   Focus: 12%
*   Pressed: 12%
*   Dragged: 16%
*   Disabled: 38%

**Haptic Feedback (Mobile):**
*   Light: Selection, toggle
*   Medium: Button press
*   Heavy: Error, warning
*   Success: Task complete

**Loading States:**
*   Show skeleton after 400ms
*   Use inline spinners for < 2s
*   Use progress bar for > 2s with known duration
*   Never block UI without feedback

---

## 9️⃣ Platform-Specific Rules

### 📱 Mobile (Android & iOS)

**Touch & Interaction:**
*   Touch target ≥ **48×48dp** (comfortable: 56×56dp)
*   Spacing between targets: 8dp minimum
*   Bottom actions within thumb zone
*   Bottom navigation for 3–5 main sections
*   Back button/gesture ALWAYS works

**iOS Gestures:**
*   Swipe from left edge: Back navigation
*   Pull down: Refresh
*   Swipe down from top: Dismiss modal
*   Long press: Context menu (iOS 13+)

**Android Gestures:**
*   Back button: Navigate back
*   Swipe on list item: Delete/archive
*   Long press: Selection mode
*   Swipe up from bottom: Home (Android 10+)

### 🌐 Web

**Layout:**
*   Max width: 1200–1280px
*   12-column grid (desktop)
*   8-column grid (tablet)
*   4-column grid (mobile)
*   Responsive breakpoints:
    *   Mobile: ≤600px
    *   Tablet: 601–1024px
    *   Desktop: ≥1025px

**Interaction:**
*   Hover states required
*   Focus indicators (3px outline)
*   Keyboard navigation support
*   Skip links for accessibility
*   Tables for admin/data-heavy only

---

## 🔟 Accessibility Standards (WCAG 2.1 AA)

**Touch Targets:**
*   Minimum: 48×48dp
*   Comfortable: 56×56dp
*   Spacing: 8dp between

**Color Contrast:**
*   Body text: **4.5:1** minimum
*   Large text (18pt+): **3:1** minimum
*   UI components: **3:1** minimum
*   Never rely on color alone

**Keyboard & Screen Readers:**
*   Logical tab order
*   Focus indicators (3px outline)
*   Semantic HTML (button, nav, main)
*   ARIA labels for icon-only buttons
*   Alt text for images
*   Live regions for dynamic content

**Support:**
*   Text scaling up to 200%
*   Reduced motion (`prefers-reduced-motion`)
*   Screen reader testing (VoiceOver, TalkBack)

---

## 1️⃣1️⃣ Forms & Validation

**Input Specifications:**
*   Height: 48dp minimum
*   Padding: 16dp horizontal, 12dp vertical
*   Border: 2px (1px default, 2px focus)
*   Helper text: 12sp

**Validation Rules:**
*   Validate **after blur** (not on keystroke)
*   Show errors inline, not in modals
*   Descriptive messages (not "Invalid input")
*   Mark required fields clearly
*   Disable submit until valid
*   Show success confirmation

---

## 1️⃣2️⃣ UX Rules (Non-Negotiable)

**Core Principles:**
*   One primary action per screen
*   Confirm destructive actions only (delete, logout)
*   Forms show errors after interaction
*   Never block user without feedback
*   Navigation must be predictable
*   Empty states have clear next action
*   Undo destructive actions when possible

**Performance:**
*   Show skeleton loader if > 400ms
*   Optimistic UI updates (assume success)
*   Debounce search input (300ms)
*   Cache API responses when appropriate
*   Progressive image loading

**Critical:**
*   Never override platform-standard gestures
*   Always provide alternative tap targets
*   Support offline mode gracefully

---

## 1️⃣3️⃣ Design Review Checklist (Before Dev Starts)

Designer must deliver:
*   ✅ Complete component library with all states
*   ✅ Design tokens (colors, typography, spacing)
*   ✅ Responsive layouts (mobile, tablet, desktop)
*   ✅ All screen states (loading, empty, error, success)
*   ✅ Interactive states (hover, focus, pressed, disabled)
*   ✅ Accessibility annotations (contrast, touch targets)
*   ✅ Animation specs (duration, easing)
*   ✅ Platform-specific variations (iOS vs Android)
*   ✅ Figma auto-layout enabled
*   ✅ Developer handoff documentation

**If ❌ → design goes back.**

---

## 1️⃣4️⃣ Naming Convention

**Figma Component Structure:**
```
Button/Primary/Default
Button/Primary/Hover
Button/Primary/Disabled
Input/Text/Default
Input/Text/Focus
Input/Text/Error
Card/Elevated
List/Item/TwoLine
Screen/Login
Screen/Dashboard/Loading
```

**Benefits:** Same names across design and code, easier implementation

---

## 🔥 Recommended Workflow

1.  Define tokens (colors, typography, spacing, elevation)
2.  Build component library with all states
3.  Design interactive states
4.  Design main screens
5.  Design edge cases (loading, empty, error)
6.  Responsive pass (mobile, tablet, desktop)
7.  Accessibility audit
8.  Platform variations (iOS vs Android)
9.  Animation specs
10. Developer handoff with documentation

---

## 📖 References

**Official Guidelines:**
*   [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)
*   [Material Design 3](https://m3.material.io/)
*   [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
