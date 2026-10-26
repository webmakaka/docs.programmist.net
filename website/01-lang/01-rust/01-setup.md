---
layout: page
title: Инсталляция rust в linux
description: Инсталляция rust в linux
keywords: программирование, языки, rust, инсталляция rust в linux
permalink: /lang/rust/setup/
---

<br/>

# Инсталляция rust в linux

<br/>

**Делаю:**  
2026.10.26

<br/>

**Вариант IDE на Rust:**  
https://zed.dev/

<br/>

```shell
$ cd ~/tmp/
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

$ source $HOME/.cargo/env

$ rustup update
```

<br/>

```shell
$ rustc --version
rustc 1.99.1 (58cf8f9c3 2026-10-13)

$ cargo --version
cargo 1.99.1 (5f94df478 2026-08-27)

$ rustup --version
rustup 1.29.2 (d8c92c676 2026-10-21)
```

<br/>

```shell
$ rustup show
Default host: x86_64-unknown-linux-gnu
rustup home:  /home/marley/.rustup

stable-x86_64-unknown-linux-gnu (default)
rustc 1.81.0 (eeb90cda1 2024-09-04)
```

<br/>

```shell
// Использовать последнюю версию rust
// $ rustup override set nightly

// Использовать стабильную версию rust
$ rustup override set stable
```

<br/>

### Дополнительные пакеты

<br/>

```shell
// Linting
$ rustup component add clippy

// Formatting
$ rustup component add rustfmt
```

<br/>

```shell
// Monitors your source code to trigger commands every time a file changes
$ cargo install cargo-watch

// Code Coverage
$ sudo apt install -y pkg-config libssl-dev
$ cargo install cargo-tarpaulin

// Security Vulnerabilities
$ cargo install cargo-audit
```

<br/>

### rust-analyzer

https://github.com/rust-analyzer/rust-analyzer

<br/>

```shell
$ cd ~/apps/
$ git clone https://github.com/rust-analyzer/rust-analyzer
$ cd rust-analyzer/

$ rustup update
$ cargo xtask install --server
```

<br/>

```shell
$ rust-analyzer --version
rust-analyzer 0.0.0 (0c4d74686b 2026-10-22)
```

<br/>

### VSCode extensions

<br/>

```shell
Ctrl+P

// rust-analyzer
ext install rust-lang.rust-analyzer

// CodeLLDB
ext install vadimcn.vscode-lldb

// crates
ext install serayuzgur.crates

// Even Better TOML
ext install tamasfe.even-better-toml
```

<br/>

```
^P
> Settings JSON
```

<br/>

```
"rust-analyzer.check.command": "clippy",
```

<br/>

### Приложение для примера

https://github.com/alfredodeza/rust-cli-example/tree/main
