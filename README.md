1. Open in VSCode with Svelte extension installed
1. `npm install`
1. Open [packages/app/App.svelte](packages/app/App.svelte)
1. Should see error:
   ```
   File '/svelte-ts-monorepo-issue/packages/dep/index.ts' is not under 'rootDir' '/svelte-ts-monorepo-issue/packages/app'. 'rootDir' is expected to contain all source files.
     The file is in the program because:
       Imported via "dep" from file '/svelte-ts-monorepo-issue/packages/app/App.svelte' with packageId 'dep/index.ts@1.0.0'
       Root file specified for compilation
   ```
   - Note that deleting/unincluding the `.svelte` file from the `tsconfig.json` will make the error go away
