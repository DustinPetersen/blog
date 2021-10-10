---
layout: post
title: javascript One-liners
date: 2021-10-08 21:48 -0600
categories:
tags: [JavaScript]
---
# DOM
## Check if an element is focused
~~~ javascript
const hasFocus = (ele) => ele === document.activeElement;
~~~
##Get all siblings of an element
~~~ javascript
const siblings = (ele) => [].slice.call(ele.parentNode.children).filter((child) => child !== ele);
~~~
##Get selected text
~~~ javascript
const getSelectedText = () => window.getSelection().toString();
~~~
##Go back to the previous page
~~~ javascript
history.back();
// Or
history.go(-1);
~~~
##Clear all cookies
~~~ javascript
const clearCookies = () => document.cookie
.split(';')
.forEach((c) =>(document.cookie = c.replace(/^ +/, '').replace(/=.*/, `=;expires=${new Date().toUTCString()};path=/`)));
Convert cookie to object
const cookies = document.cookie.split(';').map((item) => item.split('=')).reduce((acc, [k, v]) => (acc[k.trim().replace('"', '')] = v) && acc, {});
~~~
# Arrays

## Compare two arrays
~~~ javascript
// `a` and `b` are arrays
const isEqual = (a, b) => JSON.stringify(a) === JSON.stringify(b);
// Or
const isEqual = (a, b) => a.length === b.length && a.every((v, i) => v === b[i]);
// Examples
isEqual([1, 2, 3], [1, 2, 3]); // true
isEqual([1, 2, 3], [1, '2', 3]); // false
~~~
## Convert an array of objects to a single object
~~~ javascript
const toObject = (arr, key) => arr.reduce((a, b) => ({ ...a, [b[key]]: b }), {});
// Or
const toObject = (arr, key) => Object.fromEntries(arr.map((it) => [it[key], it]));
// Example
toObject([
{ id: '1', name: 'Alpha', gender: 'Male' },
{ id: '2', name: 'Bravo', gender: 'Male' },
{ id: '3', name: 'Charlie', gender: 'Female' }],
'id');
/*
{
'1': { id: '1', name: 'Alpha', gender: 'Male' },
'2': { id: '2', name: 'Bravo', gender: 'Male' },
'3': { id: '3', name: 'Charlie', gender: 'Female' }
}
*/
~~~

## Count by the properties of an array of objects
~~~ javascript
const countBy = (arr, prop) => arr.reduce((prev, curr) => ((prev[curr[prop]] = ++prev[curr[prop]] || 1), prev), {});
// Example
countBy([
{ branch: 'audi', model: 'q8', year: '2019' },
{ branch: 'audi', model: 'rs7', year: '2020' },
{ branch: 'ford', model: 'mustang', year: '2019' },
{ branch: 'ford', model: 'explorer', year: '2020' },
{ branch: 'bmw', model: 'x7', year: '2020' },
],
'branch');
// { 'audi': 2, 'ford': 2, 'bmw': 1 }
~~~
## Check if an array is not empty
~~~ javascript
const isNotEmpty = (arr) => Array.isArray(arr) && Object.keys(arr).length > 0;
// Examples
isNotEmpty([]); // false
isNotEmpty([1, 2, 3]); // true
Objects

Check if multiple objects are equal
~~~ javascript
const isEqual = (...objects) => objects.every((obj) => JSON.stringify(obj) === JSON.stringify(objects[0]));
// Examples
isEqual({ foo: 'bar' }, { foo: 'bar' }); // true
isEqual({ foo: 'bar' }, { bar: 'foo' }); // false

Extract values of a property from an array of objects
const pluck = (objs, property) => objs.map((obj) => obj[property]);
// Example
pluck([
{ name: 'John', age: 20 },
{ name: 'Smith', age: 25 },
{ name: 'Peter', age: 30 },
],
'name');
// ['John', 'Smith', 'Peter']
~~~
## Invert keys and values of an object
~~~ javascript
const invert = (obj) => Object.keys(obj).reduce((res, k) => Object.assign(res, { [obj[k]]: k }), {});
// Or
const invert = (obj) => Object.fromEntries(Object.entries(obj).map(([k, v]) => [v, k]));
// Example
invert({ a: '1', b: '2', c: '3' }); // { 1: 'a', 2: 'b', 3: 'c' }

Remove all null and undefined properties from an object
~~~ javascript
const removeNullUndefined = (obj) => 
Object.entries(obj)
.reduce((a, [k, v]) => (v == null ? a : ((a[k] = v), a)), {});
// Or
const removeNullUndefined = (obj) =>
Object.entries(obj)
.filter(([_, v]) => v != null)
.reduce((acc, [k, v]) => ({ ...acc, [k]: v }), {});
// Or
const removeNullUndefined = (obj) => Object.fromEntries(Object.entries(obj).filter(([_, v]) => v != null));
// Example
removeNullUndefined({
foo: null,
bar: undefined,
fuzz: 42}); 
// { fuzz: 42 }
~~~
## Sort an object by its properties
~~~ javascript
const sort = (obj) =>
Object.keys(obj)
.sort()
.reduce((p, c) => ((p[c] = obj[c]), p), {});
// Example
const colors = {
white: '#ffffff',
black: '#000000',
red: '#ff0000',
green: '#008000',
blue: '#0000ff',
};
sort(colors);
/*
{
black: '#000000',
blue: '#0000ff',
green: '#008000',
red: '#ff0000',
white: '#ffffff',
}
*/
~~~
## Check if an object is a Promise
~~~ javascript
const isPromise = (obj) =>
!!obj && (typeof obj === 'object' || typeof obj === 'function') && typeof obj.then === 'function';
~~~
## Check if an object is an array

~~~ javascript
const isArray = (obj) => Array.isArray(obj);
~~~