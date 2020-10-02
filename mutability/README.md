# Mutability

Variables are immutable by default. You can change that by adding the `mut` keyword.

## Examples

🅙🅢 JavaScript

```javascript
function main() {
  let breakfast = "cereal";
  console.log(`This morning's breakfast was ${breakfast}`);

  breakfast = "waffles";
  console.log(`This morning's breakfast was ${breakfast}`);
}
```

🦀 Rust

```rust
fn main() {
    // this would throw an error since `breakfast` is immutable:
    // let breakfast = "cereal";
    // breakfast = "waffles";

    let mut breakfast = "cereal";
    println!("This morning's breakfast was {}", breakfast);

    breakfast = "waffles";
    println!("This morning's breakfast was {}", breakfast);
}
```
