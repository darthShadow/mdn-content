---
title: WebAssembly
slug: WebAssembly
page-type: landing-page
browser-compat:
  - webassembly.api
  - webassembly.BigInt-to-i64-integration
  - webassembly.bulk-memory-operations
  - webassembly.exception-handling
  - webassembly.extended-constant-expressions
  - webassembly.fixed-width-SIMD
  - webassembly.garbage-collection
  - webassembly.multiMemory
  - webassembly.multi-value
  - webassembly.mutable-globals
  - webassembly.non-trapping-float-to-int-conversions
  - webassembly.reference-types
  - webassembly.sign-extension-operations
  - webassembly.tail-calls
  - webassembly.threads-and-atomics
sidebar: webassemblysidebar
---

WebAssembly is a type of code that can be run in modern web browsers.
It is a low-level assembly-like language with a compact binary format that runs with near-native performance and provides languages such as C/C++, C# and Rust with a compilation target so that they can run on the web.
It is also designed to run alongside JavaScript, allowing both to work together.

WebAssembly is designed to complement and run alongside JavaScript — using the WebAssembly JavaScript APIs, you can load WebAssembly modules into a JavaScript app and share functionality between the two. This allows you to take advantage of WebAssembly's performance and power and JavaScript's expressiveness and flexibility in the same app, even if you don't know how to write WebAssembly code.

WebAssembly has big implications for the web platform, not only because it provides a way for code written in multiple languages to run on the web at near-native speed, but also because it enables client apps to run on the web that previously could not.

And what's even better is that it is being developed as a web standard via the [W3C WebAssembly Working Group](https://www.w3.org/groups/wg/wasm/) and [Community Group](https://www.w3.org/community/webassembly/) with active participation from all major browser vendors.

## Guides

The [WebAssembly guides](/en-US/docs/WebAssembly/Guides) cover topics such as high-level concepts, compiling from different languages, the textual representation of the Wasm binary format, and how to run WebAssembly.

- [WebAssembly concepts](/en-US/docs/WebAssembly/Guides/Concepts)
  - : Get started by reading the high-level concepts behind WebAssembly — what it is, why it is so useful, how it fits into the web platform (and beyond), and how to use it.
- [Compiling a new C/C++ module to WebAssembly](/en-US/docs/WebAssembly/Guides/C_to_Wasm)
  - : When you've written code in C/C++, you can then compile it into Wasm using a tool like [Emscripten](https://emscripten.org/). Let's look at how it works.
- [Compiling an existing C module to WebAssembly](/en-US/docs/WebAssembly/Guides/Existing_C_to_Wasm)
  - : A core use-case for WebAssembly is to take the existing ecosystem of C libraries and allow developers to use them on the web.
- [Compiling from Rust to WebAssembly](/en-US/docs/WebAssembly/Guides/Rust_to_Wasm)
  - : If you've written some Rust code, you can compile it into WebAssembly! This tutorial takes you through all you need to know to compile a Rust project to Wasm and use it in an existing web app.
- [Loading and running WebAssembly code](/en-US/docs/WebAssembly/Guides/Loading_and_running)
  - : After you have a Wasm module, this article covers how to fetch, compile and instantiate it, combining the [WebAssembly JavaScript](/en-US/docs/WebAssembly/Reference/JavaScript_interface) API with the [Fetch](/en-US/docs/Web/API/Fetch_API) or [XHR](/en-US/docs/Web/API/XMLHttpRequest) APIs.
- [Using the WebAssembly JavaScript API](/en-US/docs/WebAssembly/Guides/Using_the_JavaScript_API)
  - : Once you've loaded a Wasm module, you'll want to use it. In this article, we show you how to use WebAssembly via the WebAssembly JavaScript API.
- [Exported WebAssembly functions](/en-US/docs/WebAssembly/Guides/Exported_functions)
  - : Exported WebAssembly functions are the JavaScript reflections of WebAssembly functions, which allow calling WebAssembly code from JavaScript. This article describes what they are.
- [Understanding WebAssembly text format](/en-US/docs/WebAssembly/Guides/Understanding_the_text_format)
  - : This article explains the Wasm text format. This is the low-level textual representation of a Wasm module shown in browser developer tools when debugging.
