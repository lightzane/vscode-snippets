# Visual Studio Code Extensions

My personal [Visual Studio Code](https://code.visualstudio.com/) extensions

## General Extensions

| Ext name                          | Author          | Description                                                                                                                             |
| --------------------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `Material Icon Theme`             | ✅ Philipp Kief | Material Design Icons for Visual Studio Code                                                                                            |
| `Prettier - Code formatter`       | ✅ Prettier     | Code formatter using prettier (for web dev and nodejs)                                                                                  |
| `Markdown Preview Github Styling` | ✅ Matt Bierner | Changes VS Code's built-in markdown preview to match Github's style                                                                     |
| `Better Comments`                 | ✅ Aaron Bond   | Improve your code commenting by annotating with alert, informational, TODOs, and more!                                                  |
| `DotENV`                          | mikestead       | Support for dotenv file syntax                                                                                                          |
| `Error Lens`                      | Alexander       | Improve highlighting of errors, warnings and other language diagnostics.                                                                |
| `GitLens -- Git supercharged`     | GitKraken       | Supercharge Git within VS Code - Visualize code authorship at a glance via Git blame annotations and CodeLens, seamlessly navigate a... |

## Vscode Themes

| Ext name                      | Author           | Description                                                                |
| ----------------------------- | ---------------- | -------------------------------------------------------------------------- |
| `Dracula Official`            | ✅ Dracula Theme | Official Dracula Theme. A dark theme for many editors, shells, and more.   |
| `Apollo Midnight Color Theme` | Apollo GraphQL   | A dark theme based on Apollo Studio's color palette in Explorer dark mode. |
| `One Dark Pro`                | binaryify        | Atom‘s iconic One Dark theme for Visual Studio Code                        |

## Angular Extensions

https://angular.io/

| Ext name                   | Author     | Description                           |
| -------------------------- | ---------- | ------------------------------------- |
| `Angular Language Service` | ✅ Angular | Editor services for Angular templates |

## GraphQL Extensions

https://graphql.org/

| Ext name                       | Author                | Description                                                                                                                  |
| ------------------------------ | --------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `GraphQL: Syntax Highlighting` | ✅ GraphQL Foundation | Adds syntax highlighting support for .graphql & embedded support for javascript, typescript, vue, markdown, python, php, ... |
| `Apollo GraphQL`               | Apollo GraphQL        | Rich editor support for GraphQL client and server development that seamlessly integrates with the Apollo platform            |

- Overall, use `GraphQL: Syntax Highlighting` on a non-federated GraphQL API.
- It is recommend to use `Apollo GraphQL` when handling [Apollo Federation and Subgraphs](https://www.apollographql.com/docs/apollo-server/using-federation/apollo-subgraph-setup/), specifically the `extend schema` syntax
  - Reference: https://www.apollographql.com/docs/devtools/editor-plugins/

## Jest Extensions

https://jestjs.io/

| Ext name             | Author    | Description                                                               |
| -------------------- | --------- | ------------------------------------------------------------------------- |
| `Jest Runner`        | firsttris | Simple way to run or debug a single (or multiple) tests from context-menu |
| `Jest Test Explorer` | kavod.io  | Run your tests in Sidebar of Visual Studio Code                           |

## Python Extensions

https://www.python.org/

| Ext name | Author       | Description                                                                                                           |
| -------- | ------------ | --------------------------------------------------------------------------------------------------------------------- |
| `Python` | ✅ Microsoft | IntelliSense (`Pylance`), Linting, Debugging (`Python Debugger`), code formatting, refactoring, unit tests, and more. |

- As of this writing, when installing `Python` ext, then it will also automatically the following VScode ext: `Pylance` and `Python Debugger`

## TailwindCSS Extensions

https://tailwindcss.com/

| Ext name                                   | Author           | Description                                  |
| ------------------------------------------ | ---------------- | -------------------------------------------- |
| [`Tailwind CSS IntelliSense`][tailwindcss] | ✅ Tailwind Labs | Intelligent Tailwind CSS tooling for VS Code |

[tailwindcss]: https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss

[Read more](./docs/tailwindcss.md) on how to customize its settings

## Vue Extensions

| Ext name                         | Author | Description              |
| -------------------------------- | ------ | ------------------------ |
| [`Vue - Official`][vue-official] | ✅ Vue | Language Support for Vue |

[vue-official]: https://marketplace.visualstudio.com/items?itemName=Vue.volar
