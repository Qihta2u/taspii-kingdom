# The Kingdom of Princess Taspii 👑

A magical interactive birthday website for Princess Taspii (Bachii). This is a beautifully crafted single-page application featuring 12 interactive scenes with games, stories, animations, and heartfelt messages.

## Features

✨ **12 Interactive Scenes:**
1. **Countdown** - Lockdown timer with bypass option
2. **Password Gate** - "Bachii" password entry
3. **Storybook** - 9-page story in Hindi & English
4. **Butterfly Passage** - Interactive butterfly catching game
5. **Memory Garden** - Flower wishes garden
6. **Star Canvas** - Draw constellation challenge
7. **Mirror Hall** - Magical mirrors with affirmations
8. **Memories** - Lightbox photo gallery
9. **Crown Hunt** - Hidden crown finder game
10. **Birthday Hall** - Cake tap with confetti celebration
11. **Letter** - Personal sealed letter
12. **Ending** - Magical conclusion scene

🎮 **Interactive Elements:**
- Clickable butterflies & flowers
- Drawing canvas for constellations
- Hidden crown search game
- Confetti animations
- Sound effects (Web Audio API)
- Local storage for progress persistence
- Touch & mobile responsive

🎨 **Design:**
- Dark mystical theme with purple & gold
- Gradient animations & shimmer effects
- Responsive CSS clamp() for all screen sizes
- Custom fonts (Cinzel, Cormorant Garamond, Great Vibes)
- Smooth transitions & particle effects

## Files

- `index.html` - Complete self-contained app (all CSS & JavaScript included)
- `README.md` - This file
- `DEPLOYMENT.md` - Hosting guides

## Quick Start

### Local Development
1. Download `index.html` 
2. Open in any modern web browser
3. Use bypass key: `athiq2026` (from the 🗝️ button)

### Testing
- Password: `bachii`
- Access all features immediately with bypass key
- All games are fully playable
- Local storage saves crown progress

## Browser Support

✅ Chrome/Edge 90+  
✅ Firefox 88+  
✅ Safari 14+  
✅ Mobile browsers (iOS Safari, Chrome Mobile)

## Deployment Options

See `DEPLOYMENT.md` for detailed hosting guides:
- GitHub Pages (Free, permanent)
- Netlify (Free, easy deployment)
- Vercel (Free, serverless)
- Firebase Hosting (Free tier available)
- Traditional web hosting

## Customization

Edit these values in `index.html`:

```javascript
// Change unlock date/time
const UNLOCK_AT = new Date("2026-06-17T18:00:00Z");

// Change bypass password
if(v==='athiq2026'){...}  // Line ~640

// Add/remove birthday audio
// Check #bday-audio element

// Customize flower messages
// Search for "Tum meri favorite person..." in HTML
```

## Technical Stack

- **HTML5** - Structure & embedded images/audio
- **CSS3** - Animations, gradients, responsive design
- **Vanilla JavaScript** - No dependencies!
- **Web Audio API** - Chime sounds
- **Canvas API** - Star drawing
- **Local Storage** - Progress persistence

## Performance

- **Size:** ~950KB (single HTML file with embedded assets)
- **Load:** Instant (no external requests except fonts)
- **Mobile:** Fully optimized for all screen sizes

## Accessibility

- Keyboard navigation support
- Mobile touch events
- High contrast theme
- Readable font sizes
- Semantic HTML

## License

Created with 💜 for Princess Taspii

---

**Credits:**
- Created by: Athiq
- Date: June 4, 2026
- Dedicated to: Bachii 👑
