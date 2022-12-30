## Intro
[**Functions**](https://sass-lang.com/documentation/values/functions) allow you to define complex operations on SassScript values that you can re-use throughout your stylesheet. They make it easy to abstract out common formulas and behaviors in a readable way.

### Function to convert px into rem
```scss
@use 'sass:math';

// font-size: rem(30);
// Throw an error if parameter has a unit: rem(30px)
@function rem($pixel) {

    // If $pixel is unitless, divide it by 16 to return rems
    @if math.is-unitless($pixel) {
        @return math.div($pixel, 16)+rem;
    }

    // Otherwise (else), throw an error
    @else {
        @error 'Don\'t use units when using the rem() function; only numbers.';
    }
}
```

## 📚 References
- 🔗 [Sass: @function](https://sass-lang.com/documentation/at-rules/function)
- 🔗 [Sass: Built-In Modules](https://sass-lang.com/documentation/modules)
- 🔗 [Sass: sass:math](https://sass-lang.com/documentation/modules/math)
- 🔗 [Sass: At-Rules](https://sass-lang.com/documentation/at-rules)
