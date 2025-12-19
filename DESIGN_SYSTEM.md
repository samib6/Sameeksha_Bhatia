# 🎨 Visual Design Guide

## Color Palette

### Primary Colors
```
Primary Green:    #207561  ██████ Professional, trustworthy
Dark Green:       #0d3f31  ██████ Deep, sophisticated
Light Gray:       #f5f7fa  ██████ Modern, clean
```

### Usage
- **#207561** → Buttons, badges, accents, hover states
- **#0d3f31** → Dark text, strong emphasis, gradients
- **#f5f7fa** → Section backgrounds, light elements
- **White** → Cards, forms, content areas

---

## Typography Hierarchy

```
Hero Title      → 3.5rem (Desktop) / 2.2rem (Mobile)  Bold, Gradient
Section Title   → 2.8rem (Desktop) / 1.8rem (Mobile)  Bold, Colored
Heading 4       → 1.3rem                              Bold, Green
Lead Text       → 1.25rem - 1.4rem                    Semi-bold
Body Text       → 1rem - 1.1rem                       Regular
Small Text      → 0.9rem - 0.95rem                    Regular
Labels          → 0.75rem - 0.85rem                   Bold, Uppercase
```

---

## Component Styles

### Buttons

**Primary Button (Call-to-Action)**
- Background: Linear gradient (#207561 → #0d3f31)
- Color: White
- Padding: 12px 32px
- Border Radius: 30px
- Hover: Transform translateY(-2px), Shadow increase
- Font Weight: 600

```css
.btn-primary {
  background: linear-gradient(135deg, #207561, #0d3f31);
  color: white;
  padding: 12px 32px;
  border-radius: 30px;
  transition: all 0.3s ease;
}
.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(32, 117, 97, 0.3);
}
```

**Outline Button (Secondary)**
- Background: Transparent
- Border: 2px #207561
- Color: #207561
- Hover: Background fills, becomes primary

---

### Cards

**Portfolio Card**
- Background: White
- Border Radius: 12px
- Shadow: 0 4px 12px rgba(0, 0, 0, 0.1)
- Hover: 
  - Shadow: 0 20px 40px rgba(0, 0, 0, 0.2)
  - Transform: translateY(-15px)
  - Smooth transition

**Experience Card**
- Background: White
- Border: 1px #f0f0f0
- Border Radius: 12px
- Logo Section: Subtle gradient background
- Hover: Green border, enhanced shadow, lift effect

**Skill Group**
- Background: White
- Padding: 30px
- Shadow: 0 4px 15px rgba(0, 0, 0, 0.08)
- Hover: Enhanced shadow, lift, better visual depth

---

### Badges & Tags

**Skill Badge (Solid)**
- Background: Linear gradient (#207561 → #0d3f31)
- Color: White
- Padding: 10px 18px
- Border Radius: 25px
- Font Size: 0.9rem
- Font Weight: 600
- Margin: 5px
- Hover: Lift + shadow

**Tech Badge (Outline)**
- Background: #e8f5f1 (Light green)
- Color: #207561
- Border: 1px #207561
- Padding: 8px 14px
- Border Radius: 20px
- Hover: Invert colors

**Category Badge**
- Background: Linear gradient (#207561 → #0d3f31)
- Color: White
- Padding: Compact
- Text Transform: Uppercase
- Letter Spacing: 0.5px
- Font Size: 0.85rem

---

### Form Elements

**Input Fields**
- Background: #f8f9fa
- Border: 2px transparent
- Border Radius: 10px
- Height: 50px
- Padding: 12px 18px
- Focus: 
  - Border Color: #207561
  - Background: White
  - Shadow: 0 0 0 0.2rem rgba(32, 117, 97, 0.25)

**Textarea**
- Same as input
- Height: 150px
- Resize: None

---

### Effects

**Animations**
```css
@keyframes slideInLeft {
  from { opacity: 0; transform: translateX(-50px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes slideInRight {
  from { opacity: 0; transform: translateX(50px); }
  to { opacity: 1; transform: translateX(0); }
}

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
```

**Transitions**
- Standard: `all 0.3s ease`
- Smooth: `all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275)`
- Hover: `all 0.3s ease`

**Transforms**
- Hover Lift: `translateY(-2px)` to `translateY(-15px)`
- Hover Scale: `scale(1.05)` to `scale(1.2)`
- Hover Translate: `translateX(10px)`

---

## Layout Grid

### Desktop (1200px+)
- **Hero:** Split layout (6 col | 6 col)
- **Skills:** 4 columns (3 col per card)
- **Portfolio:** 3 columns per row
- **Experience:** 3 columns per row
- **Education:** Single centered column (8 col)

### Tablet (768px - 1199px)
- **Hero:** Stacked (top/bottom)
- **Skills:** 2 columns
- **Portfolio:** 2 columns
- **Experience:** 2 columns, 1 on second row
- **Education:** Centered, full width

### Mobile (< 768px)
- **All Sections:** Single column
- **Hero:** Stacked vertically
- **SVG Illustration:** Hidden or reduced size
- **Cards:** Full width with adjusted padding
- **Timeline:** Simplified (no vertical line)

---

## Spacing System

```
xs: 5px    (Small gaps, borders)
sm: 10px   (Element spacing)
md: 15px   (Card padding)
lg: 25px   (Section padding)
xl: 40px   (Large section spacing)
xxl: 50px  (Section margins)
```

**Common Patterns:**
- Section Padding: `2.5rem 0` (default) or `40px`
- Card Padding: `25px - 30px`
- Heading Bottom Margin: `20px - 30px`
- Element Gap: `10px - 15px`
- Between Sections: `50px`

---

## Shadow System

```
Subtle:        0 4px 12px rgba(0, 0, 0, 0.08)
Standard:      0 4px 15px rgba(0, 0, 0, 0.1)
Medium:        0 8px 16px rgba(32, 117, 97, 0.3)
Elevated:      0 12px 30px rgba(32, 117, 97, 0.15)
Strong:        0 15px 35px rgba(32, 117, 97, 0.2)
Heavy:         0 20px 40px rgba(0, 0, 0, 0.2)
```

**Usage:**
- Cards: Standard (0 4px 15px)
- Hover Cards: Heavy (0 20px 40px)
- Images: Strong (0 15px 35px)
- Buttons: Medium (0 8px 16px)

---

## Gradient Examples

**Primary Gradient**
```css
linear-gradient(135deg, #207561, #0d3f31)
```

**Background Gradient**
```css
linear-gradient(135deg, #f5f7fa 0%, #ffffff 100%)
linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%)
```

**Text Gradient**
```css
background: linear-gradient(135deg, #207561, #0d3f31);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
```

---

## Accessibility Considerations

✅ **Color Contrast**
- Text on primary: White on #207561 (WCAG AAA)
- Text on light: #333 on #f5f7fa (WCAG AAA)

✅ **Focus States**
- All interactive elements have visible focus
- Tab navigation works smoothly

✅ **Touch Targets**
- Buttons: 44px minimum height
- Links: 40px minimum touch area

✅ **Semantic HTML**
- Proper heading hierarchy (h1, h2, h4)
- Section landmarks
- Alt text on images

---

## Performance Tips

1. **Use CSS Transforms** for animations (better performance)
2. **Avoid Layout Shifts** - define dimensions
3. **Lazy Load Images** when possible
4. **Minimize Shadows** on hover (performance impact)
5. **Use SVG** for illustrations (crisp, scalable)

---

## Browser Support

- **Modern Browsers** (Chrome, Firefox, Safari, Edge)
- **CSS Grid & Flexbox** - Fully supported
- **CSS Animations** - Fully supported
- **CSS Gradients** - Fully supported
- **SVG** - Fully supported
- **Transform & Transitions** - Fully supported

---

## Customization Guide

### Want to Change Primary Color?
Replace `#207561` with your color:
```css
/* Search and replace globally */
--primary: #207561;  /* Change this */
--dark: #0d3f31;     /* And this */
```

### Want to Adjust Hover Effects?
Modify in `.css` file:
```css
transform: translateY(-8px);  /* Distance to lift */
box-shadow: 0 15px 35px...;   /* Shadow size */
transition: all 0.3s ease;    /* Duration */
```

### Want to Change Font Sizes?
Adjust in responsive breakpoints:
```css
.section-title {
  font-size: 2.8rem;    /* Desktop */
}
@media (max-width: 768px) {
  .section-title {
    font-size: 1.8rem;  /* Mobile */
  }
}
```

---

Made with design precision for maximum impact! 🎨
