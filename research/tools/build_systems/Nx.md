## Useful Commands
### nx g @nx/react:application apps/my-app
Generates a react app named my-app in the apps folder

## Configurations
### tsconfig.json
#### types
- Value: `string | string[]`
- Example: ["node", "vite/client", "@nx/react/typings/cssmodule.d.ts"]
- Description: Defines the type files that are to be included from internal or downloaded (node_modules) modules. Any file that extends `tsconfig.json` also extends the defined type files. 