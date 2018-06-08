# ![Logo](assets/signature.png) Wappla PHP

A repository containing dotfiles, code style guides, best practices used in our company related to CSS and SCSS.

## Dotfiles

Predefined dotfiles used for standard configuration. Can be added on per-project basis and adjusted accordingly.


# CSS Style Guide & Best practices

- [General PHP Rules](#general-php-rules)
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
