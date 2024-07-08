# Amplate - HTML AMP Template build with TailwindCSS

This repository contains the source code for Amplate, a free and open-source HTML AMP template built with Tailwind CSS.

## Demo

https://insertapps.com/demo/amplate

## Features

- AMP (Accelerated Mobile Pages) compatible: The template utilizes AMP components for exceptional loading speeds on mobile devices.
- Tailwind CSS integration: Style your website efficiently with pre-built Tailwind classes.
- Responsive design: The template adjusts to various screen sizes, delivering an optimal user experience.
- Clean and modern design: Amplate offers a sleek and minimalist aesthetic suitable for diverse content types.

## Using the Template

1. Clone the repository:

    ```bash
    git clone git@github.com:insertapps/amplate.git
    ```

2. Install dependencies:

    Navigate to your project directory and run:

    ```bash
    npm install
    ```

3. Run development server:

    Start a local development server to preview your changes:

    ```bash
    npm run dev
    ```

    This will create a file named `style.css` in your project and then open index.html either with a live server or by launching the development server, which will display your AMP template in the browser.

4. Customize the template:

    Edit the HTML files (e.g., index.html) to modify the content and layout. Utilize Tailwind CSS classes for styling.

5. Build for production:

    ```bash
    npm run build
    ```
    This will generate minified CSS files in the specified output directory (e.g., style.css).

    **Important Note:** Copy the entire contents of the built style.css into the `<style amp-custom>` tag because AMP has limitations on inline styles.

## Customize The Styling

This template ships with no custom CSS; it purely uses Tailwind utility classes throughout.

As a result, the HTML code to display the search icon becomes very long:

```html
<span class="relative w-5 h-5 before:absolute before:content-[''] before:block before:top-0 before:w-4 before:h-4 before:border-2 before:border-black before:rounded-full after:absolute after:content-[''] after:block after:h-[10px] after:border-2 after:rounded-full after:border-black after:right-[2.5px] after:-rotate-45 after:-bottom-[1px]"></span>
```

To simplify things, you can use the following custom style:

Add custom css to main.css:

### Custom CSS for Search Icon

```css
/* main.css 
@tailwind base;
@tailwind components;
@tailwind utilities;
*/
@layer components {

    .search-icon {
        @apply relative w-5 h-5;

        &::before,
        &::after {
            @apply absolute block content-[''];
        }
    }

    .search-icon::before {
        @apply top-0 w-4 h-4 border-2 border-black rounded-full;
    }

    .search-icon::after {
        @apply h-[10px] border-2 rounded-full border-black right-[2.5px] -rotate-45 -bottom-[1px];
    }
}
```

Change to:

```html
<span class="search-icon"></span>
```

### Custom CSS Formatter for Text Content

```css
/* main.css
@tailwind base;
@tailwind components;
@tailwind utilities;
*/
@layer components {

    .content {
        @apply break-words;
    }

    .content p,
    .content .lead,
    .content blockquote,
    .content ol li,
    .content h2,
    .content h3 {
        @apply leading-normal;
    }

    .content p,
    .content .lead,
    .content blockquote,
    .content ol li {
        @apply my-5 text-lg sm:text-xl;
    }

    .content .lead {
        @apply text-xl sm:text-2xl mb-5;
    }

    .content h2,
    .content h3 {
        @apply font-bold mt-8;
    }

    .content h2 {
        @apply text-3xl;
    }

    .content h3 {
        @apply text-2xl;
    }

    .content blockquote {
        @apply italic border-l-4 pl-4;
    }

    .content ol {
        @apply list-inside list-decimal pl-2;
    }
}
```

Change to :

```html
<div id="entry-content" class="content">
    <p>Lorem ipsum...</p>
    <h2>Embracing New Directions</h2>
    ...
    ...
</div>
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.