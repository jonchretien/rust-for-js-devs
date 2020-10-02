# Primitive Types

## Characters

Character literals are represented with a single quote (vs double quote for strings).

🦀 Rust

```rust
fn main() {
    let a = '𝒜';
    let pizza = '🍕';
    let party = '🥳';

    println!("It's {} {} {}!", a, pizza, party);
}
```

## Arrays

Arrays in Rust behave differently than in JavaScript. Each array element must have the same type. They also have a fixed length and should be used for collections whose size isn't going to change. Fortunately there are some alternatives if you need additional functionality:

- I need a collection with different types: [tuple](https://doc.rust-lang.org/book/ch03-02-data-types.html#the-tuple-type)
- I need a collection with flexible sizing: [vector](https://doc.rust-lang.org/std/vec/struct.Vec.html)

**slice**

🅙🅢 JavaScript

```javascript
const roots = [
  "questlove",
  "black thought",
  "james poyser",
  "damon bryson",
  "captain kirk douglas",
];
console.log(roots.slice(1, 4));
// Array ["black thought", "james poyser", "damon bryson"]
```

🦀 Rust

```rust
fn main() {
    let roots = [
        "questlove",
        "black thought",
        "james poyser",
        "damon bryson",
        "captain kirk douglas",
    ];

    // in rust we need to borrow the array above.
    let roots_slice = &roots[1..4];
    println!("roots_slice ->  {:?}", roots_slice);
    // roots_slice ->  ["black thought", "james poyser", "damon bryson"]
}
```

## Tuples

🦀 Rust

```rust
fn main() {
    let musician = ("questlove", 170_000);

    // destructure tuple
    let (name, records) = musician;
    println!("{} has {} records in his collection", name, records);
    // questlove is 49 years old
}
```
