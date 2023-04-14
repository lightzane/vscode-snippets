# Visual Studio Code Snippets

My personal [Visual Studio Code](https://code.visualstudio.com/) user snippets for Javascript and Typescript

## How To

**Windows**

1. `File`
2. `Preferences > User Snippets`
3. Select existing snippet file **or** create your own new snippet
4. Copy the **user-snippet.json** content below

**MacOS**

1. `Code`
2. `Settings... > Configure User Snippets`

Steps 3-4: Same as **Windows**

**user-snippet.json**

```ts
{
  // Place your global snippets here. Each snippet is defined under a snippet name and has a scope, prefix, body and
  // description. Add comma separated ids of the languages where the snippet is applicable in the scope field. If scope
  // is left empty or omitted, the snippet gets applied to all languages. The prefix is what is
  // used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
  // $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders.
  // Placeholders with the same ids are connected.
  // Example:
  // "Print to console": {
  // 	"scope": "javascript,typescript",
  // 	"prefix": "log",
  // 	"body": [
  // 		"console.log('$1');",
  // 		"$2"
  // 	],
  // 	"description": "Log output to console"
  // }
  "@lightzane/arrow-function-single-line": {
    "scope": "javascript, typescript",
    "prefix": ["afs", "fns"],
    "description": "Generate arrow function (single line) which implicitly returns the value",
    "body": ["($1) => $0"]
  },
  "@lightzane/arrow-function": {
    "scope": "javascript, typescript",
    "prefix": ["af", "fn"],
    "description": "Generate arrow function",
    "body": ["($1) => {", "\t$2", "}"]
  },
  "@lightzane/describe-it": {
    "scope": "javascript, typescript",
    "prefix": ["describeit", "ldescribeit"],
    "description": "Generate describe() and it() for unit testing",
    "body": [
      "describe('$1', () => {",
      "\tit('$2', () => {",
      "\t\t$3",
      "\t});$4",
      "});"
    ]
  },
  "@lightzane/describe": {
    "scope": "javascript, typescript",
    "prefix": ["describe", "ldescribe"],
    "description": "Generate describe() for unit testing",
    "body": ["describe('$1', () => {", "\t$2", "});"]
  },
  "@lightzane/it": {
    "scope": "javascript, typescript",
    "prefix": ["it", "lit"],
    "description": "Generate it() for unit testing",
    "body": ["it('$1', () => {", "\t$2", "});"]
  },
  "Typescript React Function Component": {
    "prefix": "fc",
    "description": "Typescript React Function Component",
    "body": [
      // "import { FC } from 'react'",
      // "",
      "interface Props {",
      "  $1",
      "}",
      "",
      // "const ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}: FC<Props> = ({$2}) => {",
      "export default function ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}(props: Props) {",
      "  return <>${TM_FILENAME_BASE} works!</>",
      "}",
      "",
      // "export default ${TM_FILENAME_BASE/(.*)/${1:/pascalcase}/g}",
      // ""
    ]
  },
}
```

## Content Overview

|                                                         # | Prefix                        | Description                                                              |
| --------------------------------------------------------: | :---------------------------- | :----------------------------------------------------------------------- |
| [arrow-function-single-line](#arrow-function-single-line) | `afs` or `fns`                | Generate arrow function (single line) which implicitly returns the value |
|                         [arrow-function](#arrow-function) | `af` or `fn`                  | Generate arrow function                                                  |
|                               [describe-it](#describe-it) | `describeit` or `ldescribeit` | Generate `describe()` and `it()` for unit testing                        |
|                                     [describe](#describe) | `describe` or `ldescribe`     | Generate `describe()` for unit testing                                   |
|                                                 [it](#it) | `it` or `lit`                 | Generate `it()` for unit testing                                         |
|                                                 [fc](#fc) | `fc`                          | Generate a Typescript React functional component template                |

## Snippets

### arrow function single line

Generate arrow function (single line) which implicitly returns the value

```ts
// afs || fns

() =>
```

### arrow function

Generate arrow function

```ts
// af || fn

() => {};
```

### describe it

Generate `describe()` and `it()` for unit testing

```ts
// describeit || ldescribeit

describe('', () => {
  it('', () => {});
});
```

### describe

Generate `describe()` for unit testing

```ts
// describe || ldescribe

describe('', () => {});
```

### it

Generate `it()` for unit testing

```ts
// it || lit

it('', () => {});
```

### fc

Generate a Typescript React functional component template

```ts
// sample.page.tsx
interface Props {}

export default function SamplePage(props: Props) {
  return <>sample.page works!</>;
}
```
