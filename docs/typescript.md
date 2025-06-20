# Typescript

## Auto-import path with alias

There are times you want to put **alias** in your **tsconfig.json** paths and as well as doing an auto-import of these in your vscode IDE.

### Update settings in vscode

`Ctrl + P` (`Command + P` for MacOS) then type **settings** [Preferences: Open User Settings (JSON)]

```json
{
  "javascript.preferences.importModuleSpecifier": "non-relative",
  "typescript.preferences.importModuleSpecifier": "non-relative"
}
```

#### Outputs

```ts
import BaseInput from '@/components/BaseInput.vue';
```

#### Instead of

```ts
import BaseInput from '../components/BaseInput.vue';
```

### Update jsconfig.json or tsconfig.json

```diff
 {
   "compilerOptions": {
+    "baseUrl": ".",
     "paths": {
+      "@/*": ["./src/*"]
     }
   },
   "exclude": ["node_modules", "dist"]
 }
```

### When using Vite

<!-- prettier-ignore -->
```diff
 // vite.config.ts
 import { fileURLToPath, URL } from 'node:url'
 
 import { defineConfig } from 'vite'
 import vue from '@vitejs/plugin-vue'
 import vueDevTools from 'vite-plugin-vue-devtools'
 
 // https://vite.dev/config/
 export default defineConfig({
   plugins: [
     vue(),
     vueDevTools(),
   ],
   resolve: {
     alias: {
+      '@': fileURLToPath(new URL('./src', import.meta.url))
     },
   },
 })
```
