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

[{
  "image": "[http://cdn0.nflximg.net/images/1442/23711442.jpg",
  "title": "Dude](http://cdn0.nflximg.net/images/1442/23711442.jpg",
  "title": "Dude), Where's My Car?",
  "year": "2000",
  "netflix_url": "[http://www.netflix.com/watch/60004019",
  "average_rating": "3.2",
  "rt-score": ["18%", "47%"],
  "nyt-review-available": "NYT](http://www.netflix.com/watch/60004019",
  "average_rating": "3.2",
  "rt-score": ["18%", "47%"],
  "nyt-review-available": "NYT) Review",
  "maturity_rating_level": "PG-13",
  "quality": "SuperHD",
  "synopsis": "Two hard-partying pizza delivery dudes wake up with no recollection of what happened the previous night -- including where they parked their car.",
  "actors": "Ashton Kutcher, Seann William Scott, Jennifer Garner, Marla Sokoloff",
  "directors": "Danny Leiner",
  "runtime": "83 minutes",
  "available-from": "Nov 16, 2015",
  "queue-count": "557"
}]

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
