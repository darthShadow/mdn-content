---
title: "console: table() static method"
short-title: table()
slug: Web/API/console/table_static
page-type: web-api-static-method
browser-compat: api.console.table_static
---

{{APIRef("Console API")}} {{AvailableInWorkers}}

The **`console.table()`** static method displays tabular data as a table.

## Syntax

```js-nolint
console.table(data)
console.table(data, columns)
```

### Parameters

- `data`
  - : The data to display. This must be either an array or an object. Each item in the array, or property in the object, is represented by a row in the table. The first column in the table is labeled `(index)` and its values are the array indices or the property names.

    If the elements in the array, or properties in the object, are themselves arrays or objects, then their items or properties are enumerated in the row, one per column.

    Note that in Firefox, `console.table()` is limited to displaying 1000 rows, including the heading row.

- `columns` {{optional_inline}}
  - : An array which can be used to restrict the columns shown in the table. It contains indices, if each entry of `data` is an array, or property names, if each entry of `data` is an object. The resulting table then includes only columns for items which match the given indices or names.

### Return value

None ({{jsxref("undefined")}}).

## Examples

### Collections of primitive types

The `data` argument may be an array or an object.

```js
// an array of strings

console.table(["apples", "oranges", "bananas"]);
```

| (index) | Values    |
| ------- | --------- |
| 0       | 'apples'  |
| 1       | 'oranges' |
| 2       | 'bananas' |

```js
// an object whose properties are strings

function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const me = new Person("Tyrone", "Jones");

console.table(me);
```

| (index)   | Values   |
| --------- | -------- |
| firstName | 'Tyrone' |
| lastName  | 'Jones'  |

### Collections of compound types

If the elements in the array, or properties in the object, are themselves arrays or objects, then their elements or properties are enumerated in the row, one per column:

```js
// an array of arrays

const people = [
  ["Tyrone", "Jones"],
  ["Janet", "Smith"],
  ["Maria", "Cruz"],
];
console.table(people);
```

| (index) | 0        | 1       |
| ------- | -------- | ------- |
| 0       | 'Tyrone' | 'Jones' |
| 1       | 'Janet'  | 'Smith' |
| 2       | 'Maria'  | 'Cruz'  |

```js
// an array of objects

function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const tyrone = new Person("Tyrone", "Jones");
const janet = new Person("Janet", "Smith");
const maria = new Person("Maria", "Cruz");

console.table([tyrone, janet, maria]);
```

If the array contains objects, then the columns are labeled with the property name.

| (index) | firstName | lastName |
| ------- | --------- | -------- |
| 0       | 'Tyrone'  | 'Jones'  |
| 1       | 'Janet'   | 'Smith'  |
| 2       | 'Maria'   | 'Cruz'   |

```js
// an object whose properties are objects

const family = {};

family.mother = new Person("Janet", "Jones");
family.father = new Person("Tyrone", "Jones");
family.daughter = new Person("Maria", "Jones");

console.table(family);
```

| (index)  | firstName | lastName |
| -------- | --------- | -------- |
| daughter | 'Maria'   | 'Jones'  |
| father   | 'Tyrone'  | 'Jones'  |
| mother   | 'Janet'   | 'Jones'  |

### Restricting the columns displayed

By default, `console.table()` lists all elements in each row. You can use the optional `columns` parameter to select a subset of columns to display:

```js
// an array of objects, logging only firstName

function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const tyrone = new Person("Tyrone", "Jones");
const janet = new Person("Janet", "Smith");
const maria = new Person("Maria", "Cruz");

console.table([tyrone, janet, maria], ["firstName"]);
```

| (index) | firstName |
| ------- | --------- |
| 0       | 'Tyrone'  |
| 1       | 'Janet'   |
| 2       | 'Maria'   |

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Microsoft Edge's documentation for `console.table()`](https://learn.microsoft.com/en-us/microsoft-edge/devtools/console/api#table)
- [Node.js documentation for `console.table()`](https://nodejs.org/docs/latest/api/console.html#consoletabletabulardata-properties)
- [Google Chrome's documentation for `console.table()`](https://developer.chrome.com/docs/devtools/console/api/#table)
