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
