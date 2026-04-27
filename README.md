# BOSS — Best Optimal Settings Style

BOSS is a CSS Core Engine and foundation layer for modern web projects. It provides a clean baseline for browser behavior, typography, form controls, media, tables, accessibility states, print output, and design tokens.

## Important Clarification

BOSS is not a UI framework.

BOSS does not provide components like cards, grids, buttons, modals, or application layouts. It provides a clean CSS foundation that can be used before your own design system, components, or product styles.

## Architecture

BOSS uses cascade layers to keep the foundation predictable:

```css
@layer reset, normalize, tokens, base, typography, forms, media, tables, a11y, theme, print, legacy;
```

- `reset`: controlled hard reset for spacing and box sizing without breaking native display behavior.
- `normalize`: browser behavior normalization for text sizing, media, forms, hidden content, and native controls.
- `tokens`: CSS Custom Properties using the `--boss-*` naming convention.
- `base`: document baseline, local Roboto font, common semantic element behavior, and core document flow.
- `typography`: readable headings, paragraphs, lists, and text rhythm.
- `forms`: consistent production-safe baseline for form controls and buttons.
- `media`: responsive defaults for images, video, canvas, SVG, audio, and iframes.
- `tables`: minimal readable table defaults.
- `a11y`: accessible focus states, reduced motion support, and forced colors support.
- `theme`: minimal light theme using semantic tokens.
- `print`: print-friendly document rules.
- `legacy`: commented optional rules for old browser support.

## Features

- Controlled hard reset
- Normalize layer
- Design tokens
- Local Roboto font
- OKLCH colors
- `rem` and `em` units
- Accessible focus states
- Reduced motion support
- Forced colors support
- Print styles
- Legacy section for optional old browser support

## Usage

```html
<link rel="stylesheet" href="boss.css">
```

## File Structure

```text
boss.css
boss.dev.scss
test.html
css/fonts/roboto.woff2
README.md
LICENSE
```

## Development

`boss.dev.scss` is the development source.

`boss.css` is the regular production build.

`boss.mini.css` may be created later as a minified build.

## License

MIT License.
