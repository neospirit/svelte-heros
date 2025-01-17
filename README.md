<h1 align="center">Svelte-Heros</h1>

<p align="center">
<a href="https://svelte-heros.codewithshin.com/">Svelte Heros</a>
</p>

<p align="center">
<a href="https://github.com/sponsors/shinokada" target="_blank"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" height="25"></a>
<a href="https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps" target="_blank"><img src="https://img.shields.io/badge/PWA-enabled-brightgreen" alt="PWA Shield" height="25">
</a>
<a href="https://www.npmjs.com/package/svelte-heros" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/v/svelte-heros" alt="npm" height="25"></a>
<a href="https://twitter.com/shinokada" rel="nofollow" target="_blank"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada" height="25"></a>
<a href="http://www.apache.org/licenses/" rel="nofollow" target="_blank"><img src="https://img.shields.io/github/license/shinokada/svelte-heros" alt="License" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-heros" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/dw/svelte-heros.svg" alt="npm" height="25"></a>
</p>

New version, [Svelte-Heros-v2](https://svelte-heros-v2.codewithshin.com) is out.

Hero Icons v1 for Svelte. You can select outline and solid icons using the variation props. Svlete-Heros support major CSS framework. You can add additional CSS using the `class` props.

<p align="center">
<img width="650" src="/static/images/heros-optimized.png" />
</p>

## Installation

```sh
npm i svelte-heros@latest
```

## Icon names

[Icon names](/icon-list.md)

## Icon images

[Icon images](/icon-images.md)

## REPL

- [Demo 1](https://svelte.dev/repl/6b774b2f8ecb402a865fac0a141e3c4a)
- [Demo 2](https://svelte.dev/repl/bf72fabef3c04c808620cfdbee047f46)

## Usage

```html
<script>
  import { AcademicCap } from 'svelte-heros';
</script>
```

## Props

| Name                         | Default   |
| ---------------------------- | --------- |
| size                         | 24        |
| class                        |           |
| ariaLabel                    | file name |
| variation (solid or outline) | outline   |

## Variation

The default variation value is outline. Use the `variation` prop to change it to solid.

```html
<AcademicCap variation="solid" />
```

## Size

Use the `size` prop to change the size of icons.

```html
<AcademicCap size="30" />
<AcademicCap size="40" />
<AcademicCap size="50" />
```

## CSS HEX Colors

Use the `color` prop to change colors with HEX color code.

```html
<AcademicCap color="#ff0000" /> <AcademicCap color="#00ffd8" />
```

## CSS framework support

Use the `class` prop to change colors and add additional css.

For example, Tailwind CSS:

```html
<AcademicCap class="text-pink-700 mr-4" />
```

If you use the dark mode on your website with Tailwind CSS, add your dark mode class to the `class` prop.

Let's use `dark` for the dark mode class as an example.

```html
<AcademicCap class="text-pink-700 dark:text-blue-300" />
```

Bootstrap example:

```html
<AcademicCap class="position-absolute top-0 px-1" />
```

## aria-label

All icons have aria-label. For example `AcademicCap` has `aria-label="academic cap"`.
Use `ariaLabel` prop to modify the `aria-label` value.

```html
<AcademicCap ariaLabel="red academic cap" class="text-red-500" />
```

## Passing down other attributes

You can pass other attibutes as well.

```html
<AcademicCap tabindex="0" />
```

## Using svelte:component

```html
<script>
  import { AcademicCap } from 'svelte-heros-v2';
</script>

<svelte:component this="{AcademicCap}" />
```

## Import all

Use `import * as Icon from 'svelte-heros`.

```html
<script>
  import * as Icon from 'svelte-heros';
</script>

<Icon.ShoppingBag size="30" class="text-red-500" />
<Icon.Sparkles size="40" class="text-blue-700" />
<Icon.Star size="50" class="text-green-700" />
<Icon.VolumeUp size="60" class="text-purple-500" />
<Icon.VolumeUp size="100" class="text-purple-500" tabindex="0" />
```

[REPL](https://svelte.dev/repl/e532f0a6cf7f4d8cae9a9cc2088d234b)

## Dynamically change the variation

```html
<script>
  import { Map } from 'svelte-heros';
  let isSolid = false;
</script>

<Map size="50" on:click={() => (isSolid = !isSolid)} variation={isSolid ? 'solid' : 'outline'} />
```

## Original source

[tailwindlabs/heroicons](https://github.com/tailwindlabs/heroicons)

## Other icons

- [Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)

## Experience lightning-fast browsing and offline access with Our PWA

This website can be downloaded and installed on your device for offline access as a Progressive Web App.

To install a PWA, look for the "Add to Home Screen" option in the browser's menu or settings. On most mobile devices, this option can be found by visiting the website, then selecting the "Options" or "Menu" button in the browser, and looking for the "Add to Home Screen" option. On some desktop browsers, right-click on the page and select "Install".
