# @mutsuntsai/esbuild-plugin-vue

building vue 3.x SFC files with esbuild, forked from [wellfrog16/esbuild-plugin-vue-next](https://github.com/wellfrog16/esbuild-plugin-vue-next).

# Quickstart

- install

```bash
npm install -D @mutsuntsai/esbuild-plugin-vue
// or
yarn add -D @mutsuntsai/esbuild-plugin-vue
// or
pnpm add -D @mutsuntsai/esbuild-plugin-vue
```

- use plugin

```js
// build.js
const { build } = require('esbuild')
const pluginVue = require('@mutsuntsai/esbuild-plugin-vue')

build({
    entryPoints: ['index.js'], // your entry file
    bundle: true,
    outfile: 'bundle.js',
    plugins: [pluginVue()]
})
```

- run esbuild

```
node build.js
```

## Options

```js
export interface Options {
    // template
    templateOptions?: Pick<SFCTemplateCompileOptions, 'compiler' | 'preprocessLang' | 'preprocessOptions' | 'compilerOptions' | 'transformAssetUrls'>

    // script
    scriptOptions?: Pick<SFCScriptCompileOptions, 'babelParserPlugins'>

    // style
    styleOptions?: Pick<SFCAsyncStyleCompileOptions, 'modulesOptions' | 'preprocessLang' | 'preprocessOptions' | 'postcssOptions' | 'postcssPlugins'>
}

```
