
Type narrowing is the process of reducing a variable's possible types inside a particular section of code. It allows TypeScript to understand which operations are safe after checking a value. Narrowing is especially useful when working with union types.

The `typeof` operator narrows primitive values such as strings, numbers, and booleans. For example:

```ts
function formatValue(value: string | number): string {
  if (typeof value === "string") {
    return value.trim().toLowerCase();
  }

  return value.toFixed(2);
}
```

Inside the first branch, TypeScript knows that `value` is a string. In the second branch, it knows that it is a number.

The `instanceof` operator checks whether an object was created from a particular class or constructor. It is useful when handling different class instances.

```ts
class Dog {
  bark(): string {
    return "Woof";
  }
}

function describeAnimal(animal: Dog | Date): string {
  if (animal instanceof Dog) {
    return animal.bark();
  }

  return animal.toDateString();
}
```

The `in` operator checks whether a property exists on an object. This can distinguish between object types in a union.

```ts
type EmailUser = { email: string };
type PhoneUser = { phone: string };

function contact(user: EmailUser | PhoneUser): string {
  if ("email" in user) {
    return user.email;
  }

  return user.phone;
}
```

These checks help TypeScript safely identify the properties and methods available in each branch.

