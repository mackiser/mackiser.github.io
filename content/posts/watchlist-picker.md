---
title: "Letterboxd Watchlist Picker"
date: 2022-12-15
draft: false
tags: ["python"]
---

{{< alert "triangle-exclamation" >}}
This script was made for educational purposes only. Web-scraping is against the Letterboxd TOS.
{{< /alert >}}

### Goal
Write a Python script that chooses a random movie from a user's [Letterboxd](https://letterboxd.com) watchlist.

### Getting Started
Start by importing the necessary Python libraries for scraping a webpage and then choosing a random selection from an array.

```python
import requests
from bs4 import BeautifulSoup
import random
```

### Configuring BeaufifulSoup
Next we will define our variables and tell the BeautifulSoup library how to find the film title when scraping the web page.

```python
# Set the URL of the user's Letterboxd watchlist
url = "https://letterboxd.com/mackiser/watchlist/"

# Make a GET request to the URL
response = requests.get(url)

# Parse the HTML content of the page
soup = BeautifulSoup(response.content, "html.parser")

# Find all the movie elements on the page
movies = soup.find_all("div", class_="film-poster")
```

### Selecting a Random Film
Now we will use the **random** library to choose a random film from the array of movies we have now.

```python
# Pick a random movie from the list
random_movie = random.choice(movies)
```

### Print the Selection

```python
print(title)
```

### Output
```r
Mac@Mac-Desktop MINGW64 /e/Github/pythonWithMosh/content (main)
$ python3 watchlistPicker.py
Citizen Kane
```