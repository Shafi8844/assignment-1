# B8A1 – Problem Solving with TypeScript & OOP

## Assignment Overview

This repository contains the B8A1 assignment for Problem Solving with TypeScript and Object-Oriented Programming.

The TypeScript solutions demonstrate:

- Optional parameters and default behaviour.
- Union types and type narrowing.
- Readonly tuples.
- Generic functions and rest parameters.
- Interfaces and array filtering.
- Generic property access using `keyof`.
- Classes, inheritance, and access modifiers.
- Asynchronous functions and Promises.

All eight coding solutions are included in **`solutions.ts`**. The implementation uses explicit parameter and return types and avoids `any`.

## Blog Posts

1. [Type Aliases vs Interfaces in TypeScript](./type-vs-interface.md)
2. [Type Narrowing in TypeScript](./type-narrowing.md)

## Project Structure

```text
.
├── solutions.ts
├── type-vs-interface.md
├── type-narrowing.md
└── README.md
```

## Run the TypeScript Solutions

Install TypeScript if it is not already available:

```bash
npm install --save-dev typescript
```

Compile the solutions:

```bash
npx tsc solutions.ts --target ES2020 --module commonjs --strict
```

The compiler generates JavaScript output. The functions and classes can then be imported into a test file or called from a suitable TypeScript environment.

## Submission

Create a public GitHub repository, add these four files, commit and push them, then submit the repository's URL through the assignment submission box.
