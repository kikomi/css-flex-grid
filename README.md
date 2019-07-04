# CSS Flex Grid
CSS Grid System based on [Bootstrap Grid v4.0.0](https://getbootstrap.com/docs/4.0/layout/grid/).

The main difference with the original Bootstrap Grid:
- Support for different column gutters for different screen sizes.
- Support for different container paddings for different screen sizes.
- Different container widths.
- Different breakpoints.
- Only essential utilities are included.

## Default configuration
The default number of columns in the grid is 12.

| Screen width (px) | Gutter size (px) | `.container` padding (px) |
| ----------------- | ---------------- | ------------------------- | 
| &ge; 0 (xss)      | 16               | 16                        | 
| &ge; 320 (xs)     | 16               | 16                        | 
| &ge; 600 (sm)     | 16               | 16                        | 
| &ge; 768 (md)     | 20               | 28                        | 
| &ge; 1024 (lg)    | 30               | 35                        | 
| &ge; 1280 (xl)    | 32               | 38                        | 

The configuration can be changed in the ```_variables.scss``` file.

## Utilities
There are several Bootstrap utilities included with the grid system:
- [Display](https://getbootstrap.com/docs/4.0/utilities/display/)
- [Flex](https://getbootstrap.com/docs/4.0/utilities/flex/)
- [Clearfix](https://getbootstrap.com/docs/4.0/utilities/clearfix/)
- [Float](https://getbootstrap.com/docs/4.0/utilities/float/)

## Build CSS Grid
### Prerequisites
1. Checkout the project.
1. Install [NodeJS](https://nodejs.org).
1. Install [SASS](https://sass-lang.com/) compiler *globally*.
1. Navigate to the project folder.

To build the CSS Grid run:
```bash
npm run build
```

The compiled and minified CSS will be put into `./dist` folder alongside mappings for SASS.

A test build without minification can be done with:
```bash
npm run build-test
```

## Making modifications
You can easily configure and build grid system that would meet your UI/UX design needs. To do that, make required changes in the `_variables.scss` file and follow the [Build CSS Grid](#Build_CSS_Grid) section to rebuild the grid system.
There are several parameters in the `_variables.scss` that can be controlled:
1. `$grid-breakpoints` &mdash; defines minimum dimensions at which your layout will change, adapting to different screen sizes.
1. `$container-max-widths` &mdash; defines the maximum width of `.container` for different screen sizes.
1. `$grid-columns` &mdash; sets the number of columns in the grid.
1. `$grid-gutter-widths` &mdash; defines paddings between grid columns for different screen sizes.
1. `$grid-container-paddings` &mdash; defines paddings for `.container` elements for different screen sizes.

**Important!**  `$grid-breakpoints`, `$container-max-widths`, `$grid-gutter-widths`, `$grid-container-paddings` parameters represent a `Map` where each key has to be unique. Additionally, make sure that key values are the same as in `$grid-breakpoints` map as it sets breakpoints for the entire grid.
