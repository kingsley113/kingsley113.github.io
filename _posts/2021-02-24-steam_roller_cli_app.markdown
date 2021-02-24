---
layout: post
title:      "Steam Roller CLI App"
date:       2021-02-24 06:48:20 +0000
permalink:  steam_roller_cli_app
---

Steam Roller - CLI app to quickly see the top games on Valve's Steam Marketplace

For my first portfolio project, I wanted to incorporate my interest in gaming and game design. I chose to create an app that scrapes the list of the top games from Valve's Steam platform and provides the user a quick look at the list of games without the need for the image heavy webpages. Thus, SteamRoller was born.

The user can select from either the list of top 15 newest releases or top selling 15 games. Once the program scrapes this summary list, it provides basic game info to the user and they can then select a game to see in more detail or sort the list by several attributes. 

The program is based primarily on a “Game” class to store each game instance, A “CLI” Class that performs the primary program operations and provides user interface, and finally a “Scraper” Class to gather the info from Steam’s website. When the user first selects the list they want to see, the scraper class is called and scrapes the selected list. I was able to pull basic game info from this page, including name, price, rank on the list, and a link to the game’s specific webpage. To improve performance, the scraper class does not automatically scrape each game’s page as much of the info will likely not be needed. From here the user can sort by various attributes or select a game. Once a game is selected, the second scraper method is called to then scrape the game’s specific webpage and pulls down detailed info such as release date, rating, developer, tags, genre, etc.

I did enjoy spending some time making the outputs easy to read and dynamically format the lists. I learned how to use left, center, and right justification, and the Colorize gem as well.  One limitation I ran into was dealing with ‘mature’ rated games, as Steam has an age verification page before accessing the game’s page. To handle this limitation, I had the program check and fill in any attribute that could not be scraped with a simple “Not Available” statues for that attribute. The basic name, price, and rank info could be gathered but not the detailed info. 

Overall, I am extremely happy with the program and its performance and reliability.


