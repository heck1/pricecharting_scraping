# pricecharting_scraping
## Lightweight Scraper for Pricecharting

When collecting video games, you might be interested in tracking your collection over time and see how it changes or you just want to check some prices and compare them to some ebay offers. With this scraper you can easily do this. 

### Basic Usage

``` python


region = "PAL" 
console = "Gamecube"
game= "Pokemon Box"

get_game_price(region, console ,game)

```

returns a pd.DataFrame object:

|        |   loose_price |   complete_price |   sealed_price |   graded_price |   box_price |   manual_price | game        |
|:-------|--------------:|-----------------:|---------------:|---------------:|------------:|---------------:|:------------|
| prices |         48.11 |           104.54 |          292.6 |         885.47 |       19.64 |          27.61 | Pokemon Box |


Works with different systems and regions:

<img width="800" alt="image" src="https://user-images.githubusercontent.com/20683786/230792702-32ee80b7-0bd6-40e5-ac75-15f71ae81b2c.png">


And also works with multiple games ( tested for all 453 PAL Gamecube games):
<img width="901" alt="image" src="https://user-images.githubusercontent.com/20683786/230792898-0c5a5e85-0c87-4c72-9034-c9c7d89cdf71.png">

If you want to be cautious, just add something like
```python
import time

<scrape>
time.sleep(10)

but it seems to work fine with the current setup. 


Since this is for collectors only and pricecharting offers an official api, please dont use this commercially :)

