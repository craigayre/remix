---
title: useHref
---

# `useHref`

Resolves a full URL to be used as an [`href`][anchor_element_href_attribute] to a [`link`][anchor_element]. If a relative path is supplied, it will resolve to a full URL.

```tsx
import { useHref } from "@remix-run/react";

function SomeComponent() {
  const href = useHref();

  return <a href={href}>Link</a>;
}
```

## Signature

```
useHref(to, options)
```

### `to`

Optional. The path to append to the resolved URL.

### `options`

The only option is `{ relative: "route" | "path"}`, which defines the behavior when resolving relative URLs.

- **route** default - relative to the route hierarchy, not the URL
- **path** - makes the action relative to the URL paths, so `..` will remove one URL segment.

[anchor_element_href_attribute]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link#href
[anchor_element]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link
