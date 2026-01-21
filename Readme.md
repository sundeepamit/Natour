## website link:
 https://sundeepamit.github.io/Natour/
## Folder Purposes

| Folder        | Description                                                                                          | Typical Files                                      | Outputs CSS? |
|---------------|------------------------------------------------------------------------------------------------------|----------------------------------------------------|--------------|
| `abstracts/`  | Global tools & helpers (variables, mixins, functions, placeholders). No CSS output.                 | `_variables.scss`, `_mixins.scss`, `_functions.scss`, `_placeholders.scss` | No           |
| `base/`       | Foundational / boilerplate styles for the entire project.                                            | `_reset.scss`, `_normalize.scss`, `_typography.scss`, `_base.scss` | Yes          |
| `components/` | Reusable UI components (the largest folder in most projects).                                        | `_button.scss`, `_card.scss`, `_modal.scss`, `_form.scss`, `_alert.scss` | Yes          |
| `layout/`     | Macro layout components (grid, header, footer, navigation, sidebar, etc.).                           | `_header.scss`, `_footer.scss`, `_grid.scss`, `_navigation.scss` | Yes          |
| `pages/`      | Page-specific styles (overrides or unique layouts for individual pages).                             | `_home.scss`, `_about.scss`, `_contact.scss`, `_blog.scss` | Yes          |
| `themes/`     | Alternate visual themes (e.g., light/dark mode, admin panel). Optional for many projects.            | `_light-theme.scss`, `_dark-theme.scss`            | Yes          |
| `vendors/`    | Third-party libraries (Bootstrap, Normalize, Font Awesome, etc.) and any necessary custom overrides. | `_bootstrap.scss`, `_normalize.scss`, `_fontawesome.scss` | Yes          |
| `main.scss`   | The single entry point. Imports all partials in the correct order.                                   | —                                                  | Yes          |

## Recommended Import Order in `main.scss`

```scss
// 1. Abstracts (tools, no output)
@import 'abstracts/variables';
@import 'abstracts/functions';
@import 'abstracts/mixins';
@import 'abstracts/placeholders';

// 2. Vendors (third-party styles)
@import 'vendors/normalize';
@import 'vendors/bootstrap';

// 3. Base (global foundation)
@import 'base/reset';
@import 'base/typography';
@import 'base/base';

// 4. Layout (structural components)
@import 'layout/grid';
@import 'layout/header';
@import 'layout/footer';
@import 'layout/navigation';

// 5. Components (reusable UI pieces)
@import 'components/button';
@import 'components/card';
@import 'components/form';
@import 'components/modal';

// 6. Pages (page-specific overrides)
@import 'pages/home';
@import 'pages/about';
@import 'pages/contact';

// 7. Themes (usually loaded last or conditionally)
@import 'themes/dark';
