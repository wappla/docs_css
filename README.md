# ![Logo](assets/signature.png) Wappla PHP

A repository containing dotfiles, code style guides, best practices used in our company related to CSS and SCSS.

## Dotfiles

Predefined dotfiles used for standard configuration. Can be added on per-project basis and adjusted accordingly.


# CSS Style Guide & Best practices

- [Folder structure](#folder-structure)
- [Coding practices](#coding-practices)


## Folder structure

```
styling
│   main.scss
│
└───1_base                  // Configuration (Variables, grid, resets, main styling, mixins, functions, ...)
│   │   _base.scss
│
└───2_pages                 // Page specific styling
│   │   _pages.scss
│
└───3_layouts               // Collection of blocks (Forms, Headers, Footers, Contact, ...)
│   │   _layouts.scss
│
└───4_blocks                // Collection of elements (Product list, Text-blocks, Image-blocks, ...)
│   │   _blocks.scss
│
└───5_elements              // Elements - Smallest possible objects (buttons, list items, products, ...)
│   │   _elements.scss
```

## Coding practices

Use [.stylelintrc](https://github.com/wappla/docs_css/blob/master/dotfiles/.stylelintrc) in your project for linting css and scss.


### Avoid !important

!important should NEVER be used. If you cannot override styling without using important you have written bad css that uses much too specific classes.
The only use case where !important can be allowed is when a javascript plugin uses inline styling which cannot be overriden. Even then !important should be a last resort.

### Avoid nesting too deep

Max nesting depth is set to 3 in the `.stylelintrc`.
This is because when you start nesting deeper your selectors will become too heavy. When you use `BEM` the need to nest deep shouldn't be an issue.


```scss
// bad
.header {
    &__nav {
        &__link {
            // styling
        }
    }
}
// good
.header {
    &__nav {
        // styling
    }

    &__link {
        // styling
    }
}
```
