# Responsive Image Astro

> **Experimental package - Please refer to source code if you don't feel comfortable using it.**

## Installation

```sh
pnpm install responsive-image-astro
```

## Usage

### Import the component and the image to be displayed

```js
---
import ResponsiveImage from "responsive-image-astro";
import world from "../assets/world.jpg";
---
```

### Component has 2 required parameters:

-   `src` (An import of the image to be used of type `<ImageMetadata>`)
-   `breakpoints` (A list of numbers arrays of the 'breakpoints' to generate the srcset for)

*   Optionally you can pass other parameters like `alt`, `format`, `class` and so on. This are present on the type `<LocalImageProps>`

```html
<ResponsiveImage src="{world}" breakpoints="{[200," 400, 600, 800]} />
<ResponsiveImage src="{world}" breakpoints="{[200," 400, 600, 800]} alt="The World" format="avif" />
```

## **Work In Progress**

There is still a lot to do and test and add...

