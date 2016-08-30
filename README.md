# express-inline-css
Express middleware to inject css inline to get better render performance

## Installation

```sh
npm install --save express-inline-css
```

## Preview
```js

import express from 'express';
import inlineCSS from 'express-inline-css';

const app = express();

app.use(inlineCSS({
  override: true,
  cssFile: '../client/public/css/style.css'
}));

app.get('/', (req, res) => {
  res.render('index', {});
});

```

## Usage

inlineCSS({ cssFile, [override] });
<!-- {.font-large} -->
where:

- `cssFile`: Path of the final css file where rules are taken out.
- `override` (optional): It brings you the possibility to override the method render or use renderInlineCSS.

## License

MIT © [Jordi López](http://jlopezxs.github.io)
