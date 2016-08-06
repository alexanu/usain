# USAIN

Welcome! This program will generate dummy stock ticks at user-specified speeds.

![alt text](http://www.miklas.org/images/usain_verbose.png "usain tick generator image")


# Introduction

As a Financial Engineer, Computer Scientist, and Quantitative Analyist, I found myself in a dilemma.

I wanted to write algorithms to analyze stock data with statistical, cryptographic, pattern recognition, and other methods. Little did I realize the nasty surprise that awaited me. As it turns out, this usage of market data is highly restricted, and VERY expensive--it can easily cost tens of thousands of USD per month. These are called "non-display fees." In other words, if you simply pipe a data feed into a terminal, the fee is minimal; around $6. If you use an API, fees are thousands of dollars per exchange. [1][2][3]

What to do? I had to remain in compliance with regulations; however, a data feed was out of my price range. At the same time, I still wanted to develop quantitative algorithms for real-time analysis of tick data.

The only answer was to write a program to generate my own data. There, I faced no restrictions, and could write analytic algorithms to my heart's content.

In addition to avoiding exchange fees and regulations, the speeds that Usain produces are far beyond that of most professional data feeds. On an Intel I7-4790K LGA1150 Core Duo processor, ASUS Z-97 Pro Mobo, I can get tick speeds of about 1.5 nanoseconds. This beats pretty much anything--even those colocated at the exchanges--With the exception of those able to run their scripts directly on exchange hardware. This provides the ability to develop low-latency algorithms without stepping on any toes.

Thus, was born Usain; and here it is for you to enjoy. John 3:16.

# Usage

The script is quite simple to use.
- For usage, just type "usain" or "./usain" if you do not have your path set.

Having struggled for decades to make things work with little or no documentation, I really try to make things as easy as possible.

Here is usage copy, which includes some helpful examples:

![alt text](http://www.miklas.org/images/usain_usage.png "usain tick generator image")

# Todo

This is the first commit, and it works, but there's a lot more that I want to do with this program. I'm hoping that some of you C++ gurus out there might help:

1. Implement the client-server model. Usain is the server; a client is needed to receive and process the data. This would require creating an interface between the client and server. I plan to model this afer industry-standard interfaces. I'm about 50% done with this script as of 05 Aug 2016. 
2. Build a standard interface so that industry-standard terminals can connect to this feed (Ninjatrader&reg; Sierra Charts&reg;, even Bloomberg Terminal&reg;)
3. Rework the tick generation algorithm--I had to hack something together. Perhaps give the user the option to generate according to a mathematical model of their choice.<br>
Side note: Initially, I innocently wrote a random number generator to produce Brownian motion, using the rand() function. This did not work! After a few seconds and a trillion ticks, USAIN flew off the handle, and quickly either spiked up to an incredible value, or went either spectacularly out of business at a price of about +/-$4000.00. I leave it to the reader to decide what this says about the theories of Browninan motion.
4. Include a command-line parser, so that options can be specfied. Example: usain --tickspeed 10 --verbose --model stochastic. 

# Usain Bolt

Usain Bolt is, at this time, the fastest human in the world.

He set the 100m dash world record on 8/16/2009 with a time of 9.58 seconds.

![alt text](http://www.miklas.org/images/usain_gold.jpg "usain tick generator image")

# References





  




