# Preparação do ambiente

### Pré Requisitos:

- node 22.15.0
- npm 11.3.0

#### 1 - Nuxt Installation

```bash
npm create nuxt <project-name> or
npx nuxi@latest init <project-name>
```

- chose npm or your favorite package manager
- chose only eslint (optional)
  - if do not chose eslint:
  ```bash
npm install @nuxt/eslint@latest -D --ignore-scripts
```
add `modules: ['@nuxt/eslint'],`

#### 2 - Clone vscode configs submodule

```bash
git submodule add https://github.com/betogroo/vscode .vscode
```

_Explain extensions, snippets, settings, cspell, prettier, etc_

#### 3 - Add Eslint rules

- Edit file: `eslint.config.mjs`
- Test on a vue file

#### 4 - Run App

```bash
npm run dev
```

#### 5 - Folder structure

- add nuxt 4 compatibility
- create app folder and move app.vue inside
- create pages and folder
- create index and about pages
- create layout folder and default.vue page

#### 6 - Install Vuetify Module

```bash
npm install vuetify-nuxt-module@latest -D --ignore-scripts
```

add `vuetify-nuxt-module` on modules array
_on this moment we note a different text formatting_

- create simple nav bar on default layout with vuetify app component

```
<template>
  <v-app full-height>
    <div class="d-flex justify-end align-center mr-4">
      <nuxt-link to="/">Home</nuxt-link>
      <div class="ma-1">|</div>
      <nuxt-link to="/about">About</nuxt-link>
    </div>

    <v-main>
      <v-container>
        <slot />
      </v-container>
    </v-main>
  </v-app>
</template>
```

- create vuetify app-bar

```
<v-app-bar>
      <v-toolbar-title>My Nuxt App</v-toolbar-title>
      <v-spacer />
      <v-btn
        text
        to="/"
        >Home</v-btn
      >
      <v-btn
        text
        to="/about"
        >About</v-btn
      >
    </v-app-bar>
```

##### Obs

- Explain app and main vuetify tags
- Explain CSpell
- Explain vscode snippets
- Explain extensions
- Explain settings
