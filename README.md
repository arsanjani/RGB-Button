# RGB Glow Button

A reusable, framework-agnostic CSS button with an animated RGB glow border.

![RGB Button Demo](https://img.shields.io/badge/CSS-RGB%20Animation-ff6b6b?style=for-the-badge&logo=css3)

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

## 📱 Size Modifiers

Predefined size classes are included:

```html
<button class="rgb-button rgb-button--sm">Small</button>
<button class="rgb-button">Default</button>
<button class="rgb-button rgb-button--lg">Large</button>
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

## 🙏 Credits

Inspired by and replicated from the original RGB button design on [Nakhl Market Plus](https://nakhlmarket.com/nakhlplus/).

---

**Made with ❤️ for the CSS community**