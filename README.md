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
```
```sh
[{
  "image": "http://cdn0.nflximg.net/images/1442/23711442.jpg",
  "title": "Dude, Where's My Car?",
  "year": "2000",
  "netflix_url": "http://www.netflix.com/watch/60004019",
  "average_rating": "3.2",
  "rt-score": ["18%", "47%"],
  "nyt-review-available": "NYT Review",
  "maturity_rating_level": "PG-13",
  "quality": "SuperHD",
  "synopsis": "Two hard-partying pizza delivery dudes wake up with no recollection of what happened the previous night -- including where they parked their car.",
  "actors": "Ashton Kutcher, Seann William Scott, Jennifer Garner, Marla Sokoloff",
  "directors": "Danny Leiner",
  "runtime": "83 minutes",
  "available-from": "Nov 16, 2015",
  "queue-count": "557"
}]
```

```js
// Return the first 23 results for movies sorted by most recently added to netflix
Netflix.search("", 1).done(function(movies){
  console.log(movies);
});
```

```sh
[{
  "image": "http://cdn1.nflximg.net/images/3039/21693039.jpg",
  "title": "Kabhi Alvida Naa Kehna",
  "year": "2006",
  "netflix_url": "http://www.netflix.com/watch/70057651",
  "average_rating": "3.5",
  "rt-score": ["64%", "68%"],
  "nyt-review-available": "NYT Review",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "This romance follows football player Dev Saran and Maya, who are both committed to loveless marriages but long to follow their hearts and be together.",
  "actors": "Shah Rukh Khan, Rani Mukerji, Amitabh Bachchan, Preity Zinta",
  "directors": "Karan Johar",
  "runtime": "191 minutes",
  "available-from": "Nov 20, 2015",
  "queue-count": "39"
}, {
  "image": "http://cdn0.nflximg.net/images/9462/23569462.jpg",
  "title": "Some Kind of Beautiful",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80063709",
  "average_rating": "3.4",
  "rt-score": ["4%", "36%"],
  "maturity_rating_level": "R",
  "quality": "SuperHD",
  "synopsis": "A womanizing poetry professor reevaluates his romantic life when he impregnates a graduate student, then falls in love with her sister.",
  "actors": "Pierce Brosnan, Salma Hayek, Jessica Alba, Malcolm McDowell",
  "directors": "Tom Vaughan",
  "runtime": "99 minutes",
  "available-from": "Nov 20, 2015",
  "queue-count": "354",
  "hot": "hot"
}, {
  "image": "http://cdn0.nflximg.net/images/0914/22260914.jpg",
  "title": "Dark Star: H.R. Giger's World",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80041085",
  "average_rating": "3.2",
  "rt-score": ["63%", "71%"],
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "This documentary examines the unique genius of Swiss artist H.R. Giger, best known for his Oscar-winning designs for \"Alien,\" in his final years.",
  "actors": "H.R. Giger",
  "directors": "Belinda Salin",
  "runtime": "95 minutes",
  "available-from": "Nov 18, 2015",
  "queue-count": "1245",
  "hot": "hot"
}, {
  "image": "http://cdn0.nflximg.net/images/9728/22919728.jpg",
  "title": "Naomi and Ely's No Kiss List",
  "year": "2015",
  "netflix_url": "http://www.netflix.com/watch/80079470",
  "average_rating": "3.4",
  "rt-score": "42%",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "Naomi and her gay best friend, Ely, have been inseparable since childhood, but their bond faces its biggest test yet when they fall for the same guy.",
  "actors": "Victoria Justice, Pierson Fode, Matthew Daddario, Ryan Ward",
  "directors": "Kristin Hanggi",
  "runtime": "90 minutes",
  "available-from": "Nov 18, 2015",
  "queue-count": "131"
}, {
  "image": "http://cdn1.nflximg.net/images/7765/23187765.jpg",
  "title": "People, Places, Things",
  "year": "2015",
  "netflix_url": "http://www.netflix.com/watch/80037761",
  "average_rating": "3.3",
  "rt-score": ["76%", "74%"],
  "maturity_rating_level": "R",
  "quality": "SuperHD",
  "synopsis": "When his wife leaves, a graphic novelist tries to keep his sanity while raising their twin daughters, juggling two jobs and starting life over.",
  "actors": "Jemaine Clement, Regina Hall, Stephanie Allynne, Jessica Williams",
  "directors": "Jim Strouse",
  "runtime": "86 minutes",
  "available-from": "Nov 18, 2015",
  "queue-count": "725",
  "hot": "hot"
}, {
  "image": "http://cdn1.nflximg.net/images/9421/23709421.jpg",
  "title": "Wanted 18  ",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80018864",
  "average_rating": "1.7",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "Stop-motion animation, reenactments and interviews tell the tale of a Palestinian West Bank dairy farm that prospered while defying the Israeli army.",
  "directors": "Amer Shomali, Paul Cowan",
  "runtime": "75 minutes",
  "available-from": "Nov 17, 2015",
  "queue-count": "51"
}, {
  "image": "http://cdn0.nflximg.net/images/1442/23711442.jpg",
  "title": "Dude, Where's My Car?",
  "year": "2000",
  "netflix_url": "http://www.netflix.com/watch/60004019",
  "average_rating": "3.2",
  "rt-score": ["18%", "47%"],
  "nyt-review-available": "NYT Review",
  "maturity_rating_level": "PG-13",
  "quality": "SuperHD",
  "synopsis": "Two hard-partying pizza delivery dudes wake up with no recollection of what happened the previous night -- including where they parked their car.",
  "actors": "Ashton Kutcher, Seann William Scott, Jennifer Garner, Marla Sokoloff",
  "directors": "Danny Leiner",
  "runtime": "83 minutes",
  "available-from": "Nov 16, 2015",
  "queue-count": "557"
}, {
  "image": "http://cdn0.nflximg.net/images/1840/23521840.jpg",
  "title": "Abominable noël",
  "year": "2012",
  "netflix_url": "http://www.netflix.com/watch/70307570",
  "average_rating": "3.3",
  "maturity_rating_level": "TV-Y7",
  "quality": "SuperHD",
  "synopsis": "Two small abominable snowmen flee their mountain to escape a scientist who's trying to capture them and end up spending Christmas with a human family.",
  "actors": "Isabella Acres, Drake Bell, Emilio Estevez, Nolan Gould",
  "directors": "Chad Van De Keere",
  "runtime": "43 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "117"
}, {
  "image": "http://cdn1.nflximg.net/images/4917/23184917.jpg",
  "title": "Comeback Dad",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80057104",
  "average_rating": "2.8",
  "rt-score": "0%",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "Nima's successful, orderly life as an accomplished pianist and music school owner is thrown into turmoil when her long-estranged father reappears.",
  "actors": "Tatyana Ali, Charles S. Dutton, Brad James, Loretta Devine",
  "directors": "Russ Parr",
  "runtime": "88 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "24"
}, {
  "image": "http://cdn1.nflximg.net/images/6461/22586461.jpg",
  "title": "Cong Cong Na Nian",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80029123",
  "average_rating": "2.1",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "A wedding guest nostalgically looks back on more than 15 years of memories with his best friends and draws inspiration from recalling a lost love.",
  "actors": "Eddie Peng, Ni Ni, Kai Zheng, Wei Chen",
  "directors": "Yibai Zhang",
  "runtime": "119 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "13"
}, {
  "image": "http://cdn1.nflximg.net/images/4559/23184559.jpg",
  "title": "Dawn Patrol",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80048937",
  "average_rating": "3.0",
  "rt-score": ["0%", "14%"],
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "After he exacts revenge on the man he believes murdered his brother, a small-town California surfer must face the consequences of his actions.",
  "actors": "Scott Eastwood, Rita Wilson, Jeff Fahey, David James Elliott",
  "directors": "Daniel Petrie Jr.",
  "runtime": "87 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "227"
}, {
  "image": "http://cdn1.nflximg.net/images/0027/23090027.jpg",
  "title": "The Dempsey Sisters",
  "year": "2013",
  "netflix_url": "http://www.netflix.com/watch/80057701",
  "average_rating": "3.2",
  "rt-score": "0%",
  "maturity_rating_level": "TV-PG",
  "quality": "SuperHD",
  "synopsis": "Three sisters at a turning point in their lives decide to get back to their musical roots and put their family band back together.",
  "actors": "Denyce Lawton, Cymphonique Miller, Teairra Mari, Lynn Whitfield",
  "directors": "Roger Melvin",
  "runtime": "88 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "24"
}, {
  "image": "http://cdn0.nflximg.net/images/1262/22261262.jpg",
  "title": "Felt",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80019073",
  "average_rating": "2.0",
  "rt-score": ["58%", "42%"],
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "To cope with the sexual abuse she suffered, a woman creates a series of volatile alter egos that begin to create new problems for her.",
  "actors": "Amy Everson, Alanna Reynolds, Kentucker Audley, Roxanne Lauren Knouse",
  "directors": "Jason Banker",
  "runtime": "80 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "214"
}, {
  "image": "http://cdn0.nflximg.net/images/5200/22615200.jpg",
  "title": "Huang jin shi dai",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80016412",
  "average_rating": "1.8",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "The story of writer Xiao Hong comes alive through memories of her great love affair, literary influence and escape from China during World War II.",
  "actors": "Wei Tang, Shaofeng Feng, Zhiwen Wang, Yawen Zhu",
  "directors": "Ann Hui",
  "runtime": "178 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "23"
}, {
  "image": "http://cdn0.nflximg.net/images/5194/1295194.jpg",
  "title": "I'm Still Here",
  "year": "2010",
  "netflix_url": "http://www.netflix.com/watch/70143240",
  "average_rating": "2.7",
  "rt-score": ["53%", "38%"],
  "maturity_rating_level": "R",
  "quality": "SuperHD",
  "synopsis": "In 2008, Oscar nominee Joaquin Phoenix walked away from acting to pursue a rap career, a bizarre detour captured in detail in this \"documentary.\"",
  "actors": "Joaquin Phoenix",
  "directors": "Casey Affleck",
  "runtime": "107 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "280"
}, {
  "image": "http://cdn0.nflximg.net/images/2170/23182170.jpg",
  "title": "The Love Letter",
  "year": "2013",
  "netflix_url": "http://www.netflix.com/watch/80057116",
  "average_rating": "3.4",
  "maturity_rating_level": "TV-PG",
  "quality": "SuperHD",
  "synopsis": "When her best friend gets engaged to a woman he doesn't love, an advice columnist turns to her readers for help and makes a surprising discovery.",
  "actors": "Keshia Knight Pulliam, Romeo Miller, Jackée Harry, Marques Houston",
  "directors": "Gary Wheeler",
  "runtime": "86 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "47"
}, {
  "image": "http://cdn1.nflximg.net/images/2477/21322477.jpg",
  "title": "Mandie and the Forgotten Christmas",
  "year": "2011",
  "netflix_url": "http://www.netflix.com/watch/80049715",
  "average_rating": "3.2",
  "rt-score": "43%",
  "maturity_rating_level": "G",
  "quality": "SuperHD",
  "synopsis": "A forbidden attic harboring a hush-hush holiday mystery. For this spirited girl, Christmas may never be the same.",
  "actors": "Kelly Washington, Amanda Waters, Joanna Daniel, Glennellen Anderson",
  "directors": "Joy Chapman",
  "runtime": "90 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "53"
}, {
  "image": "http://cdn0.nflximg.net/images/2742/23382742.jpg",
  "title": "Marry Me for Christmas",
  "year": "2013",
  "netflix_url": "http://www.netflix.com/watch/80074151",
  "average_rating": "3.7",
  "maturity_rating_level": "TV-PG",
  "quality": "SuperHD",
  "synopsis": "A New York career woman who's tired of her family pressuring her to get married convinces a handsome employee to pose as her fiancé for the holidays.",
  "actors": "Malinda Williams, Brad James, Tamara LaSeon Bass, Jason Weaver",
  "directors": "Roger Melvin",
  "runtime": "86 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "57"
}, {
  "image": "http://cdn0.nflximg.net/images/2212/23182212.jpg",
  "title": "My Dad's a Soccer Mom",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80049727",
  "average_rating": "3.9",
  "rt-score": "50%",
  "maturity_rating_level": "TV-PG",
  "quality": "SuperHD",
  "synopsis": "A former football player becomes a stay-at-home dad to his 10-year-old daughter, and discovers that she has a previously untapped talent for soccer.",
  "actors": "Wendy Raquel Robinson, Lester Speight, Skai Jackson, Tracey Gold",
  "directors": "Randall Stevens",
  "runtime": "82 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "54"
}, {
  "image": "http://cdn1.nflximg.net/images/0505/23150505.jpg",
  "title": "Naked Among Wolves",
  "year": "2015",
  "netflix_url": "http://www.netflix.com/watch/80080205",
  "average_rating": "3.7",
  "rt-score": "89%",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "When an orphan boy is smuggled into a concentration camp, he is protected by the prisoners, but the camp's Nazi guards soon learn of his presence.",
  "actors": "Florian Stetter, Peter Schneider, Sylvester Groth, Sabin Tambrea",
  "directors": "Philipp Kadelbach",
  "runtime": "101 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "227"
}, {
  "image": "http://cdn0.nflximg.net/images/0962/23180962.jpg",
  "title": "Qin ai de",
  "year": "2014",
  "netflix_url": "http://www.netflix.com/watch/80016406",
  "average_rating": "2.3",
  "rt-score": "0%",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "When a 3-year-old boy vanishes from a playground, his parents begin a long and desperate search that leads them into unexpected territory.",
  "actors": "Wei Zhao, Bo Huang, Dawei Tong, Lei Hao",
  "directors": "Peter Chan",
  "runtime": "128 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "27"
}, {
  "image": "http://cdn0.nflximg.net/images/1234/22601234.jpg",
  "title": "Shi Gu",
  "year": "2015",
  "netflix_url": "http://www.netflix.com/watch/80044684",
  "average_rating": "2.0",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "A father whose toddler son was kidnapped forms a special bond with a young survivor of abduction as they search together for the loved ones they lost.",
  "actors": "Andy Lau, Boran Jing, Sandra Ng Kwan Yue, Tony Leung Ka Fai",
  "directors": "Peng Sanyuan",
  "runtime": "108 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "16"
}, {
  "image": "http://cdn0.nflximg.net/images/1932/23601932.jpg",
  "title": "Soaked in Bleach",
  "year": "2015",
  "netflix_url": "http://www.netflix.com/watch/80057508",
  "average_rating": "4.1",
  "rt-score": ["30%", "78%"],
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "An investigator Courtney Love hired to find Kurt Cobain a few days before his death shares a side of the tragedy not revealed in official reports.",
  "directors": "Benjamin Statler",
  "runtime": "89 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "807",
  "hot": "hot"
}, {
  "image": "http://cdn1.nflximg.net/images/7987/23537987.jpg",
  "title": "Tengo Ganas De Ti",
  "year": "2012",
  "netflix_url": "http://www.netflix.com/watch/70267459",
  "average_rating": "4.2",
  "maturity_rating_level": "NR",
  "quality": "SuperHD",
  "synopsis": "In this sequel to Tres Metros Sobre el Cielo, Hache slowly begins to get over his ex-girlfriend Babi when he meets the vivacious Gin.",
  "actors": "Mario Casas, Clara Lago, María Valverde, Marina Salas",
  "directors": "Fernando González Molina",
  "runtime": "118 minutes",
  "available-from": "Nov 15, 2015",
  "queue-count": "29"
}]
```

```js
// Return the next 23 results for movies sorted by most recently added to netflix
Netflix.search("", 2).done(function(movies){
  console.log(movies);
});

// Return the next 23 results for movies sorted by most recently added to netflix
Netflix.search("", 3).done(function(movies){
  console.log(movies);
});
```
