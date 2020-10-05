# Functions

Functions are declared using `snake_case`, and the `main` function will be the entry to most of your applications.

## Examples

**Declaring the return type of a function**

You must declare them in type signatures. Also note that if a semicolon is added to the end of the expression, it turns that into a statement. Statements [don't return a value](https://doc.rust-lang.org/book/ch03-03-how-functions-work.html#function-bodies-contain-statements-and-expressions).

🅙🅢 JavaScript

```javascript
function calculateSalesTax(a) {
  const SALES_TAX = 0.8;
  return a * SALES_TAX;
}

function main() {
  let salesTax = calculateSalesTax(54.99);
  console.log(`Total bill is $${salesTax.toFixed(2)}`);
}
```

🦀 Rust

```rust
fn calculate_sales_tax(a: f64) -> f64 {
    const SALES_TAX: f64 = 0.8;
    a * SALES_TAX
}

fn main() {
    let sales_tax = calculate_sales_tax(54.99);
    println!("Total bill is ${:.2}", sales_tax);
}
```

**Implicit return values**

🅙🅢 JavaScript

```javascript
const sum = (a, b) => a + b;
sum(4, 5);
```

🦀 Rust

```rust
fn sum(a: i32, b: i32) -> i32 {
    a + b
}

fn main() {
    sum(4, 5);
}
```

**Explicit return values**

🅙🅢 JavaScript

```javascript
const sum = (a, b) => {
  return a + b;
};

sum(4, 5);
```

🦀 Rust

```rust
fn sum(a: i32, b: i32) -> i32 {
    return a + b;
}

fn main() {
    sum(4, 5);
}
```
