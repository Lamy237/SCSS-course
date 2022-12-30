## Intro
[**Mixins**](https://sass-lang.com/documentation/at-rules/mixin) are styles rules that you can create and reuse in your styles.

## Example
```scss
/* _breakpoints.scss */

// Sass map
$breakpoints-up: (
    "medium": 43.75em,
    "large": 56.25em,
    "xlarge": 90em
);

// Sass mixin for media queries
@mixin breakpoint($size) {
    @media screen and (min-width: map-get($breakpoints-up, $size)) {
        @content;
    }
}


/* _grid.scss */
@use '../util' as u;

// Using the Sass mixin: <=> @media screen and (min-width: 56.25em)
@include u.breakpoint(large) {
    grid-template-columns: 2fr 1fr;
    grid-template-rows: auto;
}

```

## 📚 References
- 🔗 [Sass: @mixin and @include](https://sass-lang.com/documentation/at-rules/mixin)
- 🔗 [Sass: Built-In Modules](https://sass-lang.com/documentation/modules)
- 🔗 [Sass: Maps](https://sass-lang.com/documentation/values/maps)
