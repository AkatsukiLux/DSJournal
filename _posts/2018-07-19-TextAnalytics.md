---
layout: post
title: "Text Analytics with Power BI: Analyzing Construction Industry Sentiment"
date: 2018-07-19
categories: [analytics, tutorial]
tags: [power-bi, text-analytics, azure, cognitive-services, nlp]
---

Microsoft has brought text analytics to Power BI and made it so simple!

## Getting Started

Check out this tutorial for connecting up Power BI to text analytics service:
[https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/tutorials/tutorial-power-bi-key-phrases](https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/tutorials/tutorial-power-bi-key-phrases)

## The Challenge

Now the big question is, once you follow this tutorial to get the key phrases and sentiment from your text, how can you use these to generate insights? Surprisingly, cognitive services made the first part of getting data out of the text so straightforward that, the question I posed, I had no idea what I could do with the data. But after a bit of head scratching I came up with a project!

## My Project: Construction Industry Sentiment Analysis

My idea is something that I've toyed about for a while now. I've wanted to be able to get an overall view or opinion on construction related topics based off the Institute of Civil Engineers (ICE) news articles and blogs.

### Project Goals

The aim is to:

1. **Aggregate Content**: Collect articles and blog posts from ICE website
2. **Extract Insights**: Use Azure Text Analytics to identify key phrases and sentiment
3. **Analyze Trends**: Track how sentiment changes over time for specific topics
4. **Visualize Results**: Create Power BI dashboards showing:
   - Topic popularity based on key phrase frequency
   - Sentiment trends for different construction domains (infrastructure, sustainability, safety, etc.)
   - Emerging themes and concerns in the industry

### Implementation Approach

1. **Data Collection**:
   - Use web scraping or RSS feeds to gather ICE articles
   - Store article metadata (date, title, category)
   - Extract article text content

2. **Text Analytics Processing**:
   - Send article text to Azure Cognitive Services Text Analytics API
   - Extract key phrases to identify main topics
   - Calculate sentiment scores (positive, neutral, negative)

3. **Data Modeling**:
   - Link key phrases to articles and dates
   - Create time-series data for trend analysis
   - Categorize topics into construction domains

4. **Visualization**:
   - Build Power BI reports showing sentiment over time
   - Create word clouds of most common key phrases
   - Compare sentiment across different topics
   - Identify correlations between industry events and sentiment shifts

### Expected Benefits

This analysis could help construction professionals:
- Understand industry sentiment on emerging technologies
- Track public perception of construction challenges
- Identify trending topics and concerns
- Make data-driven decisions based on industry discourse

## Next Steps

I'll continue developing this project and share detailed implementation steps, code samples, and visualizations in future posts. Stay tuned for updates on how text analytics can provide valuable insights into the construction industry!

## Resources

- [Azure Cognitive Services Text Analytics](https://azure.microsoft.com/en-us/services/cognitive-services/text-analytics/)
- [Power BI Custom Visuals](https://appsource.microsoft.com/en-us/marketplace/apps?product=power-bi-visuals)
- [ICE News and Blogs](https://www.ice.org.uk/)
