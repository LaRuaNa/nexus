---
id: api-unionType
title: unionType
sidebar_label: unionType
---

Union types are very similar to interfaces, but they don't get to specify any common fields between the types.

```ts
const MediaType = unionType({
  name: "MediaType",
  description: "Any container type that can be rendered into the feed",
  definition(t) {
    t.members("Post", "Image", "Card");
    t.resolveType((item) => item.name);
  },
});
```

@see https://graphql.org/learn/schema/#union-types