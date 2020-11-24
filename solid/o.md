# Open Closed Principle

> It states that a piece of software is open for extension but closed for modification.

> Allow adding new functionalities without changing existing code

[Example](https://github.com/vladilenm/SOLID_javascript/blob/master/2_O.js)

```js
class AjaxAdapter extends Adapter {
  constructor() {
    super();
  }
  request(url) {
    // request and return promise
  }
}

class NodeAdapter extends Adapter {
  constructor() {
    super();
  }
  request(url) {
    // request and return promise
  }
}

class HttpRequester {
  constructor(adapter) {
    this.adapter = adapter;
  }

  fetch(url) {
    return this.adapter.request(url).then((response) => {
      // transform response and return
    });
  }
}
```
