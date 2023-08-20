1. Open in VSCode with Svelte extension installed
1. `npm install`
1. Compare outputs of:
   - `npm -w app run check:ts`
   - `npm -w app run check:svelte`
1. Should see no error in TS but in Svelte:
   ```
   File '/svelte-ts-monorepo-issue/packages/dep/index.ts' is not under 'rootDir' '/svelte-ts-monorepo-issue/packages/app'. 'rootDir' is expected to contain all source files.
     The file is in the program because:
       Imported via "dep" from file '/svelte-ts-monorepo-issue/packages/app/App.svelte' with packageId 'dep/index.ts@1.0.0'
       Root file specified for compilation
   ```
