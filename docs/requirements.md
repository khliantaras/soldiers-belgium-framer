# Soldiers Belgium – Map App (Framer Code Components)

## Overview
This project is a mobile-first interactive route map app built with Framer code components.

Homepage is built manually in Framer and is NOT part of this implementation.

This repo contains:
- Map component
- Popup system
- Gallery viewer
- Supporting logic

---

## Core Flow

1. User opens Homepage (built in Framer)
2. Clicks "Start Route"
3. Navigates to Map page
4. Sees map with route + points + own location
5. Clicks point → opens popup
6. Can:
   - Navigate (Google Maps)
   - Open Story (full screen)
   - Mark as Visited

---

## Tech Requirements

- React (Framer Code Components)
- TypeScript preferred
- Must use `addPropertyControls` for editable content in Framer
- Map library: MapLibre GL JS (preferred) or Mapbox GL JS
- Mobile-first UI
- Smooth animations (no janky behavior)
- Clean, modular code (split into components if needed)

---

## Components to Build

### 1. SoldiersMap.tsx

#### Features:
- Dark/black map style
- Accept route points via Framer property panel

Each point must support:
- id (1–6)
- latitude
- longitude
- title
- shortDescription
- longDescription
- coverPhoto
- markerPhoto
- audioUrl
- gallery (array of images)
- navigateUrl (Google Maps link)

#### Map Behavior:
- Show user live location
- Animated user marker
- Show heading/direction if available (compass)
- Draw fixed route line between points (1 → 2 → 3 → ...)

#### Initial View:
- Fit bounds to include:
  - all route points
  - user location
- Padding:
  - top: 20px
  - left/right: 20px
  - bottom: ~220px (space for popup)

#### Markers:
- Circular image marker
- Yellow border
- Small number badge (top-right)
- If visited:
  - replace number badge with yellow check icon

#### Interaction:
- On marker click:
  - select point
  - center horizontally
  - offset vertically so popup does not cover it
  - open popup

---

### 2. RoutePopup.tsx

#### Small Popup (default):
- Bottom sheet style
- Animated open
- Content:
  - photo
  - title
  - short description

#### Buttons:
- Navigate → opens Google Maps link
- Open Story → expands popup
- Visited → toggle state

---

### 3. Full Story Mode

#### Behavior:
- Expands to full screen
- Has close button (X) top-right
- X must be sticky (fixed while scrolling)

#### Content:
- Cover photo
- Title
- Long description
- Audio player
- Horizontal gallery (5–6 images)
- Navigate button
- Visited toggle

---

### 4. GalleryViewer.tsx

#### Features:
- Fullscreen image viewer
- Swipe left/right between images
- Close button (X)
- Smooth transitions

---

## State Management

- Store visited points in `localStorage`
- Key example:
