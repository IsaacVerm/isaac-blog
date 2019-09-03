# devtools

## Sources

[Vue detective story](https://vuejsdevelopers.com/2018/10/16/vue-js-advanced-debugging/)

[Separate Vue Devtools exist](https://chrome.google.com/webstore/detail/vuejs-devtools)

[Tutorial how to use Vue Devtools](https://flaviocopes.com/vue-devtools/)

```
Any popular framework has its own devtools extension, which generally adds a new panel to the browser developer tools that is much more specialized than the ones that the browser ships by default. 
```

[Vuex](https://flaviocopes.com/vuex/#introduction-to-vuex)

## Installation

```
npm install
```

## Setup

Simple Vue application containing some common bugs. See how Chrome DevTools can make debugging easier.

### Vue CLI

We use the [Vue CLI](https://cli.vuejs.org/) (installed globally) to scaffold the application:

```
vue create sample-app
```

The Vue CLI also offers other option like a UI to manage your application. Use the following command to start the UI server.

```
vue ui
```

The UI is a handy way to see what options the Vue CLI offers. You can ofcourse also run `vue --help` in the command line.

## Cypress

Cypress has a debugger with DevTools included. A [plugin](https://github.com/vuejs/vue-cli/tree/v3/packages/%40vue/cli-plugin-e2e-cypress) exists helping with integrating Cypress with Vue (e.g. by starting the Vue server each time the Cypress tests are run).

## Vetur

Visual code Vue [extension](https://github.com/vuejs/vetur).

## Run the app

```
npx vue-cli-service serve
```

We use npx to use the `vue-cli-service` as specified in the `package.json` of `sample-app`. `vue-cli-service` is added automatically to the `package.json` after scaffolding the app with `vue create`.