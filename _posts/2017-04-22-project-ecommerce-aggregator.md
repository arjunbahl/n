---
id: AZ7bEHQXlXEKfR9s3JPsc
title: 'Project: Ecommerce Aggregator'
desc: ''
updated: 1636922485777
created: 1636922485777
date: '2017-04-22'
categories:
  - research
---

![](https://aakashkathuria.files.wordpress.com/2017/04/nk.png?w=300)

While checking out a product on Amazon UK i found this graph and at first i was wrecked! I had a similar product(MVP) and now Amazon already bought such functionality from someone that makes my hardwork for last 3 months futile.

On further looking for it, i found that its a firefox addon i had installed that tampers with all html before viewing and appends any such comparsion graphs. Phewww! Ass saved!

Now that my product is almost ready, few things are imminent:

1. Collection of data- Crawling
2. Less clicks more interaction- UX Fix
3. Create a vision for its future- Product Philosophy
4. Decide Name- (this one's particularly hard, indecisive on this.)

I think Raspberry Pi would be able to handle initial traffic, but theres more to it. Hardik and i have started this blog: foundersflesh.com and it's being hosted on the same Pi therefore traffic congestion could be seen.

Configuring Pi is a hell lot of pain in the ass.

**26.04.2017**

Finally kicked off the project.

![](images/screenshot_2017-04-26-00-56-311.png)

![](images/wp-1493148311100.jpg)

Looks pretty good. Data collection is fast. I'm currently clocking it, predicting it yo take 8hrs. Mainly due to slow writing speed into DB. Heating level is fine. Although i turn on fan everytime. RPi is good for light scraping. I have threaded 4x for utilising pi's full potential. I think i can add more threads. Using Pool.

Further requirements:

1. Forwarding page
2. Instagram coverage
3. Twitter Bot (selerity) announcing deals
4. Further scraping on portals(Croma, snapdeal,etc), use Klipsee app API.
5. Future vision: Aggregator or intelligence assistant

01/05/17

1. Indexed around 70000 products.
2. Need to work on GUI
3. Fear of failure is gradually transcending towards hope.
4. Still no idea about promotion?
5. Should i contact for funds? Or wait until i get good customer base? But that will take time. What if i worn out in between? If i could generatr revenue from service itself in the very beginning and bootstrap it i can make it work. But still promotion is needed.

13 May 2017

1. We crossed 90000+ products on our database.
2. Slight change in model, instead of aggregator plain and simple we can launch it as a recommender service, like Spotify, collaborative recommendations.
3. Also maybe we could sell this service to messenger platforms like Hike for in app product discovery and browsing.

22 June 2017

1. Crossed 100000 products today. Exactly 115494 products right now.
2. Shifted filesystem to USB from sd card.

26 June 2017

1. Learn preferences as well like what should go with what, as in shorts lowers with sports t-shirts. Like decision trees 2 ways to get input, search by typing or though share buttons Import tool fir website wishlist or bookmarks.
    
    More filters like popular, trendy, etc
    
    Use clients to update particular product data by fetching it through their phone and using our DB.
    
    Initial interface like in Spotify to learn preferences.
    
    Use Spotify's playlist builder like function to automatically build lists without user's requirement to search specifically. User interface shall be duel, fir instance in a grid every item shall have cube effect to show complementary items white every item on grid would be item searched.

2 Sept 2017

1. This project can work as an Aggregator, think of unorganized online sector like facebook pages instagram pages etc that can be under radar.

5-12-2017

1. [Workflow](https://workflow.is/) stitches together tasks from multiple apps into one. Users can post an image to Facebook, get directions, order food, and do other things without leaving the app.
    
    Workflow became the most purchased iPhone app for four days after it launched in 2014. In 2015, Apple awarded Weinstein and Kramer an award for the [most innovative app of the year](http://www.usatoday.com/story/tech/2015/12/09/most-innovative-app-year---workflow/77021308/).
