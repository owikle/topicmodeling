---
title: Text Analysis
nav: true
---

# Text Analysis

## Discussion:

Why digital text analysis?
- For exploration, hypothesis generation
- To expand the audience for under-recognized texts

Tools you know about/are using to analyze and visualize text?

Franco Moretti (Distant Reading - how to expand worldview of world literature)
- Analyzing 30,000 British novels. Reading 'more' can't be the answer 
- Close reading depends on an extremely small canon
- Distant reading allows you to focus on units that are much smaller or much larger than the text

Ben Schmidt, Ryan Cordell,
Fyfe (2011 How Not to Read) "most promising opportunity of the digital humanities - it makes us ask new questions"

## Word Frequency

What questions do you want to answer by analyzing your text? Whether you have a specific hypothesis in mind or your work is more exploratory, analyzing the frequency of words in your text can be a good place to start. The results may confirm your suspicions or yield surprising outcomes that lead to further research.

**Word Frequency**
- Raw frequency
- Relative frequency
- [Voyant Tools](https://voyant-tools.org/)
- Stopword List

## Word Concordance
- Looking at context

## Other Voyant Tools

Overview of Voyant Interface:

At first you will see three tool panels along the top and two tool panels along the bottom:

- [Cirrus](https://voyant-tools.org/docs/#!/guide/cirrus): a kind of word cloud showing the most frequent terms
- [Reader](https://voyant-tools.org/docs/#!/guide/reader): an efficient corpus reader that fetches segments of text as you scroll
- [Trends](https://voyant-tools.org/docs/#!/guide/trends): a distribution graph showing terms across the corpus (or terms within a document)
- [Summary](https://voyant-tools.org/docs/#!/guide/summary): a tool that provides a simple, textual overview of the current corpus
- [Contexts](https://voyant-tools.org/docs/#!/guide/contexts): a concordance that shows each occurrence of a keyword with a bit of surrounding context

{% capture text %}
Using our Walden text, a text of your choice, or the Austen or Shakespeare corpuses that Voyant provides, explore some of these other Voyant tools:
{% endcapture %}
{% include alert.md text=text color=secondary %}

**Some tips for uploading your texts**

We won't experiment for now with more advanced options for Corpus creation, but there are several [options](https://voyant-tools.org/docs/#!/guide/corpuscreator-section-options) available to tweak the processing of text, XML, and even spreadsheets. 

**Tool Interactions**

An essential part of Voyant is that events in one tool can cause changes in other tools (the exact interactions depend on a number of factors, including which tools are visible). For instance, try the following sequence in the window above:

- click on a word (like "know") in Cirrus, the tool in the upper left
- notice how the Trends tool (upper right) now shows just the word you clicked
- click on one of the discs in the Trends tool
- notice that the Contexts tool (bottom right) has updated with just the clicked word
- click the first row of the Contexts tool (bottom right)
- notice how the Reader tool has jumped to a location where that word appears, highlighted

{% capture text %}
**Reflection Time** 
- What insights, if any, do these tools provide?
- Are there patterns or in/consistencies?
- How might your 'read' groups of words?
- What keywords or patterns did you pursue and why?
- What are the values/limitations of 'not reading' this way?
{% endcapture %}
{% include alert.md text=text color=secondary %}

## Word Tree
- Visualizing context with [WordTree](https://www.jasondavies.com/wordtree/)

