## Web Worker

- Web workers provide a mechanism to spawn a separate script in the background
- Basic communication happens between UI and web worker using following API
  - postmessage() - to send message
  - onmessage() - to receive message
  - myWorker.terminate() - to terminate the worker thread

#### Web workers use cases

- Data and web page caching
- Image encoding - base64 conversion
- Canvas drawing
- Network polling and websockets
- Background I/O operations
- Video/audio bu

## Server-side rendering SSR vs Client-side rendering CSR

### Client-side rendering

- When the browser makes a request to the server
  - HTML is returned as response
  - But no content yet
  - Browsers gets almost empty document
  - User sees a blank page until other resources such as JavaScript, styles, etc are fetched
  - Browser compiles everything then renders the content
- Steps involved
  - Download HTML
  - Download styles
  - Download JS
  - Browser renders page
  - Browser compiles and executes JavaScript
  - The page is then viewable and interact-able

#### Advantages of Client-Side Rendering

- Lower server load since the browser does most of the rendering
- Once loaded pages don't have to be re-rendered so navigating between pages is quick

#### Disadvantages of Client-Side Rendering

- Initial page load is slow
- SEO (Search Engine Optimization) may be low if not implemented correctly

### Server-side rendering

- When the browser makes a request to the server
  - Server generates the HTML as response plus the content
  - Server sends everything - HTML, JS to render page
  - So, the page is viewable but not interact-able
- Steps involved
  - Server sends ready to be rendered HTML, JS, and all the content
  - Browser renders page - the page is now viewable
  - Browser downloads JavaScript
