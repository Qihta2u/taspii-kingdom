# 🏠 Local Testing & Development Guide

## Quick Start (30 seconds)

### Option 1: Just Open It 🎉
1. Navigate to: `c:\Users\athiq\OneDrive\Documents\Athiq\New folder\kingdom-taspii\`
2. Right-click `index.html`
3. Select "Open with" → your browser
4. Use bypass key: `athiq2026`

**That's it!** No server needed.

---

## Option 2: Python Web Server (Recommended)

### Setup:
```bash
cd "c:\Users\athiq\OneDrive\Documents\Athiq\New folder\kingdom-taspii"
python -m http.server 8000
```

### Access:
```
http://localhost:8000
```

**Benefits:**
- Better performance
- Consistent with production
- Simpler debugging
- Works perfectly offline

---

## Option 3: Node.js Server

### Install Node.js (if not installed):
Download from nodejs.org

### Setup:
```bash
npm install -g http-server
cd "c:\Users\athiq\OneDrive\Documents\Athiq\New folder\kingdom-taspii"
http-server
```

### Access:
```
http://localhost:8080
```

---

## Option 4: VS Code Live Server

### Install Extension:
1. Open VS Code
2. Extensions (Ctrl+Shift+X)
3. Search "Live Server"
4. Install by Ritwick Dey

### Launch:
1. Right-click `index.html`
2. Select "Open with Live Server"
3. Browser opens automatically

**Perfect for real-time development!**

---

## Testing Checklist ✅

### Scene 1: Countdown
- [ ] Timer displays correctly
- [ ] Timer counts down
- [ ] Bypass button (🗝️) works
- [ ] Bypass key `athiq2026` unlocks

### Scene 2: Password
- [ ] Password input accepts text
- [ ] Wrong password shows error/shake
- [ ] Correct password `bachii` unlocks
- [ ] Key animation plays
- [ ] Transitions to Storybook

### Scene 3: Storybook
- [ ] First page displays correctly
- [ ] Navigation arrows work (← →)
- [ ] Page 9 has butterfly 🦋 (hover reveals)
- [ ] All pages readable
- [ ] Page indicator shows position

### Scene 4: Butterfly Game
- [ ] 8 butterflies visible and animated
- [ ] Click/tap catches butterfly
- [ ] Sound plays on catch
- [ ] Progress counter increments
- [ ] Auto-continues at 8/8

### Scene 5: Flower Garden
- [ ] 6 flowers visible in 3x2 grid
- [ ] Click blooms flower
- [ ] Messages appear
- [ ] Color change on bloom
- [ ] Progress counter works

### Scene 6: Star Drawing
- [ ] Canvas draws lines smoothly
- [ ] 18 star points visible
- [ ] Pixel counter shows progress
- [ ] Success at 20+ pixels
- [ ] Continue button appears

### Scene 7: Mirror Hall
- [ ] 3 mirrors visible
- [ ] Click reveals affirmation text
- [ ] Text fades in smoothly
- [ ] Mirror changes appearance
- [ ] Progress counter works

### Scene 8: Memories
- [ ] 3 portrait images visible
- [ ] Click opens lightbox
- [ ] Images display in fullscreen
- [ ] Close button works
- [ ] Moonlight note appears

### Scene 9: Crown Hunt
- [ ] Crown field visible
- [ ] Crowns barely visible initially
- [ ] Hover reveals crown visibility
- [ ] Click collects crown
- [ ] Toast shows count
- [ ] Progress persists after refresh
- [ ] Secret modal at 10/10

### Scene 10: Birthday Celebration
- [ ] Cake visible and clickable
- [ ] Confetti falls on click
- [ ] Chime sound plays
- [ ] "Happy Birthday!" message appears
- [ ] Works multiple times

### Scene 11: Letter
- [ ] Wax seal visible (with glow)
- [ ] Click opens letter
- [ ] Letter text readable
- [ ] Hindi and English both present
- [ ] Signature visible
- [ ] Moon 🌙 glyph clickable
- [ ] Moon popup works with message

### Scene 12: Ending
- [ ] Scene displays properly
- [ ] Moon floats and glows
- [ ] Farewell message visible
- [ ] Both languages present

### Global Features
- [ ] Twinkling stars in background
- [ ] Sparkle cursor trail works
- [ ] Smooth transitions between scenes
- [ ] No console errors (F12 → Console)
- [ ] Responsive on mobile
- [ ] Audio/sound works

---

## Debugging Tips

### Open Developer Tools:
```
Windows: F12 or Ctrl+Shift+I
Mac: Cmd+Option+I
```

### Check Console for Errors:
- Click "Console" tab
- Look for red error messages
- Report any errors

### Clear Browser Cache:
```
Ctrl+Shift+Delete → Select "All time" → Clear data
```

### Test Mobile:
1. Open DevTools (F12)
2. Click device icon (top-left)
3. Select iPhone or Android

### Test LocalStorage (Crown Progress):
```javascript
// In Console, type:
localStorage.getItem('taspii_crowns')

