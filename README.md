# react-children-render
A component for rendering children.

[![npm](https://img.shields.io/npm/v/react-children-render.svg)](https://www.npmjs.com/package/react-children-render)

## Usage

```js
import React from 'react';
import Children from 'react-children-render';

const Component = () => {
  return (
    <Children>
      <p>Foo</p>
      <p>Bar</p>
    </Children>
  );
};
```

```html
<!-- HTML Output -->
<p>Foo</p>
<p>Bar</p>
```

## Why?

Before React v16, returning adjacent JSX elements had to be wrapped in an enclosing tag.

```js
import React from 'react';

const Component = () => {
  return (
    <div>
      <p>Foo</p>
      <p>Bar</p>
    </div>
  );
};
```

After React v16, a single component can return multiple components without an enclosing tag.

```js
import React from 'react';

const Component = () => {
  return [
    <p key='1'>Foo</p>
    <p key='2'>Bar</p>
  ];
};
```

With react-children-render you can eliminate the need for unique keys.
