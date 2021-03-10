# The 7-1 Pattern

The architecture known as the 7–1 pattern (7 folders, 1 file), is a widely-adopted structure that serves as a basis for large projects. You have all your partials organised into 7 different folders, and a single file sits at the root level (usually named main.scss) to handle the imports — which is the file you compile into CSS.

## About folders

**Abstracts or Utilities:** holds Sass tools, helper files, variables, functions, mixins and other config files. These files are meant to be just helpers which don’t output any CSS when compiled.

**Base:** holds the boilerplate code for the project. Including standard styles such as resets and typographic rules, which are commonly used throughout your project.

**Components or Modules:** holds all of your styles for buttons, carousels, sliders, and similar page components (think widgets). Your project will typically contain a lot of component files — as the whole site/app should be mostly composed of small modules.

**Layout:** contains all styles involved with the layout of your project. Such as styles for your header, footer, navigation and the grid system.

**Pages:** any styles specific to individual pages will sit here. For example it’s not uncommon for the home page of your site to require page specific styles that no other page receives.

**Themes:** this is likely not used in many projects. It would hold files that create project specific themes. For example if sections of your site contain alternate color schemes.

**Vendors:** contains all third party code from external libraries and frameworks — such as Normalize, Bootstrap, jQueryUI, etc. However, there is often a need to override vendor code. If this is required, its good practice to create a new folder called vendors-extensions/ and then name any files after the vendors they overwrite. The filevendors-extensions/\_bootstrap.scss would contain all your Bootstrap overrides — as editing the vendor files themselves, isn’t generally a good idea.

**Main.scss:** This file should only contain your imports!
