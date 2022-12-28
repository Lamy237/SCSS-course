## Intro
[**Mixins**](https://sass-lang.com/documentation/at-rules/mixin) are styles rules that you can create and reuse in your styles.

## Example
```scss
// Sass map
$breakpoints-up: (
    "medium": 43.75em,
    "large": 56.25em,
    "xlarge": 90em
);

// Sass mixin
@mixin breakpoint($size) {
    @media screen and (min-width: map-get($breakpoints-up, $size)) {
        @content;
    }
}
```

## 📚 References
- 🔗 [Sass: @mixin and @include](https://sass-lang.com/documentation/at-rules/mixin)
- 🔗 [Sass: Built-In Modules](https://sass-lang.com/documentation/modules)
- 🔗 [Sass: Maps](https://sass-lang.com/documentation/values/maps)
