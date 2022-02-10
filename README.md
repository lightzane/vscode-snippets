# Visual Studio Code Snippets

My personal [Visual Studio Code](https://code.visualstudio.com/) user snippets for Javascript and Typescript

## How To

1. `File`
2. `Preferences > User Snippets`
3. Select existing snippet file **or** create your own new snippet
4. Copy the snippet content below

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
  }
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

## Snippets

### arrow function single line

Generate arrow function (single line) which implicitly returns the value

```
// afs || fns
() =>
```

### arrow function

Generate arrow function

```
// af || fn
() => {

};
```

### describe it

Generate `describe()` and `it()` for unit testing

```
// describeit || ldescribeit
describe('', () => {
    it('', () => {

    });
});
```

### describe

Generate `describe()` for unit testing

```
// describe || ldescribe
describe('', () => {

});
```

### it

Generate `it()` for unit testing

```
// it || lit
it('', () => {

});
```
