## Client-side Rendering

> Render your application's UI on the client

- The logic, data fetching, templating and routing required to display content on the page is handled by JavaScript code that executes in the browser/client.
- The entire web application is loaded on the first request. As the user navigates by clicking on links, no new request is generated to the server for rendering the pages. The code runs on the client to change the view/data.

#### Improving CSR performance

- **Budgeting JavaScript**: An initial bundle of < 100-170KB minified and gzipped is a good starting point.
- **Preloading**
- **Lazy loading**: With lazy loading, you can identify resources that are non-critical and load these only when needed.
- **Code Splitting**: To avoid a large bundle of JavaScript code, you could start splitting your bundles. -**Application shell caching with service workers**: This technique involves caching the application shell which is the minimal HTML, CSS, and JavaScript powering a user interface.

## Server-side Rendering

> Generate HTML to be rendered on the server in response to a user request

- SSR generates the full HTML for the page content to be rendered in response to a user request.

## Static Rendering

> Deliver pre-rendered HTML content that was generated when the site was built

## Incremental Static Generation

> Update static content after you have built your site

## Streaming Server-Side Rendering

> Generate HTML to be rendered on the server in response to a user request

## React Server Components

> Server Components compliment SSR, rendering to an intermediate abstraction without needing to add to the JavaScript bundle
