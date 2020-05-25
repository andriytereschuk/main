# Middleware

> `Middleware` in general is **filter** functions, **interceptor** wich allow to manage the data between different parts of a system.

In server-side web application frameworks, the term is often more specifically used to refer to pre-built software components that can be added to the framework's request/response processing pipeline, to handle tasks such as database access.

> `Middleware` in Nodejs - function that execute after the server receives the request and before the controller sends the response; and can modify **res** and **request** during this trip. To go to the next middleware run function **next()**. If you want to exit run **return**.
Command **app.use(func)** registers the middleware globally. Remember, the order is important.

## Middlewares in Express

* [http://expressjs.com/en/guide/using-middleware.html](http://expressjs.com/en/guide/using-middleware.html)
* [How To Use And Write Express Middleware](com/en/guide/using-middleware.html)

## Example

```js
// register middleware for the specific route

app.get('/users', auth, (req, res) => {
  console.log(req.admin)
  res.send('Users Page')
})

// middleware implementation
function auth(req, res, next) {
  if (req.query.admin === 'true') {
    req.admin = true
    next()
  } else {
    res.send('ERROR: You must be an admin')
  }
}
```

