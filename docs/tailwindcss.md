# Tailwindcss

It happens that even after installing the vscode extension, it will not work.

For example using the npm package **tailwind-merge** and writing inside a `<script>` of **Vue** framework.

```
npm i -D tailwind-merge
```

## Update Tailwindcss vscode extension

Reference: https://github.com/tailwindlabs/tailwindcss-intellisense?tab=readme-ov-file#tailwindcssclassfunctions

`tailwindCSS.classFunctions` to include "**twMerge**"

```vue
<script setup lang="ts">
import { twMerge } from 'tailwind-merge';
import { computed, useAttrs } from 'vue';

const attrs = useAttrs();

const buttonClass = computed(() =>
  // Tailwindcss classes should now have auto-completion inside this function
  twMerge(
    'rounded-md',
    'bg-teal-600',
    'hover:bg-teal-500',
    'focus-visible:outline-teal-600 focus-visible:outline-2 focus-visible:outline-offset-2',
    'text-sm font-semibold text-white',
    'shadow-xs',
    'px-3.5 py-2.5',
    attrs.class as string
  )
);
</script>

<template>
  <button :class="buttonClass">
    <slot />
  </button>
</template>
```
