# Netflix search

Uses YQL to parse instantwatcher.com results.

Requires jQuery

# How to use

Include the script in your page:
```html
<script src="netflixSearch.js"></script>
```

```js
// Netflix search accepts 2 parameters:
// query and page number (page number is optional)

// Search for a specific title
Netflix.search("Dude Where's My Car?").done(function(movies){
  console.log(movies);
});

// Return the first 23 results for movies sorted by most recently added to netflix
Netflix.search("", 1).done(function(movies){
  console.log(movies);
});

// Return the next 23 results for movies sorted by most recently added to netflix
Netflix.search("", 2).done(function(movies){
  console.log(movies);
});

// Return the next 23 results for movies sorted by most recently added to netflix
Netflix.search("", 3).done(function(movies){
  console.log(movies);
});
```
