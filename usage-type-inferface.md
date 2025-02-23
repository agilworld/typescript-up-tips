In TypeScript, **types** and **interfaces** are both used to define the shape of objects, but they have key differences. Here’s a breakdown:

---

## **Types in TypeScript**
A `type` is a way to define a custom type alias. It can represent primitives, unions, intersections, tuples, and even mapped types.

### **Example 1: Basic Type Alias**
```typescript
type User = {
  name: string;
  age: number;
};
```

### **Example 2: Union Types**
```typescript
type Status = "active" | "inactive" | "pending";
```

### **Example 3: Intersection Types**
```typescript
type Employee = { id: number; name: string };
type Manager = Employee & { department: string };

const manager: Manager = { id: 1, name: "Alice", department: "Sales" };
```

### **Example 4: Function Type**
```typescript
type Add = (a: number, b: number) => number;

const add: Add = (x, y) => x + y;
```

---

## **Interfaces in TypeScript**
An `interface` is used to define the structure of an object and is extendable via inheritance.

### **Example 1: Basic Interface**
```typescript
interface User {
  name: string;
  age: number;
}
```

### **Example 2: Extending Interfaces**
```typescript
interface Employee {
  id: number;
  name: string;
}

interface Manager extends Employee {
  department: string;
}

const manager: Manager = { id: 1, name: "Bob", department: "HR" };
```

### **Example 3: Implementing an Interface**
```typescript
interface Person {
  name: string;
  greet(): string;
}

class User implements Person {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  greet() {
    return `Hello, ${this.name}`;
  }
}
```

### **Example 4: Readonly & Optional Properties**
```typescript
interface Product {
  readonly id: number;
  name: string;
  price?: number;
}

const product: Product = { id: 123, name: "Shoes" };
// product.id = 456; // Error: Cannot assign to 'id' because it is a read-only property.
```

---

## **Key Differences Between Type and Interface**
| Feature         | Type                          | Interface                     |
|---------------|-----------------------------|-------------------------------|
| Object shape  | ✅ Yes                        | ✅ Yes                        |
| Union Types   | ✅ Yes                        | ❌ No                         |
| Intersection  | ✅ Yes (`&`)                   | ✅ Yes (`extends`)            |
| Extensibility | ❌ No (cannot be reopened)    | ✅ Yes (can be extended)       |
| Class Implementation | ✅ Yes | ✅ Yes |

### **When to Use What?**
- Use `interface` when designing object structures, especially when they need to be extended.
- Use `type` when dealing with unions, intersections, primitives, or function signatures.
