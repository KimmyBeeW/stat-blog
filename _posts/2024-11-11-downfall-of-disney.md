---
layout: post
title:  "The Downfall of Disney? Once upon a Web Scraper"
date: 2024-11-11
description: "Disney movies haven't been the same for a few years, and I've been missing the magic. Just me? Disagree? The data is all there, let's web scrape and find out."
image: "/assets/img/data-vis3.0.png"
display_image: false
---
<p class="intro"><span class="dropcap">O</span>kay, downfall may be a little dramatic, but if Disney continues at the rate it's going, I may not be far off. I used to be obsessed with the MCU. I loved watching all the theory videos on YouTube and was so excited every time a new movie was announced, but when, epic though it was, Endgame managed to kill off or fatally change many of my favorite characters, I knew the MCU would never be the same. Around the same time in 2019 and 2020 Disney's live-action remakes churned out some interesting choices with a not-at-all-live-action "live action" Lion King including ["Can You Feel the Love Tonight"](https://youtu.be/DZr-VTULYQ8?si=H3eaDo2D2kChAh_x) being sung in the middle of the day and the titular character of Mulan's fighting spirit being replaced with [magical](https://www.imdb.com/title/tt4566758/reviews/) [chi](https://www.reddit.com/r/TwoBestFriendsPlay/comments/ily73g/you_dont_just_have_power_you_have_chi_power_or/?rdt=65373) [superpowers](https://www.polygon.com/entertainment/2020/9/3/21419876/mulan-review-live-action-disney-plus), in other words completely missing the points of some of the old stories. The animations are still beautiful and the stories are still enjoyable, but I started sensing a pattern when looking back on those memories, and it got me wondering if those changes, and the apparent emphasis on quantity over quality, was starting to hurt Disney as a business. So I took my newfound web-scraping skills to the [Box Office Mojo](https://www.boxofficemojo.com/) website to see what the movie theater goers votes had to say.</p>

### How has Disney been doing as a company over the last few years?
Since Disney does more than just movies, I figured we should take a look first on how the shareholders view Disney's success in terms of what they're willing to pay for it in stocks. I got this stock data from [Yahoo! Finance](https://finance.yahoo.com/quote/DIS/history/?period1=1571423893&period2=1729276688), and you can see that other than the obvious dip caused by the pandemic in March of 2020, Disney was on the rise until around February 2021, then fell again November of 2021, and hasn't gone above $130 since the beginning of 2022.
<img src="{{site.url}}/{{site.baseurl}}/assets/img/disstocks5yrs.png" alt="" class="center"/>

Because of the rise of inflation and the noteriaty of the company, Disney is still doing better than pre-2014. Loyal fans are still clinging on to the nostalgia of the past and the merch of the present, and there is no doubt that Disney is still a successful company, it is just an interesting thing to note before diving into the success of current movies.
<img src="{{site.url}}/{{site.baseurl}}/assets/img/disstocks_allyrs.png" alt="" class="center"/>

### A tale as old as Box Office numbers
Now that we have an overview of what the shareholders think, let's look at what actual movie-goers think by how they voted with their ticket purchases. [Box Office Mojo](https://www.boxofficemojo.com/brand/?ref_=bo_nb_gs_secondarytab) has a really awesome collection of brands, their respective movies, and info about those movies' lifetime gross income to date, max number of theaters, opening weekend gross income, opening number of theaters, release date, and distributer. It's fun to look through their website, but I really wanted an aggregate of brands owned by disney, so I used web-scraping to look at the following brands from the [Box Office Mojo Website](https://www.boxofficemojo.com/brand/?ref_=bo_nb_gs_secondarytab):
+ [Marvel Comics](https://www.boxofficemojo.com/brand/bn3732077058/) – Disney acquired Marvel Entertainment in 2009.
+ [Lucasfilm](https://www.boxofficemojo.com/brand/bn4168284674/) – Disney purchased Lucasfilm in 2012.
+ [Pixar](https://www.boxofficemojo.com/brand/bn3530750466/) – Acquired by Disney in 2006.
+ [Walt Disney Animation Studios](https://www.boxofficemojo.com/brand/bn3295869442/)
+ [Blue Sky Studios](https://www.boxofficemojo.com/brand/bn3430087170/) – Disney acquired Blue Sky as part of the 2019 purchase of 21st Century Fox, but it was shut down in 2021.
+ [Disney Channel](https://www.boxofficemojo.com/brand/bn3446864386/)
+ [DisneyToon Studios](https://www.boxofficemojo.com/brand/bn4185061890/) – A division of Disney, closed in 2018.
+ [Disneynature](https://www.boxofficemojo.com/brand/bn3245537794/)


### Want to do it yourself?
Check out my [repo](https://github.com/KimmyBeeW/Disney-Web-Scraping) with all of the code I used to webscrape the Box Offic Mojo website, my RequestGuard file for parsing the robots.txt files, the data I gathered, and some helpful links I found. Web scraping is a lot easier than I remembered it being, it just takes some puzzling and time. Go analyze data about your own interests, and always remember to have fun coding in color!