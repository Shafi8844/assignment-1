

TypeScript provides both `type` aliases and `interface` declarations to describe the shape of data. They often look similar, especially when defining objects, but they support different features. Understanding those differences helps developers choose a clear and maintainable approach.


An `interface` is mainly used to describe object structures. It can be extended by another interface, and declarations with the same name can be merged.

```ts
interface User {
  name: string;
}

interface Admin extends User {
  permissions: string[];
}
```

Interfaces are useful when modelling objects, classes, and public contracts that may need to be extended. For example, a class can implement an interface to guarantee that it provides the required properties or methods.

A `type` alias can describe an object too, but it can also represent unions, intersections, primitives, tuples, and function types.

```ts
type Status = "pending" | "approved" | "rejected";

type Point = {
  x: number;
  y: number;
};

type UserWithStatus = Point & {
  status: Status;
};
```

Unlike interfaces, type aliases cannot be reopened through declaration merging. This can make a type alias more predictable when defining a fixed type.
