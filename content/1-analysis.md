---
title: Text Analysis
nav: true
---

# Text Analysis

## The Why:

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

What questions do you want to answer by analyzing your text? Whether you have a specific hypothesis in mind or your work is more exploratory, analyzing the frequency of words in your text can be a good place to start. The results may confirm your suspicions or yield surprising outputs that lead to further research.

## The How:

### Word Frequency

- Raw frequency
    - The number of times a word appears in a text
- Relative frequency
    - The number of times a word appears in a text, relative to the size of that text. 
- Example: The word "love" might appear 200 times in a 100,000-word book and 200 times in a 50,000-word book. The word has the same raw frequency in both books, but the 50,000-word book has a higher relative frequency of the word "love" because there are a fewer number of words in the book.

We can look at word frequency using [Voyant Tools](https://voyant-tools.org/){:target='_blank'}. Voyant Tools is an extremely powerful and modular online tool set for visualizing one or many documents.

**Basics of Voyant**

- Variety of tools for reading, finding, analyzing and visualizing digital texts
- No installation or login are required, and you can work with texts in a wide variety of formats (plain text, PDF, XML, MS Word, RTF, etc.)
- Open-source and a work in progress, it may not always work as intended and it's best to approach all observations with some circumspection

Voyant Tools is intended as a tool for exploration and to assist with interpretative practices, it is not intended to tell you what questions to ask or to provide irrefutable results, though you may notice some interesting things and you may be led to construct some compelling interpretations while using it.

{% capture text %}
**Activity: Word Frequency in *Walden***

{% include figure.html img="voyant.jpg" alt="voyant" width="75%" %}

1. Go to [Voyant Tools](https://voyant-tools.org/){:target='_blank'}
2. Upload the walden.txt file we created and cleaned in the previous lesson
3. After uploading your text, you should see a screen with three tool panels along the top and two tool panels along the bottom:

{% include figure.html img="voyant-interface.jpg" alt="voyant interface" width="75%" %}

- [Cirrus](https://voyant-tools.org/docs/#!/guide/cirrus): a kind of word cloud showing the most frequent terms
- [Reader](https://voyant-tools.org/docs/#!/guide/reader): an efficient corpus reader that fetches segments of text as you scroll
- [Trends](https://voyant-tools.org/docs/#!/guide/trends): a distribution graph showing terms across the corpus (or terms within a document)
- [Summary](https://voyant-tools.org/docs/#!/guide/summary): a tool that provides a simple, textual overview of the current corpus
- [Contexts](https://voyant-tools.org/docs/#!/guide/contexts): a concordance that shows each occurrence of a keyword with a bit of surrounding context

"Summary" at the bottom-left and "Cirrus" at the top-left give us the top five most frequent words in the text:

{% include figure.html img="summary.jpg" alt="voyant summary" width="75%" %}

{% include figure.html img="cirrus.jpg" alt="voyant cirrus" width="75%" %}

"Trends" at the top-right allows us to view the relative frequency of the top words in this text as they appear throughout the text. Voyant has separated the text into ten equal segments for this visualization.

{% include figure.html img="trends.jpg" alt="voyant trends" width="75%" %}
{% endcapture %}
{% include alert.md text=text color=secondary %}

**Stopword List**

A stopword is a word (usually a commonly-used word) that an application has been programmed to ignore. Usually, stopword lists contain common words such as a, an, the, and, to, from, etc. Stopword lists are customizable, allowing the researcher to remove words such as character or place names from the analysis. Voyant automatically analyzes your text using a stop word list, but you can delete or edit this list as you see fit.

Compare the following two screenshots. The first uses Voyant's *Auto-detect* stopword setting. In this case, it has recognized this text as English, so it is using a standard English stopword list. The second uses Voyant's *None* stopword setting.

{% include figure.html img="walden-stoplist.jpg" alt="walden with stoplist" caption="Voyant's Cirrus visualization of Walden with an English stopword list" width="75%" %}

{% include figure.html img="walden-nostoplist.jpg" alt="walden without stoplist" caption="Voyant's Cirrus visualization of Walden without a stopword list" width="75%" %}

If you have your own stopword list, you can upload this instead. Or you can simply add words to Voyant's ready-made lists. To add or edit stopwords, click on the `options` icon in the top right of the visualization. This will produce a dialog box where you can select a list or edit it. 

<div class="text-center">{% include figure.html img="voyant-options.jpg" alt="voyant options tab" caption="Click on the 'options' tab (upper right)" width="75%" %}</div>

{% include figure.html img="stoplist.jpg" alt="voyant stoplist dropdown" caption="Voyant's stoplist options" width="75%" %}


{% capture text %}
**Activity: Voyant Stop Words**

{% endcapture %}
{% include alert.md text=text color=secondary %}

### Word Concordance
- Looking at the context of your words

### Other Voyant Tools

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
**Exploration Time**
Using a text corpus of your choice, or the Austen or Shakespeare corpuses that Voyant provides, spend some time exploring various Voyant tools:
{% endcapture %}
{% include alert.md text=text color=secondary %}

{% capture text %}
**Reflection Time** 
- What insights, if any, do these tools provide?
- Are there patterns or in/consistencies?
- How might your 'read' groups of words?
- What keywords or patterns did you pursue and why?
- What are the values/limitations of 'not reading' this way?
{% endcapture %}
{% include alert.md text=text color=secondary %}

### Word Tree
- Visualizing context with [WordTree](https://www.jasondavies.com/wordtree/)

