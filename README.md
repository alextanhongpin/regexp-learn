# regexp-learn
Useful regex


## Find character repeating 10 or more times

`\1` points back to the initial match.
```
/(.)\1{9,}/
```

## Find word repeating 10 or more times

```
/([\w.]+)\1{9,}/
```

## Replace multiple white space with single space

```js
text.replace(/ {2, }/, ‘ ’)
```


## Check if a unicode starts with capital

The `\p{...}` is the unicode properties. The unicode flag `u` must be enabled. See full list [here](https://javascript.info/regexp-unicode).

```js
/^\p{Lu}/gum.test("Hello") // true
/^\p{Lu}/gum.test("hello") // false
```

If we just need to test 'A-Z', this regex below will work just fine:

```js
/^[A-Z]/.test("Hello")
```
