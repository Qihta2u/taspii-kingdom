# 🎨 Customization Guide

Everything you need to personalize your Kingdom! 👑

---

## 📝 Text Content Customization

### Page Titles & Headings

**Location:** Lines 1-7
```html
<title>👑 The Kingdom of Princess Taspii 👑</title>
```
**Change to:**
```html
<title>👑 [Your Celebration] 👑</title>
```

---

## ⏰ Date & Time Customization

### Unlock Date & Time

**Location:** Line ~620
```javascript
const UNLOCK_AT = new Date("2026-06-17T18:00:00Z");
```

**To change unlock time:**
```javascript
const UNLOCK_AT = new Date("2025-12-25T18:00:00Z");  // Christmas 2025, 6:00 PM UTC
```

**Format:** `YYYY-MM-DDTHH:MM:SSZ` (24-hour time in UTC)

**Examples:**
```javascript
// January 1, 2025, midnight UTC
const UNLOCK_AT = new Date("2025-01-01T00:00:00Z");

// July 4, 2025, 3:30 PM UTC
const UNLOCK_AT = new Date("2025-07-04T15:30:00Z");

// Set to past date to unlock immediately
const UNLOCK_AT = new Date("2020-01-01T00:00:00Z");
```

---

## 🔐 Password & Bypass Key

### Main Password

**Location:** Line ~640
```javascript
if(v==='bachii'){
```

**Change to:**
```javascript
if(v==='your-password-here'){
```

**Tip:** Use a meaningful word or phrase (2-3 words work great)

### Bypass Key (Creator Access)

**Location:** Line ~630
```javascript
if(v==='athiq2026'){
```

**Change to:**
```javascript
if(v==='your-secret-key'){
```

**Tip:** This is for testing and creator access only

---

## 🌈 Colors & Themes

### CSS Variables (at top of `<style>`)

**Location:** Lines 12-20
```css
:root{
  --bg:#0a0a1a;              /* Dark purple background */
  --gold:#d4a84b;            /* Primary gold color */
  --gold2:#f0c060;           /* Bright gold accents */
  --moon:#e8e0f0;            /* Light text color */
  --rose:#d4829a;            /* Rose/pink accent */
  --lavender:#9b7ec8;        /* Purple accent */
  --blue:#2244aa;            /* Blue accent */
  --deep:#050510;            /* Very dark background */
}
```

### Color Palettes (Pre-made)

**Warm & Romantic:**
```css
--bg: #1a0f0a;
--gold: #d97706;
--gold2: #f59e0b;
--rose: #dc2626;
--lavender: #a855f7;
```

**Cool & Dreamy:**
```css
--bg: #0a1428;
--gold: #0ea5e9;
--gold2: #06b6d4;
--rose: #a78bfa;
--lavender: #60a5fa;
```

**Forest & Nature:**
```css
--bg: #0c2e1f;
--gold: #10b981;
--gold2: #34d399;
--rose: #f87171;
--lavender: #a7f3d0;
```

---

## 🖼️ Images & Portraits

### Portrait Images (Scene 8)

**Location:** Lines ~780 (search for "portrait-grid")

Current setup uses base64 embedded images. To use your own:

1. Convert image to base64: https://www.base64-image.de/
2. Find the image tags (search "portrait")
3. Replace the data URL

**Example:**
```html
<!-- Replace this -->
<img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABA..." alt="">

<!-- With this -->
<img src="data:image/jpeg;base64,[YOUR_BASE64_STRING_HERE]" alt="">
```

Or use a simple image URL:
```html
<img src="https://example.com/your-image.jpg" alt="">
```

---

## 🎵 Music & Sound

### Chime Sound Frequency

**Location:** Line ~750
```javascript
const osc = ctx.createOscillator();
osc.frequency.setValueAtTime(880, now);
```

**Change 880 to:**
- `440` - Lower, deeper chime
- `1000` - Higher, brighter chime
- `1320` - Super high sparkle

### Birthday Audio

**Location:** Line ~820
Search for `triggerBirthday()` function

Add audio file or Web Audio synthesis here

---

## 📖 Storybook Content

### Edit Story Pages

**Location:** Lines ~560 (search for "scene-storybook")

Each page is HTML markup:
```html
<div class="page-card">
  <div class="page-text">Your text here...</div>
  <div class="page-num">1</div>
</div>
```

**To edit Page 1:**
Find the first storybook div and change the text

**To change number of pages:**
1. Update `TOTAL_PAGES = 9` (line ~585)
2. Add/remove page divs
3. Update page numbers

---

## 🦋 Butterfly Game Customization

### Number of Butterflies

**Location:** Line ~565
```javascript
const TOTAL_BUTTERFLIES = 8;
```

Change to: `6`, `10`, `12`, etc.

### Butterfly Emoji

