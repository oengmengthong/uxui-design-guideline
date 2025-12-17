# 🚀 Universal Project Design Generator (Mobile + Web)

Use this every time you start a new project.

---

## 1️⃣ Project Design Setup (Mandatory)

Before design starts, always define:

*   **Project Type:** (Admin / Consumer App / Landing / SaaS)
*   **Platforms:** Android / iOS / Web
*   **Primary Users:** (Admin / Staff / Customer)
*   **Theme Style:** Clean / Modern / Corporate / Playful
*   **Primary Action:** (e.g. Create, Book, Pay, Track)

👉 **No UI work until this is filled.**

---

## 2️⃣ Design Tokens (Global – must be reused)

### 🎨 Colors

*   Primary
*   Secondary
*   Background
*   Surface
*   Text Primary
*   Text Secondary
*   Success
*   Warning
*   Error

**Rules:**
*   Background = neutral (white / light gray)
*   Primary color = actions only
*   Error/Success ONLY for status

### 🔤 Typography

One font family only (two max)

*   Display / H1
*   H2
*   H3
*   Body
*   Caption

**Recommended:**
*   Mobile body: 14–16
*   Web body: 16–18
*   Line height: 1.4–1.6

### 📐 Spacing System

Use 8pt system only

`4 / 8 / 12 / 16 / 24 / 32 / 40 / 48`

❌ No random spacing

### 🔲 Radius

*   Small: 8
*   Medium: 12
*   Large: 16

Pick 2 sizes max per project.

---

## 3️⃣ Screen Structure Generator

Every screen must follow this structure:

```text
Safe Area
└── App Bar / Header
└── Content Area
    └── Sections
        └── Cards / Lists / Forms
└── Primary Action
└── Feedback (Loading / Error / Empty)
```

❌ No floating random elements.

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

## 5️⃣ Component Generator (Reusable)

Before designing screens, create these components:

**Buttons**
*   Primary
*   Secondary
*   Text
*   Danger
*   Loading
*   Disabled

**Inputs**
*   Text
*   Password
*   Number
*   Dropdown
*   Search
*   Date

**Others**
*   Card
*   List Item
*   Dialog
*   Bottom Sheet
*   Toast / Snackbar
*   Tabs
*   Avatar

**Rule:**
No custom component allowed unless approved

---

## 6️⃣ Platform-Specific Rules

### 📱 Mobile (Android & iOS)
*   Touch target ≥ 48dp
*   Bottom actions within thumb zone
*   Bottom navigation for 3–5 main sections
*   Back button ALWAYS works

### 🌐 Web
*   Max width: 1200–1280px
*   Responsive breakpoints:
    *   Mobile ≤600
    *   Tablet 601–1024
    *   Desktop ≥1025
*   Hover + focus states required
*   Tables for admin only

---

## 7️⃣ UX Rules (Non-Negotiable)

*   One primary action per screen
*   Confirm destructive actions only
*   Forms show errors after interaction
*   Never block user without feedback
*   Navigation must be predictable

---

## 8️⃣ Design Review Checklist (Before Dev Starts)

Designer must deliver:
*   ✅ Components with variants
*   ✅ Color & typography tokens
*   ✅ Responsive layouts
*   ✅ All states (loading / empty / error)
*   ✅ Figma auto-layout enabled

If ❌ → design goes back.

---

## 9️⃣ Naming Convention (Figma & Dev)

*   `Button/Primary`
*   `Input/Text/Default`
*   `Card/Default`
*   `Screen/Login`
*   `Screen/Dashboard`

Same names = easier Flutter / Web implementation.

---

## 🔥 Recommended Workflow

1.  Define tokens
2.  Build components
3.  Design main screens
4.  Design states
5.  Responsive pass
6.  Dev handoff
