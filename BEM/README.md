## Syntax

### HTML
```html
<div class="grid">
  <aside class="grid__sidebar">
    <div class="grid__widget grid__widget--green">
      <h2>More Info</h2>
      <p>
        <!-- content here -->
      </p>
    </div>
  </aside>
</div>
```

### SCSS
```scss
// block
.grid { 

    // Element
    &__widget {

        // Modifier
        &--green {
            
        }
    }
}
```

## 📚 References
- 🔗 [Sass: Adding Suffixes](https://sass-lang.com/documentation/style-rules/parent-selector#adding-suffixes)
