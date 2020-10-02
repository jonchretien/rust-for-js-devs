# Variables

## Similarities with JS

- Block scoped.
- Initialized with `let` or `const`.

## Differences with JS

- Immutable by default(more examples in [mutability](../mutability/README.md)).
- Must be initialized (you can't just do `let x: i32;`).

## Examples

JavaScript

```javascript
function main() {
  const CAR_MILEAGE = 72_468;
  console.log(`my current car mileage is ${CAR_MILEAGE}`);

  let x = 10;
  console.log(`x has the value ${x}`);

  // block scoping
  {
    let x = 45;
    console.log(`x has the value ${x}`);
  }
}
```

Rust

```rust
fn main() {
    // when using const the type of the value must be annotated
    const CAR_MILEAGE: u32 = 72_468;
    println!("my current car mileage is {}", CAR_MILEAGE);

    let x = 10;
    println!("x has the value {}", x);

    // shadowing
    {
        let x = 45;
        println!("x has the value {}", x);
    }
}
```
