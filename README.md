# defaultcss

A very simple module for creating a little bit of defaultcss.  This is
really useful if you are creating a small JS widget that you want to be
completely stylable by the application implementer but would also like it
to look "kind of ok" if someone want to have a quick play.

## How it Works

The provided css text is injected into the HTML document within the document
`<head>` prior to any other `<link>` or `<style>` tags.  This ensures that
any definitions that are made within your provided CSS have ample
opportunity to be overridden by user defined CSS.

## Example Usage

```js
var defaultcss = require('defaultcss');
var crel = require('crel');

defaultcss('widget', '.widget { background: red; width: 50px; height: 50px }');
document.body.appendChild(crel('div', { class: 'widget' }));
```
