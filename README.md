# Donald-Trump-Twitter-Tweets-Sentiment-Analysis


I don’t usually post about politics (I’m not particularly savvy about polling, which is where data science has had the most substantial impact on politics), but I saw a hypothesis about Donald Trump’s Twitter account that simply begged to be investigated with data:

@tvaziri's hypothesis about Donald Trump’s Twitter account

When Trump wishes the Olympic team good luck, he’s tweeting from his iPhone. When he’s insulting a rival, he’s usually tweeting from an Android. Is this an artifact showing which tweets are Trump’s own and which are by some handler in the campaign?

Others have explored Trump’s timeline and noticed this tends to hold up. And Trump himself did indeed tweet from a Samsung Galaxy until March 2017. But how could we examine it quantitatively? During the development of the tidytext R package, I was writing about writing about text mining and sentiment analysis, and this is an excellent opportunity to apply it again.

My analysis, shown below, concludes that the Android and iPhone tweets are clearly from different people. Tweets from these two devices are posted during different times of day, and the use of hashtags, links, and retweets are distinctive. What’s more, we can see that the Android tweets are angrier and more negative, while the iPhone tweets tend to be benign announcements and pictures. Overall I’d agree with @tvaziri’s analysis. We can tell the difference between the campaign’s tweets (iPhone) and Trump’s own (Android). Let's see how.

First, let's load the content of Donald Trump’s timeline. Our dataset is from The Trump Twitter Archive by Brendan Brown, which contains all 35,000+ tweets from the @realDonaldTrump Twitter account from 2009 (the year Trump sent his first tweet) through 2018. We'll filter it for the election period only, June 1st, 2015 through November 8th, 2016.

## Below are some of the Visualizations from my Analysis

# A. Is TIME the giveaway?
<img width="725" alt="Screen Shot 2023-01-01 at 11 08 58 AM" src="https://user-images.githubusercontent.com/111389636/210179186-6196d898-b6e1-4a73-a349-d9318a0cfcec.png">


# B. Whether the tweet starts with a quotation mark
<img width="722" alt="Screen Shot 2023-01-01 at 11 08 35 AM" src="https://user-images.githubusercontent.com/111389636/210179179-e90532a4-54be-4def-9de3-0fe785b16ac0.png">


# C. The number of tweets with and without picture/links by device
<img width="709" alt="Screen Shot 2023-01-01 at 11 08 01 AM" src="https://user-images.githubusercontent.com/111389636/210179173-8445b1c0-1926-4b6e-9bb1-0985724c4c1e.png">


# D. The most common words from @realDonaldTrump tweets
<img width="722" alt="Screen Shot 2023-01-01 at 11 07 33 AM" src="https://user-images.githubusercontent.com/111389636/210179170-6a809e6e-b708-4ddb-a53c-8c1b93ffa130.png">

