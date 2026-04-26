# Architecture

## Components Structure

/components
  SoldiersMap.tsx        → main map logic
  RoutePopup.tsx         → bottom sheet popup
  GalleryViewer.tsx      → fullscreen gallery

## Data Flow

- SoldiersMap holds:
  - points data
  - selected point
  - visited state

- RoutePopup:
  - receives selected point
  - handles UI + actions

- GalleryViewer:
  - receives images array
  - handles fullscreen swipe

## State

- selectedPoint → Map
- visitedPoints → localStorage
- popupState → closed / small / full
