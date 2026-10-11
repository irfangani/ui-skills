# Layout Patterns & Component Blueprints

This document provides visual balance guidelines, anti-patterns, and optimal structures for common UI components and page sections.

---

## 1. Navigation Bars

### Balance Guidelines

* **Role**: Primary function is orientation and routing, not promotion. Keep visual weight low to medium.
* **Structure**: Logo / Brand anchor on the far left; navigation links grouped centrally or left-aligned; utility actions and primary CTA on the far right.
* **Restraint**: Maximum of 1 Accent CTA button in the navigation bar. Secondary items should be plain text links or subtle ghost buttons.

### Anti-Patterns to Flag

* Multiple solid colored buttons competing in the top navigation.
* Overcrowded navigation with more than 7 top-level links without dropdown grouping.

---

## 2. Hero Sections

### Balance Guidelines

* **Role**: Establish core value proposition within 2 seconds.
* **Structure**: Eyebrow label -> Prominent H1 Display -> Breathable paragraph (`< 60ch`) -> CTA group (1 Accent button + 1 Ghost/Text link) -> Supporting social proof or visual asset.
* **Whitespace**: Provide ample top and bottom padding (`64px`–`120px` on desktop).

### Anti-Patterns to Flag

* Placing 3 or more solid colored CTA buttons side-by-side.
* Stuffing multiple unrelated badges, promo banners, and announcements into the hero container.

---

## 3. Cards and Card Grids

### Balance Guidelines

* **Role**: Encapsulate related information into digestible modular units.
* **Surface Balance**: Cards represent the **30% Secondary** surface. They must softly stand out from the 60% Primary canvas via subtle tonal shifts or a delicate 1px border.
* **Internal Hierarchy**: Card Image/Header -> Card Title -> Subtitle/Meta -> Body -> Footer action.

### Anti-Patterns to Flag

* "Russian Doll" nesting: cards placed inside cards placed inside cards.
* Pairing heavy borders (`2px` solid black) with dark drop shadows (`shadow-2xl`) on every card in a grid.

---

## 4. Forms & Data Inputs

### Balance Guidelines

* **Alignment**: Stack form fields in a single vertical column whenever possible. Multi-column forms disrupt the natural downward scanning path.
* **Grouping**: Group related inputs (e.g., Personal Info vs. Billing Info) with sectional headers and distinct spacing (`24px`–`32px`).
* **Actions**: Primary submission button should be Accent (10%); secondary actions (Cancel, Back) must be ghost buttons or text links.

### Anti-Patterns to Flag

* Labels placed far away from their respective input fields.
* Placing Save, Cancel, Delete, and Export buttons side-by-side in identical visual weights.

---

## 5. Dashboards & Analytics

### Balance Guidelines

* **Density Management**: Dashboards carry high information density. Balance high data density with calm background surfaces (neutral 60% canvas) and consistent widget padding (`20px`–`24px`).
* **KPI Metric Cards**: Number first (Level 1, large bold weight), Label second (Level 2, muted small text), Trend indicator third (Level 3, semantic green/red indicator).
* **Color Discipline**: Avoid assigning a rainbow of arbitrary colors to metric cards. Keep backgrounds unified and reserve bright hues strictly for data visualization charts or urgent warnings.

### Anti-Patterns to Flag

* Every metric card using a different bright pastel background.
* Wall-to-wall metrics with 0px margin between cards.

---

## 6. Tables & Data Lists

### Balance Guidelines

* **Headers**: Low visual weight (muted, semi-bold or medium, slightly smaller font size than row text).
* **Row Separation**: Use subtle 1px dividers or alternating row fills. Avoid heavy borders.
* **Alignment**: Left-align text; right-align numeric and currency values; center-align icons, badges, or binary states.

---

## 7. Dialogs & Modals

### Balance Guidelines

* **Focus**: The backdrop overlay dims the rest of the application (60%–70% opacity dark overlay), isolating the modal as the sole focal point.
* **Sizing**: Size modal width to content (e.g., `400px` for confirmation alerts, `600px`–`800px` for task flows). Never stretch modals full width on desktop.
* **Action Footer**: Right-align actions with the Primary Accent action on the outer edge and Cancel immediately adjacent.

---

## 8. Mobile Layout Adaptations

### Balance Guidelines

* **Stacking**: Multi-column grids must collapse to a single column to prevent horizontal crowding.
* **Sticky Navigation / CTAs**: Position primary actions in thumb-friendly bottom zones rather than crowded top bars.
* **Padding Reduction**: Reduce outer margins to `16px` so content utilizes available screen width while retaining breathing room.
