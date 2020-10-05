# Ownership

[This concept](https://doc.rust-lang.org/book/ch04-01-what-is-ownership.html) took some getting used to. In JavaScript, memory is allocated when objects are created and then freed when it's no longer needed (aka ["garbage collection"](<https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)>)). The MDN docs outline the typical [memory life cycle](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management):

> 1. Allocate the memory you need
> 2. Use the allocated memory (read, write)
> 3. Release the allocated memory when it is not needed anymore

> The second part is explicit in all languages. The first and last parts are explicit in low-level languages but are mostly implicit in high-level languages like JavaScript.

Rust takes a different approach. According to the docs:

> memory is managed through a system of ownership with a set of rules that the compiler checks at compile time.

When you assign a value to a variable and then pass that variable around, its ownership is also passed around.

## Examples

🅙🅢 JavaScript

```javascript
const greet = (name) => console.log(`Hello ${name}!`);

function main() {
  let name = "Kwame";
  greet(name);
  console.log(name);
}

// Expected Output:
// Hello Kwame!
// Kwame
```

🦀 Rust

```rust
// `&` in front of `String` indicates a reference
fn greet(name: &String) {
    println!("Hello {}!", name);
}

fn main() {
    let name = String::from("Kwame");
    // `&name` creates a reference to the value of `name`.
    // This reference doesn't own the value, so we can pass it
    // to our function and log it out. Otherwise Rust would throw an
    // error since the value would be dropped when the reference goes
    // out of scope.
    greet(&name);
    println!("{}", name);
}

// Expected Output:
// Hello Kwame!
// Kwame
```
