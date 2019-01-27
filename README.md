# **Rust play**

Collection of **rust** programs from the official book [The Rust Programming Language](https://doc.rust-lang.org/book/index.html).

### **TOC**

1. [Setup](#setup)
2. [Usage](#usage)
3. [Playground](#playground)
4. [Docker](#docker)
5. [Resources](#resources)
6. [Doc](#doc)
7. [License](#license)

### **Setup**

To start to use **rust** on **UNIX-like** system it's enough to run using [rustup](https://rustup.rs/):

```shell
$ curl https://sh.rustup.rs -sSf | sh
```

to install the latest stable version and add this line to your `rc` file
to add **cargo** to your system `PATH`:

```shell
export PATH="$HOME/.cargo/bin:$PATH"
```

### **Usage**

Firstly check if **rust** and **cargo** are properly set:

```shell
$ rustc -V; cargo -V
```

If all is good the output will show the **version** of both binaries.

:crab:

There are 2 different ways to compile **rust** programs.

**Rustc**

The 1st using the compiler `rustc`. So starting from a classic `hello.rs`:

```rust
fn main() {
    println!("Hello, world!");
}
```

To compile our function:

```shell
$ rustc hello.rs
```

This will create a binary called `hello`, that will print the string `Hello, World!`.

**Cargo**

The 2nd using the package manager `cargo`. So running:

```shell
$ cargo new hello_world
```

we can create our first **rust** package and have a structure like the following:

```shell
$ cd hello_world
$ tree .
.
├── Cargo.toml
└── src
    └── main.rs

1 directory, 2 files
```

To interact with this package there are several options:

```shell
$ cargo check # To check if is error-proof
$ cargo build # To compile our package and store the binary under target/debug
$ cargo build --release # To compile our package and store the binary under target/release
$ cargo run # To run our binary
```

### **Playground**

![cup](img/cup.jpg)

+ [hello_cargo](hello_cargo)
+ [guessing_game](guessing_game)

_Hack without fear!_

### **Docker**

The official docker images:

+ [rust](https://hub.docker.com/_/rust)

### **Resources**

+ [into_rust()](http://intorust.com/)

### **Doc**

+ [Rust Documentation](https://doc.rust-lang.org/)

### **License**

This work is unlicensed under the terms of [Unlicense](http://unlicense.org/).
