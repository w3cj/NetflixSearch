# Netflix search

Uses YQL to parse instantwatcher.com results.

Requires jQuery

# How to use

Include the script in your page:
```html
<script src="netflixSearch.js"></script>
```

```js
Netflix.search("Dude Where's My Car?").done(function(movies){
  console.log(movies);
});
```
