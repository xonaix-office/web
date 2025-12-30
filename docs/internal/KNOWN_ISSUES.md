# Known Issues

## Website v9.2 - iOS Third-Party Browser Color Animation

**Status:** Known, Deferred  
**Severity:** Cosmetic  
**Affected:** Chrome, Edge, Brave, Firefox on iOS/iPadOS  
**Logged:** 2025-12-07  
**Version:** v9.2

### Description
X stroke color animations display as static white in third-party browsers on iOS/iPadOS. Safari on iOS works correctly.

### Root Cause
Apple requires all iOS browsers to use WebKit. Third-party browsers use a restricted WebKit version that doesn't support `style.fill` and `style.stroke` manipulation on SVG elements the same way Safari does.

### Current Behavior
- **Safari (iOS/iPadOS):** Full color-shifting animation ✅
- **Safari (macOS):** Full color-shifting animation ✅
- **Chrome/Firefox/Edge (Desktop):** Full color-shifting animation ✅
- **Chrome/Edge/Brave/Firefox (iOS):** Static white X strokes ⚠️

### Attempted Solutions
1. CSS keyframe animations - Failed
2. JavaScript `setAttribute()` - Failed  
3. SMIL `<animate>` - Failed
4. JavaScript `style.property` - Works Safari only
5. Canvas rendering for X strokes - Works everywhere

### Future Fix
Extend Canvas rendering to ALL animated SVG elements (nodes, rings, rays, etc.) for complete iOS compatibility across all browsers.

### Decision
Accepted for v9.2. Safari is the primary iOS browser (~90% market share on iOS). Fix deferred to future iteration.
