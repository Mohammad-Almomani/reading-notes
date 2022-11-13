# Chakra UI

What is a Chakra UI?

    Chakra UI is a simple, modular and accessible component library that gives you the building
    blocks you need to build your React applications. It is built on top of styled-system,
    a utility library that allows you to style your components quickly and easily.

Is Chakra UI better than material UI?

    Chakra UI is best known for having:

    fewer classes for each HTML tag;
    easy manual manipulation in CSS classes;
    a robust, layout-focused library;
    easier-to-pick-up controls (since it's new);
    composable, flexible, and scalable code;
    built-in support (fewer code changes);
    good documentation; and
    a level of performance that is good for small- to medium-sized, uniquely designed apps.

    Material UI is best known for having:

    a large variety of pre-styled UI components;
    more classes for individual HTML tags;
    more CSS classes with more components;
    less facility for the creation of custom components;
    robust documentation (slightly better than Chakra UI);
    a more mature and active community; and
    a level of performance that is great for large, data-driven apps.

    If you need something that’s quick on its feet, Chakra UI is the best option,
    since it is super easy to learn and lightweight.

    If custom designs are important for your project, Chakra’s developer convenience is the more attractive option.

    Material UI has many more ready-to-use UI components, so we recommend going with it for websites
    and apps where a unique design is not central to the app, for larger websites,
    and for apps that require extremely good performance and reliability.

How to use Chakra UI?

    To use Chakra UI, you need to install it first. You can do this by running the following command in your terminal:

    npm install @chakra-ui/react @emotion/react @emotion/styled framer-motion

    After installing Chakra UI, you need to set up the ChakraProvider at the root of your application.
    This can be either in your index.jsx, index.tsx or App.jsx depending on the framework you use.

```js
import * as React from "react";

// 1. import `ChakraProvider` component
import { ChakraProvider } from "@chakra-ui/react";

function App() {
  // 2. Wrap ChakraProvider at the root of your app
  return (
    <ChakraProvider>
      <TheRestOfYourApplication />
    </ChakraProvider>
  );
}
```
