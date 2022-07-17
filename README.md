# Nuxt 3 Minimal Starter

Look at the [nuxt 3 documentation](https://v3.nuxtjs.org) to learn more.

## Setup

versions
```
$node -v
v16.16.0
$yarn -v
1.22.19
```

start dev
```
$yarn dev
```

output
```
 ERROR  Cannot start nuxt:  Error: Cannot find module /node_modules/@vicons/tabler/es/BrandSentry.js imported from file:///Users/XXXX/Develop/nuxt3-vite-error, file:///Users/XXXX/Develop/nuxt3-vite-error/node_modules

  at resolvePath (node_modules/mlly/dist/index.mjs:972:10)
  at isValidNodeImport (node_modules/mlly/dist/index.mjs:1055:30)
  at isExternal (node_modules/externality/dist/index.mjs:122:49)
  at runMicrotasks (<anonymous>)
  at processTicksAndRejections (node:internal/process/task_queues:96:5)
  at async transformRequest (node_modules/@nuxt/vite-builder/dist/index.mjs:388:7)
  at async transformRequestRecursive (node_modules/@nuxt/vite-builder/dist/index.mjs:420:15)
  at async transformRequestRecursive (node_modules/@nuxt/vite-builder/dist/index.mjs:429:5)
  at async transformRequestRecursive (node_modules/@nuxt/vite-builder/dist/index.mjs:429:5)
  at async transformRequestRecursive (node_modules/@nuxt/vite-builder/dist/index.mjs:429:5)
```

`nuxt dev` is failed when module include a file that file name include 'entry', like 'BrandSentry.js'. 

the logic is here.
https://github.com/nuxt/framework/blob/v3.0.0-rc.5/packages/vite/src/dev-bundler.ts#L66