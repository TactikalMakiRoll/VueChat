# vite_vue_tailwind_chat

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Run Unit Tests with [Vitest](https://vitest.dev/)

```sh
npm run test:unit
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```


### Features

## Firebase login - supports logging in with google
## Onboarding - on the first time user enters the app (local storage for developing), show him the onboarding and leave it available in menu
## Telegram like interface on non-mobile: Left side for Contacts, middle for the chat/channel, right for info. 

Page structure:{
    Onboarding,
    Login,
    Home,

}

Component structure:{
    UI: {
        Tab button (mobile),
        Profile Pic,
        Icon Btn,
        Search input,
        Message input,
    },
    Chat Feed + {ChatItem},
    Chat + {Chat message(+reactions probably)}
    NavigationMenu,
    Group/Chat Info (appears only when chat is selected)
}