---
title: Machine Learning
nav: true
---

# Machine Learning

## Natural Language Processing
- An example of supervised machine learning
- [Natural Language Understanding Demo](https://natural-language-understanding-demo.ng.bluemix.net/)
- Sentiment Analysis with books [Book Visualizations Sandbox](https://observablehq.com/@bmschmidt/book-visualizations-sandbox?htid=pst.000061166424)
- [Software 2.0](https://medium.com/@karpathy/software-2-0-a64152b37c35) (work on curating training data sets, rather than developing software, machine learning does the rest!)

-----------------

## Topic Modeling

{% capture text %}
- Text mining that allows the user to identify patterns in a corpus of texts
    - **Input**: texts 
    - **Output**: several lists of words that appear in the texts
- Groups words across the corpus into clusters of words, or "topics" based on those words similarity and dissimilarity
- In a good topic model, the words in a topic make sense (for example: "navy, ship, captain" and "tobacco, farm, crops")
- Usually works best on large bodies of text
- Some familiarity with your text is important
    - See ["When you have a MALLET, everything looks like a nail"](http://sappingattention.blogspot.com/2012/11/when-you-have-mallet-everything-looks.html) for an example of what can happen when you're not familiar with your data or the tools you're using
{% endcapture %}
{% include card.md text=text header="A few basics of topic modeling" %}

Topic modeling is an example of **unsupervised machine learning**
- You have input data but don't know the output variables
- Used as a process to find meaningful structure and groupings in your data

**Latent Dirichlet Allocation (LDA)**
- A type of topic modeling
- Matt Jockers's Topic Modeling "Fable" ([LDA Buffet](http://www.matthewjockers.net/2011/09/29/the-lda-buffet-is-now-open-or-latent-dirichlet-allocation-for-english-majors/))

**What to do with your output?**
- [Mining the Dispatch](http://dsl.richmond.edu/dispatch/pages/intro){:target='_blank'}

{% capture text %}
**Topic Modeling Activity** 
- Topic modeling in-browser with [jsLDA](https://mimno.infosci.cornell.edu/jsLDA/)
{% endcapture %}
{% include alert.md text=text color=secondary %}

Don't be afraid to fail or get bad results. Topic modeling is exploratory, and sometimes you have to play around with it before you know what settings work best for your project.

-----------------

## Exploring big data

**Google Books [Ngram Viewer](https://books.google.com/ngrams){:target='_blank'}**

<div class="pb-3" style="max-width:854px"><div style="position:relative;height:0;padding-bottom:56.25%"><iframe src="https://embed.ted.com/talks/lang/en/what_we_learned_from_5_million_books" width="854" height="480" style="position:absolute;left:0;top:0;width:100%;height:100%" frameborder="0" scrolling="no" allowfullscreen></iframe></div></div>

-----------------

## Having fun with text generators
- [Talk to Transformer](https://talktotransformer.com/)