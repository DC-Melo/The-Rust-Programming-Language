# The-Rust-Programming-Language
rust language code base on https://doc.rust-lang.org/book/ch01-02-hello-world.html

This tutorial is base on [The Rust Programming Language](https://doc.rust-lang.org/book/title-page.html) 
## Table of Contents

- [Foreword](#foreword)
- [Introduction](#introduction)
- [1. Getting Started](#1-getting-started)
  - [1.1. Installation](#11-installation)
  - [1.2. Hello, World!](#12-hello-world)
  - [1.3. Hello, Cargo!](#13-hello-cargo)
- [2. Programming a Guessing Game](#2-programming-a-guessing-game)
- [3. Common Programming Concepts](#3-common-programming-concepts)
  - [3.1. Variables and Mutability](#31-variables-and-mutability)
  - [3.2. Data Types](#32-data-types)
  - [3.3. Functions](#33-functions)
  - [3.4. Comments](#34-comments)
  - [3.5. Control Flow](#35-control-flow)
- [4. Understanding Ownership](#4-understanding-ownership)
  - [4.1. What is Ownership?](#41-what-is-ownership)
  - [4.2. References and Borrowing](#42-references-and-borrowing)
  - [4.3. The Slice Type](#43-the-slice-type)
- [5. Using Structs to Structure Related Data](#5-using-structs-to-structure-related-data)
  - [5.1. Defining and Instantiating Structs](#51-defining-and-instantiating-structs)
  - [5.2. An Example Program Using Structs](#52-an-example-program-using-structs)
  - [5.3. Method Syntax](#53-method-syntax)
- [6. Enums and Pattern Matching](#6-enums-and-pattern-matching)
  - [6.1. Defining an Enum](#61-defining-an-enum)
  - [6.2. The match Control Flow Construct](#62-the-match-control-flow-construct)
  - [6.3. Concise Control Flow with if let](#63-concise-control-flow-with-if-let)
- [7. Managing Growing Projects with Packages, Crates, and Modules](#7-managing-growing-projects-with-packages-crates-and-modules)
  - [7.1. Packages and Crates](#71-packages-and-crates)
  - [7.2. Defining Modules to Control Scope and Privacy](#72-defining-modules-to-control-scope-and-privacy)
  - [7.3. Paths for Referring to an Item in the Module Tree](#73-paths-for-referring-to-an-item-in-the-module-tree)
  - [7.4. Bringing Paths Into Scope with the use Keyword](#74-bringing-paths-into-scope-with-the-use-keyword)
  - [7.5. Separating Modules into Different Files](#75-separating-modules-into-different-files)
- [8. Common Collections](#8-common-collections)
  - [8.1. Storing Lists of Values with Vectors](#81-storing-lists-of-values-with-vectors)
  - [8.2. Storing UTF-8 Encoded Text with Strings](#82-storing-utf-8-encoded-text-with-strings)
  - [8.3. Storing Keys with Associated Values in Hash Maps](#83-storing-keys-with-associated-values-in-hash-maps)
- [9. Error Handling](#9-error-handling)
  - [9.1. Unrecoverable Errors with panic!](#91-unrecoverable-errors-with-panic)
  - [9.2. Recoverable Errors with Result](#92-recoverable-errors-with-result)
  - [9.3. To panic! or Not to panic!](#93-to-panic-or-not-to-panic)
- [10. Generic Types, Traits, and Lifetimes](#10-generic-types-traits-and-lifetimes)
  - [10.1. Generic Data Types](#101-generic-data-types)
  - [10.2. Traits: Defining Shared Behavior](#102-traits-defining-shared-behavior)
  - [10.3. Validating References with Lifetimes](#103-validating-references-with-lifetimes)
- [11. Writing Automated Tests](#11-writing-automated-tests)
  - [11.1. How to Write Tests](#111-how-to-write-tests)
  - [11.2. Controlling How Tests Are Run](#112-controlling-how-tests-are-run)
  - [11.3. Test Organization](#113-test-organization)
- [12. An I/O Project: Building a Command Line Program](#12-an-io-project-building-a-command-line-program)
  - [12.1. Accepting Command Line Arguments](#121-accepting-command-line-arguments)
  - [12.2. Reading a File](#122-reading-a-file)
  - [12.3. Refactoring to Improve Modularity and Error Handling](#123-refactoring-to-improve-modularity-and-error-handling)
  - [12.4. Developing the Library’s Functionality with Test Driven Development](#124-developing-the-librarys-functionality-with-test-driven-development)
  - [12.5. Working with Environment Variables](#125-working-with-environment-variables)
  - [12.6. Writing Error Messages to Standard Error Instead of Standard Output](#126-writing-error-messages-to-standard-error-instead-of-standard-output)
- [13. Functional Language Features: Iterators and Closures](#13-functional-language-features-iterators-and-closures)
  - [13.1. Closures: Anonymous Functions that Capture Their Environment](#131-closures-anonymous-functions-that-capture-their-environment)
  - [13.2. Processing a Series of Items with Iterators](#132-processing-a-series-of-items-with-iterators)
  - [13.3. Improving Our I/O Project](#133-improving-our-io-project)
  - [13.4. Comparing Performance: Loops vs. Iterators](#134-comparing-performance-loops-vs-iterators)
- [14. More about Cargo and Crates.io](#14-more-about-cargo-and-cratesio)
  - [14.1. Customizing Builds with Release Profiles](#141-customizing-builds-with-release-profiles)
  - [14.2. Publishing a Crate to Crates.io](#142-publishing-a-crate-to-cratesio)
  - [14.3. Cargo Workspaces](#143-cargo-workspaces)
  - [14.4. Installing Binaries from Crates.io with cargo install](#144-installing-binaries-from-cratesio-with-cargo-install)
  - [14.5. Extending Cargo with Custom Commands](#145-extending-cargo-with-custom-commands)
- [15. Smart Pointers](#15-smart-pointers)
  - [15.1. Using Box<T> to Point to Data on the Heap](#151-using-boxt-to-point-to-data-on-the-heap)
  - [15.2. Treating Smart Pointers Like Regular References with the Deref Trait](#152-treating-smart-pointers-like-regular-references-with-the-deref-trait)
  - [15.3. Running Code on Cleanup with the Drop Trait](#153-running-code-on-cleanup-with-the-drop-trait)
  - [15.4. Rc<T>, the Reference Counted Smart Pointer](#154-rct-the-reference-counted-smart-pointer)
  - [15.5. RefCell<T> and the Interior Mutability Pattern](#155-refcellt-and-the-interior-mutability-pattern)
  - [15.6. Reference Cycles Can Leak Memory](#156-reference-cycles-can-leak-memory)
- [16. Fearless Concurrency](#16-fearless-concurrency)
  - [16.1. Using Threads to Run Code Simultaneously](#161-using-threads-to-run-code-simultaneously)
  - [16.2. Using Message Passing to Transfer Data Between Threads](#162-using-message-passing-to-transfer-data-between-threads)
  - [16.3. Shared-State Concurrency](#163-shared-state-concurrency)
  - [16.4. Extensible Concurrency with the Sync and Send Traits](#164-extensible-concurrency-with-the-sync-and-send-traits)
- [17. Object Oriented Programming Features of Rust](#17-object-oriented-programming-features-of-rust)
  - [17.1. Characteristics of Object-Oriented Languages](#171-characteristics-of-object-oriented-languages)
  - [17.2. Using Trait Objects That Allow for Values of Different Types](#172-using-trait-objects-that-allow-for-values-of-different-types)
  - [17.3. Implementing an Object-Oriented Design Pattern](#173-implementing-an-object-oriented-design-pattern)
- [18. Patterns and Matching](#18-patterns-and-matching)
  - [18.1. All the Places Patterns Can Be Used](#181-all-the-places-patterns-can-be-used)
  - [18.2. Refutability: Whether a Pattern Might Fail to Match](#182-refutability-whether-a-pattern-might-fail-to-match)
  - [18.3. Pattern Syntax](#183-pattern-syntax)
- [19. Advanced Features](#19-advanced-features)
  - [19.1. Unsafe Rust](#191-unsafe-rust)
  - [19.2. Advanced Traits](#192-advanced-traits)
  - [19.3. Advanced Types](#193-advanced-types)
  - [19.4. Advanced Functions and Closures](#194-advanced-functions-and-closures)
  - [19.5. Macros](#195-macros)
- [20. Final Project: Building a Multithreaded Web Server](#20-final-project-building-a-multithreaded-web-server)
  - [20.1. Building a Single-Threaded Web Server](#201-building-a-single-threaded-web-server)
  - [20.2. Turning Our Single-Threaded Server into a Multithreaded Server](#202-turning-our-single-threaded-server-into-a-multithreaded-server)
  - [20.3. Graceful Shutdown and Cleanup](#203-graceful-shutdown-and-cleanup)
- [21. Appendix](#21-appendix)
  - [21.1. A - Keywords](#211-a---keywords)
  - [21.2. B - Operators and Symbols](#212-b---operators-and-symbols)
  - [21.3. C - Derivable Traits](#213-c---derivable-traits)
  - [21.4. D - Useful Development Tools](#214-d---useful-development-tools)
  - [21.5. E - Editions](#215-e---editions)
  - [21.6. F - Translations of the Book](#216-f---translations-of-the-book)
  - [21.7. G - How Rust is Made and “Nightly Rust”](#217-g---how-rust-is-made-and-nightly-rust)


## The Rust Programming Language
## Foreword
## Introduction
## 1. Getting Started
### 1.1. Installation
### 1.2. Hello, World!
Now open the main.rs file you just created and enter the code in Listing 1-1.
Filename: main.rs
```rs
fn main() {
    println!("Hello, world!");
}
```
enter the following commands to compile and run the file:
```sh
❯ rustc main.rs
❯ rustc main.rs
❯ ./main
Hello, world!
```
### 1.3. Hello, Cargo!
- Install Cargo and use Cargo to make projects.
```sh
❯ cargo --version                                                                              
cargo 1.75.0 (1d8b05cdd 2023-11-20)
```
- Creating a Project with Cargo
```
❯ cargo new hello_cargo
     Created binary (application) `hello_cargo` package
❯ cd hello_cargo
```
- Building and Running a Cargo Project
```sh
❯ cargo build
   Compiling hello_cargo v0.1.0 (/home/dc/5W/github/DC-Melo/The-Rust-Programming-Language/01-Getting
-Started/1.3.Hello-Cargo/hello_cargo)
    Finished dev [unoptimized + debuginfo] target(s) in 0.15s
# run the executable with this command:
❯ ./target/debug/hello_cargo
Hello, world!
# we can also use cargo run to compile the code and then run the resultant executable all in one command:
❯ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/hello_cargo`
Hello, world!
# cargo check. This command quickly checks your code to make sure it compiles but doesn’t produce an executable:
❯ cargo check
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
```
- Building for Release 
```sh 
❯ cargo build --release
   Compiling hello_cargo v0.1.0 (/home/dc/5W/github/DC-Melo/The-Rust-Programming-Language/01-Getting
-Started/1.3.Hello-Cargo/hello_cargo)
    Finished release [optimized] target(s) in 0.15s
```

## 2. Programming a Guessing Game
- Setting Up a New Project
```sh
❯ cargo new guessing_game
     Created binary (application) `guessing_game` package
dc in 🌐 dc-iMac in The-Rust-Programming-Language/02-Programming-a-Guessing-Game on  02.Programming-a-Guessing-Game [!?] 
❯ cd guessing_game
dc in 🌐 dc-iMac in The-Rust-Programming-Language/02-Programming-a-Guessing-Game/guessing_game on  02.Programming-a-Guessing-Game [!?] is 📦
 v0.1.0 via 🦀 v1.75.0 
❯ cargo run
   Compiling guessing_game v0.1.0 (/home/dc/5W/github/DC-Melo/The-Rust-Programming-Language/02-Programming-a-Guessing-Game/guessing_game)
    Finished dev [unoptimized + debuginfo] target(s) in 0.16s
     Running `target/debug/guessing_game`
Hello, world!
```
- Processing a Guess
Filename: src/main.rs

```rs
use std::io;

fn main() {
    println!("Guess the number!");

    println!("Please input your guess.");

    let mut guess = String::new();

    io::stdin()
        .read_line(&mut guess)
        .expect("Failed to read line");

    println!("You guessed: {guess}");
}
```

```sh
❯ cargo build
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
❯ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/guessing_game`
Guess the number!
Please input your guess.
10
You guessed: 10
```



## 3. Common Programming Concepts
### 3.1. Variables and Mutability
### 3.2. Data Types
### 3.3. Functions
### 3.4. Comments
### 3.5. Control Flow
## 4. Understanding Ownership
### 4.1. What is Ownership?
### 4.2. References and Borrowing
### 4.3. The Slice Type
## 5. Using Structs to Structure Related Data
### 5.1. Defining and Instantiating Structs
### 5.2. An Example Program Using Structs
### 5.3. Method Syntax
## 6. Enums and Pattern Matching
### 6.1. Defining an Enum
### 6.2. The match Control Flow Construct
### 6.3. Concise Control Flow with if let
## 7. Managing Growing Projects with Packages, Crates, and Modules
### 7.1. Packages and Crates
### 7.2. Defining Modules to Control Scope and Privacy
### 7.3. Paths for Referring to an Item in the Module Tree
### 7.4. Bringing Paths Into Scope with the use Keyword
### 7.5. Separating Modules into Different Files
## 8. Common Collections
### 8.1. Storing Lists of Values with Vectors
### 8.2. Storing UTF-8 Encoded Text with Strings
### 8.3. Storing Keys with Associated Values in Hash Maps
## 9. Error Handling
### 9.1. Unrecoverable Errors with panic!
### 9.2. Recoverable Errors with Result
### 9.3. To panic! or Not to panic!
## 10. Generic Types, Traits, and Lifetimes
### 10.1. Generic Data Types
### 10.2. Traits: Defining Shared Behavior
### 10.3. Validating References with Lifetimes
## 11. Writing Automated Tests
### 11.1. How to Write Tests
### 11.2. Controlling How Tests Are Run
### 11.3. Test Organization
## 12. An I/O Project: Building a Command Line Program
### 12.1. Accepting Command Line Arguments
### 12.2. Reading a File
### 12.3. Refactoring to Improve Modularity and Error Handling
### 12.4. Developing the Library’s Functionality with Test Driven Development
### 12.5. Working with Environment Variables
### 12.6. Writing Error Messages to Standard Error Instead of Standard Output
## 13. Functional Language Features: Iterators and Closures
### 13.1. Closures: Anonymous Functions that Capture Their Environment
### 13.2. Processing a Series of Items with Iterators
### 13.3. Improving Our I/O Project
### 13.4. Comparing Performance: Loops vs. Iterators
## 14. More about Cargo and Crates.io
### 14.1. Customizing Builds with Release Profiles
### 14.2. Publishing a Crate to Crates.io
### 14.3. Cargo Workspaces
### 14.4. Installing Binaries from Crates.io with cargo install
### 14.5. Extending Cargo with Custom Commands
## 15. Smart Pointers
### 15.1. Using Box<T> to Point to Data on the Heap
### 15.2. Treating Smart Pointers Like Regular References with the Deref Trait
### 15.3. Running Code on Cleanup with the Drop Trait
### 15.4. Rc<T>, the Reference Counted Smart Pointer
### 15.5. RefCell<T> and the Interior Mutability Pattern
### 15.6. Reference Cycles Can Leak Memory
## 16. Fearless Concurrency
### 16.1. Using Threads to Run Code Simultaneously
### 16.2. Using Message Passing to Transfer Data Between Threads
### 16.3. Shared-State Concurrency
### 16.4. Extensible Concurrency with the Sync and Send Traits
## 17. Object Oriented Programming Features of Rust
### 17.1. Characteristics of Object-Oriented Languages
### 17.2. Using Trait Objects That Allow for Values of Different Types
### 17.3. Implementing an Object-Oriented Design Pattern
## 18. Patterns and Matching
### 18.1. All the Places Patterns Can Be Used
### 18.2. Refutability: Whether a Pattern Might Fail to Match
### 18.3. Pattern Syntax
## 19. Advanced Features
### 19.1. Unsafe Rust
### 19.2. Advanced Traits
### 19.3. Advanced Types
### 19.4. Advanced Functions and Closures
### 19.5. Macros
## 20. Final Project: Building a Multithreaded Web Server
### 20.1. Building a Single-Threaded Web Server
### 20.2. Turning Our Single-Threaded Server into a Multithreaded Server
### 20.3. Graceful Shutdown and Cleanup
## 21. Appendix
### 21.1. A - Keywords
### 21.2. B - Operators and Symbols
### 21.3. C - Derivable Traits
### 21.4. D - Useful Development Tools
### 21.5. E - Editions
### 21.6. F - Translations of the Book
### 21.7. G - How Rust is Made and “Nightly Rust”