**Location:** Line ~715 (search for "b-fly")
```javascript
c.textContent='🦋';
```

Change to any emoji: `🐝`, `🐞`, `🦗`, `🐛`

---

## 🌸 Flower Garden Messages

**Location:** Lines ~775 (search for "garden messages")

Current messages in Hindi/English:
```javascript
// Format: [emoji, 'English message', 'हिंदी संदेश']
```

Edit the text directly or replace with your own messages

### Example:
```javascript
{emoji:'🌹', en:'You are kind', hi:'तुम दयालु हो'},
```

---

## 👑 Crown Hunt Positions

### Change Crown Locations

**Location:** Line ~905
```javascript
const crownPositions=[
  {x:5,y:5},{x:85,y:8},...
];
```

**Format:** `{x:[0-100], y:[0-100]}`
- x: percentage from left (0-100)
- y: percentage from top (0-100)

**To randomize:**
```javascript
const crownPositions = Array.from({length:10}, () => ({
  x: Math.random()*100,
  y: Math.random()*100
}));
```

---

## 💌 Letter Content

### Personal Message

**Location:** Line ~810 (search for "scene-letter")

**Edit the letter text:**
```html
<div class="letter-text">
  <div class="line">Dear Birthday Person,</div>
  <div class="line">Your custom message here...</div>
</div>
```

### Signature

**Location:** Same section
```html
<div class="letter-sig">— Your Name</div>
```

### Moon Note Message

**Location:** Line ~870 (search for "One Tiny Favor")

Change the popup text:
```html
<div class="m-body">
  Your custom message here...
</div>
```

---

## 🎂 Birthday Scene

### Birthday Message

**Location:** Line ~835 (search for "bday-msg")

Change the celebration text:
```html
<div id="bday-msg" class="bday-big">
  Your custom message!
</div>
```

### Cake Image

Replace with your own cake image (base64 or URL)

---

## 🌙 Ending Scene

### Farewell Message

**Location:** Line ~870 (search for "scene-ending")

Edit the ending text:
```html
<div class="ending-sub">
  Your custom farewell message...
</div>
```

### Quote

```html
<div class="ending-whisper">
  "Your custom quote here..."
</div>
```

---

## 🎯 Creator Information

### Author/Creator Name

Search for "Athiq" and replace with your name

**Locations:**
- package.json line 5
- README.md
- HTML comments

### Metadata

**package.json:**
```json
"author": "Your Name",
"homepage": "https://yourdomain.com",
"description": "Your description"
```

---

## 🎨 Font Customization

### Change Fonts

**Location:** Lines 6-7
```html
<link href="https://fonts.googleapis.com/css2?family=...">
```

**Use Google Fonts:**
1. Go to fonts.google.com
2. Select fonts you like
3. Copy the `<link>` tag
4. Paste in `<head>`
5. Update CSS `font-family` properties

### Available font variables:
```css
font-family: 'Cinzel Decorative', serif;    /* Title font */
font-family: 'Cormorant Garamond', serif;   /* Main font */
font-family: 'Great Vibes', cursive;        /* Fancy font */
```

---

## 🎬 Animation Customization

### Animation Speeds

**Location:** Lines ~50-100

```css
@keyframes shimmer {
  animation: shimmer 3s linear infinite;  /* Change 3s */
}

@keyframes twinkle {
  animation: twinkle var(--d,3s) ...;     /* Change 3s */
}
```

Lower values = faster (e.g., `1s`)  
Higher values = slower (e.g., `5s`)

---

## 📱 Responsive Sizing

### Change Size Ranges

```css
font-size: clamp(11px, 3vw, 14px);
/*          ↑       ↑   ↑
            min    mobile  desktop
*/
```

**Example:** Make everything bigger
```css
font-size: clamp(14px, 4vw, 18px);  /* Larger minimum & maximum */
```

---

## 🔗 External Links

### Add Social Links

Find the ending scene and add:
```html
<div style="margin-top:20px;">
  <a href="https://instagram.com" target="_blank">Instagram</a>
  <a href="https://twitter.com" target="_blank">Twitter</a>
</div>
```

---

## ✅ Verification Checklist

After customizing, verify:

- [ ] Password works with new value
- [ ] Bypass key works
- [ ] Unlock date is correct
- [ ] All text displays properly
- [ ] Images load without errors
- [ ] Colors look good
- [ ] Fonts render correctly
- [ ] No console errors (F12)
- [ ] Mobile still responsive
- [ ] All buttons still work

---

## 💾 Save Your Changes

1. Edit `index.html` in your text editor
2. Save (Ctrl+S)
3. Refresh browser (F5) to see changes
4. Test thoroughly

---

## 🚀 Ready to Customize!

Start small, test each change, and have fun making it uniquely yours! 👑✨
