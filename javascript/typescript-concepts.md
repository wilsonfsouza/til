<h1 align="center">
    <img height=50 alt="idea" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn-images-1.medium.com%2Fmax%2F1200%2F1*0ei2MOQxAzF7krm-v60wnQ.jpeg&f=1&nofb=1" />
    <br>
    Typescript
</h1>

<h2 align="left">Table of Contents</h2>

* [Introduction](#introduction)
* [When should I add types](#when-should-i-add-types)
* [Practice TypeScript](#practice-typescript)
    * [Ex1: Declaring a type](#ex-1-declaring-a-type)

# Introduction
TypeScript is an open-source language that extends JavaScript by adding static type definitions and improves our development experience.

Types not only provide better documentation and code readability but also allow TypeScript to check if our code is working correctly.

Since TypeScript is built on JavaScript, it provides access to the most recent JavaScript features. For example, when developing with Node.js and TypeScript, you can use the command `import` instead of `require` when importing components and other libraries.

All the TypeScript code is transformed into JavaScript code via the **TypeScript compiler** or **Babel**, and it works in any browser, host, or Operational System (OS) - basically anywhere JavaScript runs.

*See the [official documentation](https://www.typescriptlang.org/docs/home) for more information.*

# When should I add types

- When we press `ctrl + space` right after calling an object, and it doesn't complete with its methods.

- When we hover over our variable, and the following message is displayed: `Parameter 'nameOfParameter' implicitly has an 'any' type`.

- When we are trying to make our code easier to understand and to perform maintanance.

- When isolating components or parts of our code.

> A type will specify the format of our data, so we can know ahead o time what are the attributes of an object and which one is required, for example.

# Practice TypeScript
*You should select an IDE that supports TypeScript. TypeScrypt makes your IDE "smart" by adding the **IntelliSense** (e.g., code completion, parameter info, quick info, and member lists features). I recommend using the VS Code.*

*See the [VS Code documentation](https://code.visualstudio.com/docs/editor/intellisense) for more information about IntelliSense.*


## Ex 1: Declaring a type
#### Node.js application with Express and TypeScript

SUMMARY: In this example, we are exporting a function that will take **request** and **response** as parameters, and it will return a JSON object with the message "Hello World." This function is using **request** and **response** from `express` in a node.js application.

PROBLEM: When we are isolating components, our IDE might not recognize types automatically.

SOLUTION: Declaring types.

Since we are not using express in our component file directly, we need to import and declare the types in the way express uses them.

```ts
import { Request, Response } from 'express';
```

We can declare a type by using a ":" (comma):

- request`: Request`
- response`: Response`

After declaring the type, by pressing `ctrl + space`, the editor can identify methods and parameters related to request and response in the function *helloWorld*.

FINAL CODE:

```typescript
import { Request, Response } from 'express';

export function helloWorld(request: Request, response: Response) {
    return response.json({ message: "Hello World" });
}
```

> If you know what to expect from your parameters and function/methods responses, the maintenance of our code becomes easier.
