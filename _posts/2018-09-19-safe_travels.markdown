---
layout: post
title:      "Safe Travels!"
date:       2018-09-19 13:36:49 +0000
permalink:  safe_travels
---


Using the tool, we’ve acquired so far in the Flatiron web development program, I built a CLI data gem called travel_safe. This gem scrapes the U.S. Department of State’s travel site for the travel advisory information for each country listed. The travel advisory info includes the travel advisory level and additional info including passport requirements, exit and entry currency restrictions and embassy information. For me, the most difficult area by far was the scraping portion. In the beginning, things were flowing nicely and I was on a roll. I used bundle to create the framework, I setup my environment and executable. Using hard-coded data I was able to get the majority of my code to work. However, when it finally came time to start scraping the website for actual data, I was faced with some difficulties.

For starters, there are over 200 countries listed on the site, each country name is a link which redirects to a second page. Each of those secondary pages has its own link that connects to a country specific site which I called the country_url. My challenge was to scrape the initial site for the country name and the link to the next page. Then I need to scrape the redirected page for the country specific link. Finally, I needed to scrape the country_url for the additional travel info and embassy locations. I had to do this process over 200 times in order to include the information for each country and so iteration was my best friend. After determining the correct identifiers to pull the information from the website I used open-uri and Nokogiri to pull and organize the info. I created a Country instance for each country I pulled and assigned the additional information using instance variables. 

About halfway through this process, I started to feel that maybe I bit off more than I could chew. I was able to scrape everything except the country_url. Every iteration I tried was failing and my confidence was faltering. I was receiving error messages that I didn’t understand, what is a 404 error message? Google. How do I fix it? Google. Which link is throwing the 404 message? 

Initially I started going through the countries one by one, click on the country name, click on the country page, yep it works, next. After testing about 10 or so countries like this I realized I wasted a half hour and there had to be a better way, this method was insane. So, I went back to google to come up with a way to use iteration to test the links. Most suggestions described raising error messages for a link that does not work and using next to continue through the iteration. I did just that and built a method called test_links that tested each link and pushed the bad links into an array.  Turns out most of the errors were due to formatting issues, the rest of the errors were typos. I hardcoded corrections for the typo exceptions and created a workaround for the formatting issues. Boom! Country information was flowing. 
In the end I was able to solve all the issues and produce workable code. The realization, that I was able to take a blank window in the learn IDE and turn it into a working CLI gem, was absolutely incredible for me. Though it is small project and I’m sure it could be improved, the accomplishment was exciting and encouraging. Success with this project reassured me that I am on my way to becoming a web developer and I can’t wait to see what’s next. 

**Things I want to learn: **How to publish a ruby gem

Was anyone able to successfully publish their gem? I followed the build and publish instructions on rubygems.org however, I was not able to install the gem I created and run it without an error. I know publishing the gem was not required but after spending 2 hours trying to figure it out, I’d love to know how! lol

