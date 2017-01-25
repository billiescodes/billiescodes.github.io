---
layout: post
title: Project Benson, or how I learned to stop worrying and love messy data
---

Here’s a few things I learned in my first week at Metis.
There’s no better way to learn Data Science than to jump into the deep end straight away. 
The kinds of things you will be able to draw insights from will never cease to amaze you. 
Perfectionism with data will blow up (mild attempt at Kubrick reference #1) in your face really fast. No, really. If pressed for time better drop it like hot potatoes.  Real life data is messy.


The Metropolitan Transit Authority in New York is in charge of the bus subway systems. They provide an awesome data set of turnstiles at each station, where they count entries and exits for each day.  So we set out to play with some entries 
The scenario we chose for our group is a consulting group to a marketing company that guarantees maximum exposure of billboards in the subway of NYC. 
The goal is to find the most traffic in the most visited subways and the exact days and weeks of of peak traffic. Easy enough, right?

We looked at the Entries column of our data to get an idea. The turnstiles have a clicker counter that corresponds to one count for every person who passes through. 
Every four hours, these clicks are recorded. Additionally the clicker is reset to to zero at some number. To find the daily count, you 
subtract the clicker record from the previous day. And here is where we found our first hurdle: each Turnstile resets at a different time,
as a result, some results showed Daily entries in the millions. If that doesn’t seem right, it’s because it isn’t. Oops. 

Sadly, this project had a time constraint, and we couldn’t exactly employ a ‘no man left behind ‘ policy. 
Daily entries with unreasonable counts were dropped, but it did allow us to get reasonable counts for traffic entered for each station. 
Looking over a couple of months, here are the Daily Entries for all turnstiles at Times square. 
![an image]({{ site.baseurl }}/images/turnstile_Times-Square.png)

As a Consulting company to marketers, we were also interested in the most popular stations for each month. 
We found the most popular stations in December and the by-Weekday traffic for those stations.
![an image]({{ site.baseurl }}/images/december_popular.png "Most popular in December")
![an image]({{ site.baseurl }}/images/weekly_avg.png "Weekly")

Just for fun, here's a map of NYC and the location of these most popular stations. Apparently New Yorkers like to hang out in Midtown.
![an image]({{ site.baseurl }}/images/NYC_Map.png "NYC Map of most popupular stations")

Other hurdles we found were related to dates and times. It was difficult to do calculations over the New Year, so we ended up
sticking with data from 2016. Also some turnstiles started their daily count at different times, which we had to account for.
Overall the data was fun to mess with and I learned a valuable lesson: leave perfectionism at the door!


