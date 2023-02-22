# intl.Listformat 

The *Intl.ListFormat* object enables language-sensitive list formatting.


Passing in a locale and then some options. If locale is undefined it will revert to whatever default there is.

```javascript
const array = ['The Hulk', 'Captain America', 'Wonder Woman'];

const f = new Intl.ListFormat('en-UK', { 
  style: 'long', 
  type: 'conjunction' 
});
```

```
console.log(f.format(array));

> "The Hulk, Captain America and Wonder Woman"
```

```javascript
f = new Intl.ListFormat('es', { 
  style: 'short', 
  type: 'disjunction' 
});
````

```
console.log(f.format(array));

> "The Hulk, Captain America o Wonder Woman"
```

```
f = new Intl.ListFormat('en', { 
  style: 'narrow', 
  type: 'unit' 
});
```

```
console.log(f.format(array));

> "The Hulk Captain America Wonder Woman"
```