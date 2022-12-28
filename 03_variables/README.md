## Intro
**Variables** are ways to store informations and give them a label with a name.

Sass and CSS both have variables:
- In CSS, they are called CSS custom properties.
- In Sass, they are called Sass variables.

**Note:** 
- You can use JavaScript to change the value of a CSS custom property.
- To make Sass variables accessible to any other Sass file, you need to use [Sass modules](https://sass-lang.com/guide#topic-5).

## Examples
### CSS custom properties
```css
/* _colors.scss */
:root {
    --BGCOLOR: hsl(0, 0%, 11%);
    --COLOR: hsl(0, 0%, 100%);
}

/* _boilerplate.scss */
body {
    background-color: var(--BGCOLOR);
    color: var(--COLOR);
}
```

### Sass variables
```scss
/* _fonts.scss */
$FF: 'Open Sans', sans-serif;

/* _boilerplate.scss */
@use '../util' as u;
html {
    font-size: 100%;
    font-family: u.$FF;
}
```
