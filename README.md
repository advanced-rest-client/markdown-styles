# Markdown styles set for API components

The styles are applied to the element with `[slot="markdown-html"]` attribute.

### API components

This components is a part of [API components ecosystem](https://elements.advancedrestclient.com/)

## Usage

### Installation
```
npm install --save @advanced-rest-client/markdown-styles
```

### In an html file

```html
<html>
  <head>
    <script type="module">
      import '@advanced-rest-client/markdown-styles/markdown-styles.js';
    </script>
  </head>
  <body>
    <style include="markdown-styles"></style>
    <marked-element markdown="...">
      <div slot="markdown-html"></div>
    </marked-element>
  </body>
</html>
```

### In a Polymer 3 element

```js
import {PolymerElement, html} from '@polymer/polymer';
import '@advanced-rest-client/markdown-styles/markdown-styles.js';

class SampleElement extends PolymerElement {
  static get template() {
    return html`
    <style include="markdown-styles"></style>
    <marked-element markdown="...">
      <div slot="markdown-html"></div>
    </marked-element>
    `;
  }
}
customElements.define('sample-element', SampleElement);
```

### Installation

```sh
git clone https://github.com/advanced-rest-client/markdown-styles
cd api-url-editor
npm install
npm install -g polymer-cli
```
