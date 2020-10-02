# Iterations

## Examples

JavaScript

```javascript
function main() {
  [...Array(10).keys()].forEach((key, i) => {
    console.log(`Now serving number ${i + 1}`);
  });
}
```

Rust

```rust
fn main() {
    for i in 0..10 {
        println!("Now serving number {}", i + 1)
    }
}
```
