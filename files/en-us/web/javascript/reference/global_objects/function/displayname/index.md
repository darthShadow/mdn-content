---
title: "Function: displayName"
short-title: displayName
slug: Web/JavaScript/Reference/Global_Objects/Function/displayName
page-type: javascript-instance-data-property
status:
  - non-standard
browser-compat: javascript.builtins.Function.displayName
sidebar: jsref
---

{{Non-standard_Header}}

The optional **`displayName`** property of a {{jsxref("Function")}} instance specifies the display name of the function.

## Value

The `displayName` property is not initially present on any function — it's added by the code authors. For the purpose of display, it should be a string.

## Description

The `displayName` property, if present, may be preferred by consoles and profilers over the {{jsxref("Function/name", "name")}} property to be displayed as the name of a function.

Among browsers, only the Firefox console utilizes this property. React devtools also use the [`displayName`](https://legacy.reactjs.org/docs/higher-order-components.html#convention-wrap-the-display-name-for-easy-debugging) property when displaying the component tree.

Firefox does some basic attempts to decode the `displayName` that's possibly generated by the [anonymous JavaScript functions naming convention](https://johnjbarton.github.io/nonymous/index.html) algorithm. The following patterns are detected:

- If `displayName` ends with a sequence of alphanumeric characters, `_`, and `$`, the longest such suffix is displayed.
- If `displayName` ends with a sequence of `[]`-enclosed characters, that sequence is displayed without the square brackets.
- If `displayName` ends with a sequence of alphanumeric characters and `_` followed by some `/`, `.`, or `<`, the sequence is returned without the trailing `/`, `.`, or `<` characters.
- If `displayName` ends with a sequence of alphanumeric characters and `_` followed by `(^)`, the sequence is displayed without the `(^)`.

If none of the above patterns match, the entire `displayName` is displayed.

## Examples

### Setting a displayName

By entering the following in a Firefox console, it should display as something like `function MyFunction()`:

```js
function a() {}
a.displayName = "MyFunction";

a; // function MyFunction()
```

### Changing displayName dynamically

You can dynamically change the `displayName` of a function:

```js
const object = {
  // anonymous
  someMethod: function someMethod(value) {
    someMethod.displayName = `someMethod (${value})`;
  },
};

console.log(object.someMethod.displayName); // undefined

object.someMethod("123");
console.log(object.someMethod.displayName); // "someMethod (123)"
```

### Cleaning of displayName

Firefox devtools would clean up a few common patterns in the `displayName` property before displaying it.

```js
function foo() {}

function testName(name) {
  foo.displayName = name;
  console.log(foo);
}

testName("$foo$"); // function $foo$()
testName("foo bar"); // function bar()
testName("Foo.prototype.add"); // function add()
testName("foo ."); // function foo .()
testName("foo <"); // function foo <()
testName("foo?"); // function foo?()
testName("foo()"); // function foo()()

testName("[...]"); // function ...()
testName("foo<"); // function foo()
testName("foo..."); // function foo()
testName("foo(^)"); // function foo()
```

## Specifications

Not part of any standard.

## Browser compatibility

{{Compat}}

## See also

- {{jsxref("Function.prototype.name")}}
