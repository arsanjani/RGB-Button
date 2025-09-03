# RGB Glow Button

A reusable, framework-agnostic CSS button with an animated RGB glow border, no JavaScript.

![RGB Button Demo](https://img.shields.io/badge/CSS-RGB%20Animation-ff6b6b?style=for-the-badge&logo=css3)
![Version](https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 🎬 Live Demo

!

> **Live Preview**: Open `index.html` in your browser to see the animation in action, or visit the [GitHub Pages demo](https://arsanjani.github.io/rgb-button/)

## ✨ Features

- **Exact replica** of the original animated RGB button
- **No JavaScript required** - pure CSS animation
- **Customizable** via CSS custom properties
- **Accessible** with keyboard navigation and reduced motion support
- **Framework agnostic** - works with any HTML/CSS setup
- **RTL support** included in demo
- Works with both `<button>` and `<a>` elements

## 🚀 Quick Start

1. **Copy the CSS file** into your project:
   ```
   styles/rgb-button.css
   ```

2. **Include it in your HTML**:
   ```html
   <link rel="stylesheet" href="styles/rgb-button.css">
   ```

3. **Add the class to any element**:
   ```html
   <button class="rgb-button">Buy Subscription</button>
   <a class="rgb-button" href="#">RGB Link</a>
   ```

## 📖 Demo

Open `index.html` in your browser to see:
- Default button with exact animation
- Size variations (small, medium, large)
- Custom gradient examples
- Accessibility features

## 🎨 Customization

Override CSS custom properties to customize the appearance:

```html
<button 
  class="rgb-button" 
  style="--rgb-speed: 10s; --rgb-blur: 8px; --rgb-radius: 20px;"
>
  Custom Button
</button>
```

### Available CSS Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `--rgb-gradient` | 9-color rainbow | The animated gradient colors |
| `--rgb-background` | `rgb(17, 17, 17)` | Main button background |
| `--rgb-after-background` | `rgb(34, 34, 34)` | Background overlay color |
| `--rgb-foreground` | `rgb(255, 255, 255)` | Text color |
| `--rgb-radius` | `10px` | Border radius |
| `--rgb-padding-y` | `0.6em` | Vertical padding |
| `--rgb-padding-x` | `2em` | Horizontal padding |
| `--rgb-speed` | `20s` | Animation duration |
| `--rgb-size` | `400%` | Gradient background size |
| `--rgb-blur` | `5px` | Glow blur intensity |
| `--rgb-glow-gap` | `2px` | Glow border thickness |
| `--rgb-speed-super-fast` | `3s` | Super fast animation speed |
| `--rgb-speed-fast` | `8s` | Fast animation speed |
| `--rgb-speed-slow` | `30s` | Slow animation speed |
| `--rgb-hover-opacity` | `0.9` | Opacity on hover |
| `--rgb-active-transform` | `translateY(1px)` | Transform on click |

> **Note**: The CSS now includes 50+ customizable variables for complete control over animation, positioning, typography, and interactive states!

### Custom Gradient Example

```css
.custom-gradient {
  --rgb-gradient: linear-gradient(
    45deg,
    #ff006e, #8338ec, #3a86ff, #06ffa5, #ffbe0b, #ff006e
  );
  --rgb-speed: 8s;
  --rgb-blur: 10px;
}
```

## 🎯 Technical Details

### Animation Breakdown
- **Duration**: 20 seconds linear infinite
- **Gradient Size**: 400% to create smooth movement
- **Blur Effect**: 5px for soft glow
- **Movement**: Background position animates from 0px to 400% and back

### CSS Structure
```css
.rgb-button::before {
  /* Animated RGB glow layer */
  background: var(--rgb-gradient);
  background-size: 400%;
  filter: blur(5px);
  animation: glowing-rgb-button 20s linear infinite;
}

.rgb-button::after {
  /* Dark background overlay for text readability */
  background: rgb(34, 34, 34);
}
```

## ♿ Accessibility

- **Keyboard Navigation**: Full focus-visible support
- **Reduced Motion**: Animation automatically disables if user prefers reduced motion
- **Color Contrast**: Maintains readable text contrast
- **Screen Readers**: Works with standard button/link semantics

## 🌐 Browser Support

- ✅ Chrome/Edge 88+
- ✅ Firefox 89+
- ✅ Safari 14+
- ✅ Mobile browsers with CSS custom property support

## 🔧 Troubleshooting

### Animation Not Working After Refresh?

**Root Cause**: The most common issue is that your system has "Reduce Motion" accessibility settings enabled, which disables CSS animations by default.

**Solution**: 
1. **Check Motion Settings**: On Windows, go to Settings → Accessibility → Visual effects → Animation effects (turn ON)
2. **Or Override CSS**: The component includes a commented accessibility rule. If you want animation regardless of system settings, it's already disabled in the CSS.

**Other potential causes**: Some browsers have issues with CSS variables in animation properties or CSS cascade conflicts. The component now uses a reliable default animation speed and specific modifier classes to control the duration, which prevents conflicts.

```html
<!-- Default animation (20 seconds) -->
<button class="rgb-button">Default Speed</button>

<!-- Fast animation (8 seconds) -->
<button class="rgb-button rgb-button--fast">Fast Button</button>

<!-- Slow animation (30 seconds) -->
<button class="rgb-button rgb-button--slow">Slow Button</button>

<!-- Custom speed using CSS variables -->
<button class="rgb-button rgb-button--custom" style="--rgb-speed: 15s;">
  Custom Speed
</button>
```

### If Animation Still Doesn't Work:

1.  **Hard Refresh**: Press `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)
2.  **Check Browser**: Ensure you're using a modern, updated browser.
3.  **Disable Extensions**: Some browser extensions can interfere with CSS.

## 📱 Size & Speed Modifiers

### Size Classes
Predefined size classes are included:

```html
<button class="rgb-button rgb-button--sm">Small</button>
<button class="rgb-button">Default</button>
<button class="rgb-button rgb-button--lg">Large</button>
```

### Speed Classes
Control animation speed with these modifier classes:

```html
<button class="rgb-button rgb-button--super-fast">Super Fast (3s)</button>
<button class="rgb-button rgb-button--fast">Fast (8s)</button>
<button class="rgb-button">Default (20s)</button>
<button class="rgb-button rgb-button--slow">Slow (30s)</button>
<button class="rgb-button rgb-button--custom" style="--rgb-speed: 15s;">Custom Speed</button>
```

## 🔧 Development

### File Structure
```
├── styles/
│   └── rgb-button.css     # Main component CSS
├── index.html             # Demo page with examples
└── README.md             # This documentation
```

### Performance Notes
- Uses CSS transforms and filters for hardware acceleration
- Single CSS file with no dependencies
- Optimized for smooth 60fps animation

## 📄 License

MIT License - Feel free to use in personal and commercial projects.

## 🚀 GitHub Setup Instructions

### For Repository Owners:
1. **Enable GitHub Pages**: Go to Settings → Pages → Deploy from branch → Select `main` branch
2. **Add Demo GIF**: 
   - Create a `demo/` folder
   - Add your screen recording as `rgb-button-demo.gif`
   - Update the GIF path in README: `![RGB Button Animation](./demo/rgb-button-demo.gif)`
3. **Add Tags**: Create version tags for releases (`git tag v1.0.0`)

### Recommended Repository Structure:
```
rgb-button/
├── demo/
│   ├── rgb-button-demo.gif    # Animation demo
│   └── screenshots/           # Additional images
├── styles/
│   └── rgb-button.css        # Main CSS file
├── index.html                # Demo page
├── README.md                 # Documentation
├── LICENSE                   # MIT License
└── package.json             # Optional: for npm publishing
```

### GitHub Topics (Add in Settings):
- `css`
- `animation`
- `button`
- `rgb`
- `glow-effect`
- `frontend`
- `ui-component`
- `reusable`

## 🙏 Credits

Inspired by and replicated from the original RGB button design on [Nakhl Market Plus](https://nakhlmarket.com/nakhlplus/).

## 📞 Support

- 🐛 **Issues**: [Report bugs or request features](https://github.com/yourusername/rgb-button/issues)
- 💡 **Discussions**: [Join the community discussion](https://github.com/yourusername/rgb-button/discussions)
- ⭐ **Star this repo** if you find it useful!

---

**Made with ❤️ for the CSS community**