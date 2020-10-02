# Structs

You can define related data with structs. They can be multiple related values that make a group. It's similar to an object in JavaScript except they're not mutable by default and are checked at compile time.

## Examples

Classic Struct

🦀 Rust

```rust
#[derive(Debug)]
struct ReleaseStruct {
    artist: String,
    title: String,
    genre: String,
    style: String,
    year: u32,
    on_streaming_services: bool,
}

fn main() {
    // create an instance of the struct by specifying concrete values for each of the fields
    let album = ReleaseStruct {
        artist: String::from("John Coltrane"),
        title: String::from("A Love Supreme"),
        genre: String::from("Jazz"),
        style: String::from("Free Jazz"),
        year: 1965,
        on_streaming_services: true,
    };

    println!("{} released {} in {}", album.artist, album.title, album.year);
    // John Coltrane released A Love Supreme in 1965

    println!("{:?}", album);
    // ReleaseStruct { artist: "John Coltrane", album: "A Love Supreme", genre: "Jazz", style: "Free Jazz", year: 1965, on_streaming_services: true }
}
```
