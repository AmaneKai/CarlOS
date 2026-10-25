# CarlOS

A minimal x86_64 kernel written in Rust, following
[A Minimal Rust Kernel](https://os.phil-opp.com/minimal-rust-kernel/) from Philipp Oppermann's "Writing an OS in Rust".

It boots and prints "Hello World!" to the VGA text buffer.

## Prerequisites

```bash
rustup component add rust-src llvm-tools-preview
cargo install bootimage
# plus QEMU, e.g. on macOS: brew install qemu
```

The nightly toolchain is selected by `rust-toolchain.toml`.

## Build and run

```bash
cargo run
```

## Layout

```
CarlOS/
├── src/main.rs           # Kernel entry point
├── .cargo/config.toml    # build-std, default target, bootimage runner
├── x86_64-blog_os.json   # Custom target specification
└── rust-toolchain.toml
```
