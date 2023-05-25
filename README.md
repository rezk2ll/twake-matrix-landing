# Twake on matrix landing page

- built using [Remix](https://remix.run/) to be used as an express request handler.

## Development

Start the Remix development asset server and the Express server by running:

```sh
npm run dev
```


## Deployment

First, build your app for production:

```sh
npm run build
```

integrate the app in the express server

```js
app.get(
  '/',
  createRequestHandler({
    build: await import(
      path.join(process.cwd(), 'landing', 'build', 'index.js')
    )
  })
)
```
