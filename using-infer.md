### **`infer` Type in TypeScript**  
The `infer` keyword in TypeScript is used within conditional types to infer (or extract) a type from another type. It is commonly used for advanced type manipulations, such as extracting return types, function argument types, or nested properties.

---

## **1. Basic Usage of `infer`**
The `infer` keyword is used inside a conditional type (`extends ? :`) to infer a part of the type.

### **Example: Inferring Function Return Type**
```typescript
type GetReturnType<T> = T extends (...args: any[]) => infer R ? R : never;

function getData(): string {
  return "Hello, TypeScript!";
}

type ReturnTypeExample = GetReturnType<typeof getData>; // string
```
- Here, `infer R` extracts the return type of the function.
- If `T` is a function, `R` will be inferred as its return type; otherwise, it returns `never`.

---

## **2. Inferring Function Parameter Types**
You can also use `infer` to extract the parameter types of a function.

```typescript
type GetParameters<T> = T extends (...args: infer P) => any ? P : never;

function logMessage(message: string, count: number) {
  console.log(message, count);
}

type Params = GetParameters<typeof logMessage>; // [string, number]
```
- `infer P` extracts the tuple of function parameters.

---

## **3. Inferring From Promise Types**
You can use `infer` to extract the resolved value type of a `Promise`.

```typescript
type UnwrapPromise<T> = T extends Promise<infer R> ? R : T;

type AsyncData = Promise<number>;
type Result = UnwrapPromise<AsyncData>; // number
```
- `infer R` extracts `number` from `Promise<number>`.

---

## **4. Inferring Nested Types**
You can also infer types from nested structures.

```typescript
type NestedArray<T> = T extends (infer U)[] ? U : T;

type Numbers = NestedArray<number[]>;  // number
type Strings = NestedArray<string[]>;  // string
type Mixed = NestedArray<(string | number)[]>; // string | number
```
- Extracts the element type from an array.

---

## **5. Inferring Class Instance Types**
You can infer the instance type of a class.

```typescript
class Person {
  name: string;
  constructor(name: string) {
    this.name = name;
  }
}

type InstanceTypeOf<T> = T extends new (...args: any[]) => infer R ? R : never;

type PersonInstance = InstanceTypeOf<typeof Person>; // Person
```
- `infer R` extracts the type of the instance returned by a constructor.

---

### **Why Use `infer`?**
- **Flexible**: Helps in extracting types dynamically instead of manually specifying them.
- **Reusability**: Used in utility types like `ReturnType<T>` and `Parameters<T>`.
- **Advanced Type Manipulation**: Useful for complex types in generic programming.

Would you like an example with a real-world use case? 🚀
