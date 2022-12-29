## Responsive Typography
For responsive typography, it is good to use the function [**clamp**](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp).

### My conventions
```css
h1 {
    font-size: clamp(1.75rem, 1rem + 2vw, 2.5rem); /* clamp(28px, 16px + 2vw, 40px); */
}

h2 {
    font-size: clamp(1.375rem, 0.875rem + 1.5vw, 2.25rem); /* clamp(22px, 14px + 1.5vw, 36px); */
}
```

**Note:**
- **1vw = 1%** of the device width. So on a mobile device (_375px_), `1vw = 3.75px`.