- [Converting WebAssembly text format to Wasm](/en-US/docs/WebAssembly/Guides/Text_format_to_Wasm)
  - : This article provides a guide on how to convert a WebAssembly module written in text format into a Wasm binary.

## API reference

- [WebAssembly instruction reference](/en-US/docs/WebAssembly/Reference)
  - : Reference documentation with interactive samples for the set of WebAssembly operators.
- [WebAssembly JavaScript interface](/en-US/docs/WebAssembly/Reference/JavaScript_interface)
  - : This object acts as the namespace for all WebAssembly-related functionality.
- [`WebAssembly.Global()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Global)
  - : A `WebAssembly.Global` object represents a global variable instance, accessible from both JavaScript and importable/exportable across one or more [`WebAssembly.Module`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Module) instances. This allows dynamic linking of multiple modules.
- [`WebAssembly.Module()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Module)
  - : A `WebAssembly.Module` object contains stateless WebAssembly code that has already been compiled by the browser and can be efficiently [shared with Workers](/en-US/docs/Web/API/Worker/postMessage), and instantiated multiple times.
- [`WebAssembly.Instance()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Instance)
  - : A `WebAssembly.Instance` object is a stateful, executable instance of a `Module`. `Instance` objects contain all the [Exported WebAssembly functions](/en-US/docs/WebAssembly/Guides/Exported_functions) that allow calling into WebAssembly code from JavaScript.
- [`WebAssembly.compile()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/compile_static)
  - : The `WebAssembly.compile()` function compiles WebAssembly binary code into a `WebAssembly.Module` object.
- [`WebAssembly.compileStreaming()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/compileStreaming_static)
  - : The `WebAssembly.compileStreaming()` function compiles a `WebAssembly.Module` directly from a streamed underlying source.
- [`WebAssembly.instantiate()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/instantiate_static)
  - : The `WebAssembly.instantiate()` function allows you to compile and instantiate WebAssembly code.
- [`WebAssembly.instantiateStreaming()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/instantiateStreaming_static)
  - : The `WebAssembly.instantiateStreaming()` function is the primary API for compiling and instantiating WebAssembly code, returning both a `Module` and its first `Instance`.
- [`WebAssembly.validate()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/validate_static)
  - : The `WebAssembly.validate()` function validates a given typed array of WebAssembly binary code.
- [`WebAssembly.Memory()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Memory)
  - : A `WebAssembly.Memory` object is a resizable {{jsxref("Global_objects/ArrayBuffer", "ArrayBuffer")}} that holds the raw bytes of memory accessed by an `Instance`.
- [`WebAssembly.Table()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Table)
  - : A `WebAssembly.Table` object is a resizable typed array of opaque values, like function references, that are accessed by an `Instance`.
- [`WebAssembly.Tag()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Tag)
  - : The `WebAssembly.Tag` object defines a type of WebAssembly exception that can be thrown to/from WebAssembly code.
- [`WebAssembly.Exception()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/Exception)
  - : The `WebAssembly.Exception` object represents a runtime exception thrown from WebAssembly to JavaScript, or thrown from JavaScript to a WebAssembly exception handler.
- [`WebAssembly.CompileError()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/CompileError)
  - : Creates a new WebAssembly `CompileError` object.
- [`WebAssembly.LinkError()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/LinkError)
  - : Creates a new WebAssembly `LinkError` object.
- [`WebAssembly.RuntimeError()`](/en-US/docs/WebAssembly/Reference/JavaScript_interface/RuntimeError)
  - : Creates a new WebAssembly `RuntimeError` object.

## Example projects

- [WASMSobel](https://github.com/JasonWeathersby/WASMSobel)
- See our [webassembly-examples](https://github.com/mdn/webassembly-examples/) repo for a number of other examples.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [WebAssembly on Mozilla Research](https://research.mozilla.org/)
- [webassembly.org](https://webassembly.org/)
- [WebAssembly articles on Mozilla Hacks blog](https://hacks.mozilla.org/category/webassembly/)
- [W3C WebAssembly Community Group](https://www.w3.org/community/webassembly/)
- [Emscripting a C Library to Wasm](https://web.dev/articles/emscripting-a-c-library)
