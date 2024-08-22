# tag-inject

> Inject tags into html

## Install

```bash
npm i tag-inject
```

## Usage

```typescript
import { inject } from 'tag-inject'

const html = `<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>title</title>
</head>
<body>
  
</body>
</html>`

const tags = [
  {
    tag: 'link',
    attrs: {
      rel: 'stylesheet',
      href: 'style.css',
    },
    injectTo: 'head',
  },
  {
    tag: 'script',
    attrs: {
      src: 'script.js',
    },
    injectTo: 'body',
  },
]

const result = inject(html, tags)
```
