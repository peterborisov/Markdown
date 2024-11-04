## Design patterns

- Creational Patterns
- Behavioral Patterns
- Functional Patterns

https://www.patterns.dev/vanilla/observer-pattern/
https://javascriptpatterns.vercel.app/patterns/design-patterns/prototype-pattern

> Design patterns are concepts to performantly solve commonly recurring problems in software architecture.

- **Module Pattern** - Split up your code into smaller, reusable pieces. Only the values that are explicitly exported with the **export** keyword are accessible to other files.
- **Singleton Pattern**- Share a single global instance throughout our application. Redux use this pattern.
- **Proxy Pattern** - Intercept and control interactions to target objects. With the Proxy pattern, we don't want to interact with the object directly. Instead, a Proxy object intercepts the request(get, set, etc.), and (optionally) forwards this to the target object.
- **Observer Pattern** - Use observables to notify subscribers when an event occurs.
- **Factory Pattern** - Use a factory function in order to create objects.

```
const createUser = (name, userName) => {
    name,
    userName
}

createUser("John", "one")
createUser("Doe", "two")
```

- **Prototype Pattern** - Share properties among many objects of the same type.

## React patterns

- **Container/Presentational Pattern** - separating the view from the application logic. To achieve this, we need to have:
  - Presentational Component, that cares about how data is shown to the user.
  - Container Component, that cares about what data is shown to the user.
- **Higher-Order Components** - Pass reusable logic down as props to components.
- **Render Props Pattern** - Pass JSX elements to components through props.
- **Hooks Pattern** - Use functions to reuse stateful logic among multiple components throughout the app.
- **Provider Pattern** - Make data available to multiple child components.
- **Compound Pattern** - Create multiple components that work together to perform a single task.

## Performance patterns

> Performance patterns can be used to achieve a better user and developer experience.

- **Bundling, compiling, minifying, tree-shaking**
  - Bundlers(Webpack) - bundles our application together in one or multiple files
  - Compilers(Babel) - A compiler converts JavaScript (or TypeScript) code into another version of JavaScript, which could be backwards compatible in current and older browsers or environments.
  - Minifiers(Terser, Uglify) - reduce the size of a JavaScript file based on a certain configuration, for example by removes comments, making variable and function names smaller, removing whitespace, and so on.

## Rendering patterns

- **Client-Side Rendering** - Render your application's UI on the client.
  - client req HTML from server
  - server return empty HTML
  - client parse and render HTML
  - client req and download JS
  - client executes JS, render content
- **Static Rendering** - Deliver pre-rendered HTML content that was generated when the site was built
  - client req HTML from server
  - server return requested HTML
  - client parse and render content
  - client req JS bundle from server
  - client hydrates elements
- **Incremental Static Regeneration** - Pre-render certain pages, and render the other pages on-demand.
- **Server-Side Rendering** - Generate HTML on every request.
  - client req HTML from server
  - server generates page HTML
  - client parse and render HTML
  - client req JS bundle from server
  - client hydrates elements
