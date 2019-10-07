# Cookies

* text file, string
* stored in browser
* written by the server after the first visit
* browser sends cookies to the server every time
* can be stored important info such as session info (login, password), preferences, statistics
* by default are removed in the end of session if don't set the expired time derictly
* write operations modify only cookies mentioned in it
* one cookie up to 4kb, 20+ cookies per site (depends on a browser)

## Example

```js
document.cookie = "cookiename=value; expires=0; path=/";
```

## Cookie options

* `path=/`, by default current path, makes the cookie visible only under that path.
* `domain=site.com`, by default a cookie is visible on current domain only, if set explicitly to the domain, makes the cookie visible on subdomains.
* `expires` or `max-age` sets cookie expiration time, without them the cookie dies when the browser is closed.
* `secure` makes the cookie HTTPS-only.
* `samesite` forbids the browser to send the cookie with requests coming from outside the site, helps to prevent XSRF attacks.

## Additionally

* Third-party cookies may be forbidden by the browser, e.g. Safari does that by default.
* When setting a tracking cookie for EU citizens, GDPR requires to ask for permission.
