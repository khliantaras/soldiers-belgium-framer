# UI Kit – Soldiers Belgium

## Brand Feel
Premium, dark, military-inspired, modern mobile app.
Should feel like a cinematic walking route experience, not a standard map app.

## Colors

### Background
- App background: #050505
- Surface: #111111
- Elevated surface: #181818

### Accent
- Primary yellow: #FFD84D
- Yellow hover: #FFE57A
- Yellow dark: #B9951E

### Text
- Primary text: #FFFFFF
- Secondary text: #B8B8B8
- Muted text: #777777

### Borders
- Soft border: rgba(255,255,255,0.12)
- Yellow border: #FFD84D

---

## Typography

### Font
Use system font by default:
- Inter
- SF Pro Display
- Arial fallback

### Sizes
- Page title: 28px / 34px / 700
- Popup title: 20px / 26px / 700
- Body: 15px / 22px / 400
- Small text: 13px / 18px / 400
- Button: 15px / 18px / 600

---

## Radius

- Marker: 999px
- Small popup: 24px top radius
- Full popup: 0px or 24px top radius
- Buttons: 999px
- Cards: 18px

---

## Shadows

Use soft shadows only:
- Popup shadow: 0 -20px 60px rgba(0,0,0,0.45)
- Marker shadow: 0 8px 24px rgba(0,0,0,0.35)

---

## Marker Style

### Default Marker
- Size: 58px
- Shape: circle
- Image: markerPhoto
- Border: 3px solid #FFD84D
- Badge:
  - top-right
  - 22px
  - black background
  - yellow border
  - white number

### Visited Marker
- Same image marker
- Badge replaced by yellow circle
- Check icon in black

---

## User Location Marker

- Animated pulsing blue/white dot
- Direction cone/arrow if heading is available
- Should not feel like default browser marker

---

## Popup Style

### Small Popup
- Bottom sheet
- Height: auto, around 190–230px
- Background: #111111
- Border top: rgba(255,255,255,0.12)
- Radius: 24px 24px 0 0
- Animated slide up

### Full Story Popup
- Full screen
- Background: #050505
- Scrollable content
- Sticky close button top-right
- Smooth transition from small popup

---

## Buttons

### Primary Button
Used for Navigate.
- Background: #FFD84D
- Text: #050505
- Radius: 999px
- Height: 48px
- Font weight: 700

### Secondary Button
Used for Open Story.
- Background: rgba(255,255,255,0.08)
- Text: #FFFFFF
- Border: rgba(255,255,255,0.12)

### Visited Button
Default:
- Background: rgba(255,255,255,0.08)
- Text: #FFFFFF

Active:
- Background: #FFD84D
- Text: #050505

---

## Gallery

- Thumbnail size: 120x90px
- Radius: 16px
- Horizontal scroll
- Gap: 10px
- Fullscreen viewer background: #000000
- Close X: top-right fixed

---

## Animation

- Bottom sheet open: 280ms ease-out
- Full popup open: 320ms ease-out
- Marker click focus: smooth map flyTo
- Gallery viewer: 220ms fade/slide
- Avoid bouncy cartoon animation

---

## Framer Property Controls

Expose these editable settings:
- accentColor
- backgroundColor
- popupBackground
- markerSize
- markerBorderWidth
- markerBorderColor
- smallPopupHeight
- mapPaddingTop
- mapPaddingSides
- mapPaddingBottom
