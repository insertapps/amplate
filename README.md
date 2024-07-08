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

    dit the HTML files (e.g., index.html) to modify the content and layout. Utilize Tailwind CSS classes for styling.

5. Build for production:

    ```bash
    npm run build
    ```
    This will generate minified CSS files in the specified output directory (e.g., style.css).

**Important Note:** Copy the entire contents of the built style.css into the `<style amp-custom>` tag because AMP has limitations on inline styles.

## Contributing

We encourage contributions to improve Amplate! Here's how you can participate:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them to your branch.
4. Open a pull request with a clear description of your changes.

We'll review your pull request and merge it if it aligns with the project's goals.

## License

This project is licensed under the MIT License. See the LICENSE file for details.