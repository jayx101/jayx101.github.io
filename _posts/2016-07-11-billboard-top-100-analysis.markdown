---
title: "Billboard Top 100 Analysis"
layout: post
date: 2016-07-11 11:01
image: '/assets/images/'
description:
tag:
blog: true
jemoji:
author:
---

# Analysis of Billboard Hits 

## Preface

###  Poject Summary
On next week's episode of the 'Are You Entertained?' podcast, we're going to be analyzing the latest generation's guilty pleasure- the music of the '00s. Our Data Scientists have poured through Billboard chart data to analyze what made a hit soar to the top of the charts, and how long they stayed there. Tune in next week for an awesome exploration of music and data as we continue to address an omnipresent question in the industry- why do we like what we like?



### Problem Statement

What are the characteristics of songs that got them to the top of the charts and kept them in the charts longer than others

1. Are any of the categorical data fields represented in the population more significantly represented than others
2. Are there any factors that made some tracks fall out or the chart faster than others
3. Are there any relationships on the dates that the tracks were on the charts

### Risks and Assumptions


1. When there is no data for a track for a week, the track was no represented for valid reasons and not due to bad quality data. When a tracks rating was near 100 it made logical sense that the track could go off the chart. For other tracks like 'Higher' and 'Amazed', they fell of the charts at 61 and 50 respectively. The data is correct as was verified on the Billboard website.

2. It is not possible to speculate what gets a track onto the chart without being able to look at data on the full population of tracks that sold but had not made it onto the charts.

3. The assumption is that the tracks provided where in order of best rated track from top to bottom.  Its is not clear whether the data set is for US only, Europe or world wide. Look at the data the tracks at the bottom perform worse incrementally which supports this assumption.

## Findings
### Genres

<img src="genres.png"></img>

One of the most significant findings were that Rock makes up 42.22% of all genres, Country at 23.23% and Rap 18.3%. Combined these three categories make up 83.75% of all tracks on the charts.

The y axis represents the count of ratings, and the x the genres

### Track Time

<img src="secdist.png"></secdist>

Track times across the total population are normally distributed with a positive skew. Within two standard deviations which accounts for 95%, tracks are between 5:18 and 2:42 minutes long.

### Time of year on the charts

<img src="eoy.png"></src>

Here I was looking for significance that when tracks were on the charts at some time of the year, they would performed better. 

Since Black Friday and Christmas / New Years fall toward the end of the year, the months from Aug until and including January make up the end of year series (green bar). The rest make up the other 6 months of the year.

The top and bottom graphs represent the best performing and worst performing tracks. This was to see if there was any relation in the peak an non peak months against the better or worse performing months

The findings were that tracks in that peaked during the end of the year have a 4.2% change of performing better than the tracks at the beginning.

2.5% Top performing track difference
7.69% Bottom performing track difference

### Timeline 

<img src="timeline.png"></img>

x axis is week from date added.
y axis is the count of tracks.

green series shows whether a track made it to  the top 10.

The graphs plots as would be expected that the longer the weeks went on, the more tracks would fall off the chart. 
At week 20, there is a drastic reduction. 

Upon closer investigation, it is clear that if track gets to the 20 week mark and 
    a. has not gotten better in ranking  
    b. is above a ranking of 50
    c. did not have a ranking before 20 and then had a subsequent ranking lower than 50
They would be removed from the charts.

A sample of the data showing this can be seen below. Column AA is week 20.

<img src="dropoff.png"></src>

## Conclusion

To improve probability of getting onto and keeping a track on the billboard, entering a Rock, Country or Rap song would have the most impact.

5:18 and 2:42 which would be representative of 95% of the tracks on the billboard would be the ideal track length.

Releasing a track to make the charts between August to the following year January has only a 4.2 percent change of being better than from February till July which does not seem significant.

When a track does make it onto the charts, aim to promote it more just before the 20 week mark to ensure that the track stays on the Billboard which could potentially drive sales from being listed.



```python

```
