# Responsive Image Astro

> **Experimental package - Please refer to [source code](https://github.com/MrAmericanMike/responsive-image-astro) if you don't feel comfortable using it.**

## Installation

```sh
npm install responsive-image-astro
```

```sh
pnpm install responsive-image-astro
```

```sh
yarn install responsive-image-astro
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
-   `breakpoints` (Numbers array of the 'breakpoints' to generate the srcset for)

*   Optionally you can pass other parameters like `alt`, `format`, `class` and so on. This are present on the type `<LocalImageProps>`

```astro
<ResponsiveImage src={world} breakpoints={[200, 400, 600, 800]} />
<ResponsiveImage src={world} breakpoints={[200, 400, 600, 800]} alt="The World" format="avif" />
```

## What it does?

It will create `srcset` for images automatically for each of the given breakpoints.

Example:

```html
<img
	alt="The World"
	src="/assets/world.73e46027_WMMQ4.avif"
	srcset="
		/assets/world.73e46027_1QVP2p.avif  200w,
		/assets/world.73e46027_Z7OSi1.avif  400w,
		/assets/world.73e46027_Z27BBCr.avif 600w,
		/assets/world.73e46027_WMMQ4.avif   800w
	" />
```

## **Work In Progress**

There is still a lot to do and test and add...

