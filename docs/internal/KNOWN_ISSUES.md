# Known Issues

Internal tracking for website issues.

## Active Issues

### Performance

- [ ] Particle count may be too high on low-end mobile devices
- [ ] 3D transforms may cause battery drain on mobile

### Browser Compatibility

- [x] iOS Safari 3D transform fixes applied (v9.2)
- [ ] Test on older Android browsers

### Accessibility

- [ ] Add proper focus states for keyboard navigation
- [ ] Add reduced-motion media query support
- [ ] Screen reader announcements for animated content

## Resolved Issues

### v9.2 (2025-12-22)

- Fixed: iOS Safari CSS animation color cycling not working
- Fixed: 3D transforms not hardware accelerated on iOS
- Applied: webkitTransformStyle preserve-3d fix