// Should return: [0,1,2,3,4,5,6,7,8,9]
// or [] if not found any yet
```

---

## Performance Monitoring

### Check Load Time:
1. Open DevTools (F12)
2. Go to "Performance" tab
3. Click record button
4. Refresh page
5. Stop recording
6. Look for bottlenecks

### Check FPS:
```
DevTools → Performance → Record 5 seconds → Check FPS
```

**Expected:** 60 FPS for smooth animations

### Check File Size:
```bash
# In terminal:
Get-Item "index.html" | Select-Object Length

# Should be ~950KB
```

---

## Customization During Testing

### Change Unlock Date:
Find this line in `index.html`:
```javascript
const UNLOCK_AT = new Date("2026-06-17T18:00:00Z");
```

Change to:
```javascript
const UNLOCK_AT = new Date("2024-01-01T00:00:00Z");  // Past date = unlocked
```

### Change Password:
Find (around line 600):
```javascript
if(v==='bachii'){
```

Change to your password

### Change Bypass Key:
Find (around line 590):
```javascript
if(v==='athiq2026'){
```

Change to your key

---

## Mobile Testing

### Using Browser DevTools:
1. F12 → Device toggle (top-left icon)
2. Select device (iPhone, Pixel, etc.)
3. Test all interactions
4. Check touch responsiveness

### Physical Device:
1. Find your computer's IP: `ipconfig` in terminal
2. On phone, visit: `http://YOUR_IP:8000`
3. Test all scenes

---

## Audio Testing

### If Sound Doesn't Play:
1. Check browser settings (unmute)
2. Check system volume
3. Try different browser
4. Check console for Audio API errors

### Audio Triggers:
- Butterfly catches (chime)
- Crown discoveries (chime)
- Birthday celebration (synth)

---

## Accessibility Testing

### Keyboard Navigation:
- [ ] Tab through buttons
- [ ] Enter to click buttons
- [ ] Password field accepts input

### Screen Reader:
- Use NVDA (Windows, free) or JAWS
- Test button labels
- Test headings

---

## Before Deployment Checklist

- [ ] All 12 scenes work
- [ ] No console errors
- [ ] Mobile responsive
- [ ] Smooth animations (60 FPS)
- [ ] Sound working
- [ ] LocalStorage working
- [ ] All buttons clickable
- [ ] Text readable on all screens
- [ ] Load time < 2 seconds

---

## Deployment from Local

Once tested locally, deploy to:
1. **GitHub Pages** (free, permanent)
2. **Netlify** (free, easy)
3. **Vercel** (free, fast)
4. **Firebase Hosting** (free)

See `DEPLOYMENT.md` for detailed steps!

---

## Getting Help

### Common Issues:

**Q: Sites says "Not Responding"**
- A: Check browser console (F12). Refresh page. Restart server.

**Q: No sound**
- A: Check system volume. Unmute browser. Try Chrome/Firefox.

**Q: Animations lag**
- A: Close other tabs. Update graphics drivers. Try fullscreen.

**Q: LocalStorage not working**
- A: Check privacy mode is OFF. Clear browser cache.

**Q: Mobile layout broken**
- A: Check viewport meta tag. Test in Chrome DevTools mobile mode.

---

**Ready to test? Start with Option 1 and use bypass key `athiq2026`!** 🚀
