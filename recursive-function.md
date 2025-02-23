Here's a simple recursive function in TypeScript that calculates the factorial of a number:  

```typescript
function factorial(n: number): number {
  if (n <= 1) {
    return 1;
  }
  return n * factorial(n - 1);
}

console.log(factorial(5)); // Output: 120
```

This function calls itself with `n - 1` until it reaches the base case (`n <= 1`). Let me know if you need a different example! 🚀
