---
layout: post
title:  "When You Wish Upon a Streamlit App: Disney Data continued"
date: 2024-12-04
description: "If you'd like to explore more of the Disney stock and movie data I scraped before, I've got just the app for you. Let's explore how interactive tools like Streamlit allow you to get a better picture for data visualization."
image: "/assets/img/marv_dis.webp"
display_image: false
---
<p class="intro"><span class="dropcap">D</span>ata visualization gets even more memorable when it can be played with. Static images can show you a good overview, but if a picture's worth a thousand words, then a movie should be worth 100 million. Pull up the <a href = 'https://disney-stocks-and-movies.streamlit.app/'>webapp</a> side by side if you'd like to see the value. (And check out the GitHub <a href = 'https://github.com/KimmyBeeW/streamlit-disney-datavis/'>repo</a> for the full code I used.)</p> 


### How to build a Streamlit app
You can attach your github account to streamlit and deploy your app directly from there by signing up for the free [community cloud](https://streamlit.io/cloud) and signing in with your github account. Once you have an account, initialize a new repo for your app, create a main.py file (or whatever you'd like to call it) and a requirements.txt file, and get to writing. You'll need to import the ```streamlit``` library, and probably a few others. My import list on main.py looked like this for this app:

```
import streamlit as st
import numpy as np
import pandas as pd
import plotly.express as px
import matplotlib.pyplot as plt
from io import BytesIO
import plotly.graph_objects as go
from plotly.subplots import make_subplots
```
Any and all libraries that you need for the app need to be included on new lines in your requirements.txt file (like [this](https://github.com/KimmyBeeW/streamlit-disney-datavis/blob/main/requirements.txt)). Once all that is done, you can deploy your app and see what your code affects in real time.

Go to [share.streamlit.io](https://share.streamlit.io/) and click "Create app" in the top right corner. If you're doing it through GitHub like me you'll select the "Deploy a public app from GitHub". Now select the repo that your code is in, select the main or master branch, select the title of your main.py file, and create a custom url for your app. The url I chose for my app is [disney-stocks-and-movies.streamlit.app/](https://disney-stocks-and-movies.streamlit.app/).
<img src="{{site.url}}/{{site.baseurl}}/assets/img/streamlit-createapp.png" alt="" class="center"/>