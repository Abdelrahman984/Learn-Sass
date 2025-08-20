# Learn Sass

A comprehensive learning project demonstrating various Sass (Syntactically Awesome Style Sheets) features and capabilities. This repository serves as a practical guide for understanding Sass syntax, features, and best practices.

## 📚 What is Sass?

Sass is a CSS preprocessor that adds powerful features to CSS, making it more maintainable, organized, and efficient. It allows you to use variables, nested rules, mixins, functions, and more, which are then compiled into standard CSS.

## 🎯 Project Overview

This project contains practical examples of Sass features organized in a modular structure. The main `main.scss` file demonstrates various Sass capabilities, while the `sass/` directory shows how to organize Sass code using partials and imports.

## ✨ Sass Features Demonstrated

### Variables & Scope
- Color variables (`$red`, `$green`, `$main`, `$alt`)
- Global and local variable scope
- Variable interpolation (`#{$variable}`)

### Nesting & Parent Selectors
- CSS rule nesting
- Parent selector (`&`) usage
- Pseudo-class and pseudo-element nesting
- Attribute selectors with parent reference

### Mixins & Functions
- Custom mixins for reusable styles
- Mixins with parameters and default values
- Built-in Sass functions (`if()`, `percentage()`, `unique_id()`)
- Error handling in mixins

### Control Directives
- `@if/@else` conditional statements
- `@for` loops for generating repetitive styles
- `@each` loops for iterating over lists
- `@while` loops for dynamic generation

### Code Organization
- `@use` and `@import` for modular architecture
- Partial files (files starting with `_`)
- Namespace management

### Advanced Features
- `@extend` and placeholder selectors (`%placeholder`)
- Media query nesting
- String interpolation
- Property nesting
- Multiple selector nesting

## 📁 File Structure

```
Learn-Sass/
├── index.html              # Demo HTML file
├── main.scss              # Main Sass file with examples
├── main.css               # Compiled CSS output
├── prepros.config         # Prepros build configuration
└── sass/
    ├── layout/
    │   └── _global-rules.scss    # Global CSS rules
    ├── variables/
    │   └── _colors.scss          # Color variables
    ├── helpers/
    │   └── _mixins.scss          # Utility mixins
    └── pages/
        └── _contact.scss         # Page-specific styles
```

## 🛠️ Setup & Compilation

### Prerequisites
- Node.js and npm (for Sass CLI) or
- Prepros (GUI tool) or  
- Any Sass compiler

### Method 1: Using Sass CLI
1. Install Sass globally:
```bash
npm install -g sass
```

2. Compile the Sass file:
```bash
sass main.scss main.css
```

3. Watch for changes (auto-compile):
```bash
sass --watch main.scss:main.css
```

### Method 2: Using Prepros
1. Install [Prepros](https://prepros.io/)
2. Open the project in Prepros
3. The configuration is already set up in `prepros.config`
4. Prepros will automatically compile Sass files when changed

### Method 3: VS Code Extensions
- Install "Live Sass Compiler" extension
- Click "Watch Sass" in the VS Code status bar

## 🎓 Learning Path

### Beginner
1. Start with variables and basic nesting in `main.scss`
2. Understand the file structure and imports
3. Practice with mixins in `sass/helpers/_mixins.scss`

### Intermediate
1. Explore control directives (`@if`, `@for`, `@each`)
2. Learn about `@extend` and placeholder selectors
3. Study the modular architecture in the `sass/` directory

### Advanced
1. Understand variable scope and `!global` flag
2. Create custom functions and advanced mixins
3. Master error handling and complex interpolation

## 🔍 Key Examples in the Code

### Variables and Interpolation
```scss
$company: "falcons";
$position: "right";

.ad-#{$company}-#{unique_id()} {
    background-image: url("imgs/#{$company}.png");
    #{$position}: 0;
}
```

### Mixins with Parameters
```scss
@mixin circle($dimensions) {
    border-radius: 50%;
    width: $dimensions;
    height: $dimensions;
}

.circle-100 {
    @include circle(100px);
}
```

### Control Directives
```scss
@for $i from 1 through 16 {
    .col-#{$i} {
        width: percentage($i / 16);
    }
}
```

### Conditional Styling
```scss
$theme: "dark";

.page {
    @if $theme == "light" {
        background-color: white;
        color: black;
    } @else {
        background-color: black;
        color: white;
    }
}
```

## 🌐 View the Demo

Open `index.html` in your browser to see the compiled styles in action. The page demonstrates various styled elements that showcase the Sass features.

## 📖 Additional Resources

- [Official Sass Documentation](https://sass-lang.com/documentation)
- [Sass Guidelines](https://sass-guidelin.es/)
- [Sass Functions Reference](https://sass-lang.com/documentation/modules)
- [CSS Tricks Sass Guide](https://css-tricks.com/sass-style-guide/)

## 🤝 Contributing

Feel free to contribute by:
- Adding more Sass examples
- Improving documentation
- Fixing any issues
- Suggesting new features to demonstrate

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

Happy learning! 🎉 Explore the code, experiment with the examples, and master the power of Sass!