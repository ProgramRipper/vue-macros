# shortBind <PackageVersion name="@vue-macros/short-bind" />

<StabilityLevel level="stable" />

A shorthand for binding prop with the same data name.

`:value` -> `:value="value"`

|   Features   |     Supported      |
| :----------: | :----------------: |
|    Vue 3     | :white_check_mark: |
|    Nuxt 3    | :white_check_mark: |
|    Vue 2     |        :x:         |
| Volar Plugin | :white_check_mark: |

## Usage

### Basic Usage

```vue twoslash
<script setup>
const value = 'foo'
</script>

<template>
  <input :value />
  <!-- => <input :value="value" /> -->
</template>
```

### With `shortVmodel`

```vue
<template>
  <Comp ::value />
  <!-- => <Comp ::value="value" /> => <Comp v-model:value="value" /> -->
  <Comp $value />
  <!-- => <Comp $value="value" /> => <Comp v-model:value="value" /> -->
  <Comp *value />
  <!-- => <Comp *value="value" /> => <Comp v-model:value="value" /> -->
</template>
```

## Volar Configuration

```jsonc {5}
// tsconfig.json
{
  "vueCompilerOptions": {
    "plugins": [
      "@vue-macros/volar/short-bind",
      // ...
    ],
  },
}
```
