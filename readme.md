This repository contains the r markdown used to analyze the Georgia Senate Special (November 3, 2020) race.

If you're looking for pretty r code, this is not it. I piece-mealed this while writing *The GOP's Giant Kelly Loeffler Problem.* Since I wrote this code and the article over a period of several days, I was more inclined to copy and paste with regex replacements than to write a function. I'd think "how did Republicans perform in X county," answer that with a little copy and paste, and keep writing.

If I actually followed best practices for this one, I would have stopped before the third copy and paste and written the function. I didn't.

If you wish to download this code and run it, add your directory to 

```
knitr::opts_knit$set(root.dir = "")
```

## Data Sources

All data used in this analysis is included as csv files.

* Historic Georgia US Senator Birth Place
  * [List of US Georgia Senators](https://en.wikipedia.org/wiki/List_of_United_States_senators_from_Georgia)
  * [Biographical Directory of the United States Congress](https://bioguideretro.congress.gov/)
  * Please note that under the Appointed column, 1 means a senator was appointed but not elected. For example, Loeffler was appointed. She made the runoff, so she's still running for election. She has not yet been elected. Therefore, she is a 1.
* Election Data
  * [Georgia's Official Election Results as Certified by the Secretary of State](https://results.enr.clarityelections.com/GA/105369/web.264614/#/summary)
  * I combined the candidate name row and the ballot type row. Then deleted all header rows except the new one. That was the only change.
* Candidate Names and Parties
  * I used a photo of my absentee ballot, which I sent to a friend as proof the senate special was "as long as my arm." Since I'd already filled out the ballot, I'm not posting the photo.