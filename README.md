# Markdown styles set for API components

The styles are applied to the element with `[slot="markdown-html"]` attribute.

[![Published on NPM](https://img.shields.io/npm/v/@advanced-rest-client/markdown-styles.svg)](https://www.npmjs.com/package/@advanced-rest-client/markdown-styles)

## Usage

### Installation

```sh
npm install --save @advanced-rest-client/markdown-styles
```

### In a LitElement

```javascript
import { LitElement, html, css } from 'lit-element';
import markdownStyles from '@advanced-rest-client/markdown-styles/markdown-styles.js';

class MarkdownImpl extends LitElement {
  static get styles() {
    return [
      css`
        :host {
          ...
        }`
      ,
      markdownStyles
    ],
  }

  render() {
    return html`
    <marked-element markdown="....">
      <div slot="markdown-html"></div>
    </marked-element>`;
  }
}
```

### In a Polymer 3 element

Note, Polymer styles are deprecated and will be removed.

```js
import {PolymerElement, html} from '@polymer/polymer';
import '@advanced-rest-client/markdown-styles/markdown-styles-polymer.js';

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

Note, the element does not include Polymer library.

## Development

```sh
git clone https://github.com/advanced-rest-client/markdown-styles
cd markdown-styles
npm install
```
