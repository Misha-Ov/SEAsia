# Components

For small components, there is the `components/` folder. While `layout/` is macro (defining the global wireframe), `components/` is more focused on widgets. It contains all kind of specific modules like a button, a slider, a loader, a widget, and basically anything along those lines. There are usually a lot of files in components/ since the whole site/application should be mostly composed of tiny modules. 

The styles described in each component file should only be concerned with:
    the style of the component itself;
    the style of the component’s variants, modifiers, and/or states;
    the styles of the component’s descendents (i.e. children), if necessary.
If you want your components to be able to be themed externally (e.g. from a theme inside the themes/ folder), limit the declarations to only structural styles, such as dimensions (width/height), padding, margins, alignment, etc. Exclude styles such as colors, shadows, font rules, background rules, etc.

A component partial can include component-specific variables, placeholders, and even mixins and functions. Keep in mind, though, that you should avoid referencing (i.e. @import-ing) component files from other component files, as this can make your project’s dependency graph an unmaintainable tangled mess.

Reference: [Sass Guidelines](https://sass-guidelin.es/) > [Architecture](https://sass-guidelin.es/#architecture) > [Components folder](https://sass-guidelin.es/#components-folder)
