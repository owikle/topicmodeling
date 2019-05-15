---
title: Machine Learning
nav: true
---

# Machine Learning: Explore a Corpus of Texts

## Natural Language Processing
- An example of `supervised machine learning`
- [Natural Language Understanding Demo](https://natural-language-understanding-demo.ng.bluemix.net/)
- Sentiment Analysis with books [Book Visualizations Sandbox](https://observablehq.com/@bmschmidt/book-visualizations-sandbox?htid=pst.000061166424)
- [Software 2.0](https://medium.com/@karpathy/software-2-0-a64152b37c35) (work on curating training data sets, rather than developing software, machine learning does the rest!)

## Topic Modeling

- Text mining that allows the user to identify patterns in a corpus of texts
    - Input: texts - Output: several lists of words that appear in the texts
- Groups words across the corpus into clusters of words, or "topics" based on those words similarity and dissimilarity
    - ["a recurring pattern of co-occurring words"](https://twitter.com/footnotesrising/status/264823621799780353)
- In a good topic model, the words in a topic make sense (for example: "navy, ship, captain" and "tobacco, farm, crops")
- Usually works best on large bodies of text
- Some familiarity with your text is important

Latent Dirichlet Allocation (LDA)
- A type of topic modeling
- Matt Jockers's "Fable" ([LDA Buffet](http://www.matthewjockers.net/2011/09/29/the-lda-buffet-is-now-open-or-latent-dirichlet-allocation-for-english-majors/))

Topic modeling as a heuristic, not as evidence
- Requires a series of judgment calls that deeply shape the results you get
    - You must choose stopwords, number of topics and iterations, and the scope of your collection of text
- "If fishing for interesting patterns in a large collection of documents, probabilistic techniques are the way to go" - [Ted Underwood](https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/)

An example of **unsupervised machine learning**
- You have input data but don't know the output variables
- Used as a process to find meaningful structure and groupings in your data

Visualizing your topic model
- [Old Bailey Online](https://www.oldbaileyonline.org/){:target='_blank'}
- [Mining the Dispatch](http://dsl.richmond.edu/dispatch/pages/intro){:target='_blank'}

{% capture text %}
**Topic Modeling Activity** 
[jsLDA](https://mimno.infosci.cornell.edu/jsLDA/): topic modeling in-browser
{% endcapture %}
{% include alert.md text=text color=secondary %}

Don't be afraid to fail or get bad results. Topic modeling is exploratory, and sometimes you have to play around with it before you know what settings work best for your project.

## Resources

Megan R. Brett, [Topic Modeling: A Basic Introduction](http://journalofdigitalhumanities.org/2-1/topic-modeling-a-basic-introduction-by-megan-r-brett/)

Ted Underwood, [Topic Modeling Made Just Simple Enough](https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/)

Scott Weingart, [Topic Modeling for Humanists: A Guided Tour](http://www.scottbot.net/HIAL/index.html@p=19113.html)

[Mallet](http://mallet.cs.umass.edu/) (Developed by David Mimno)
- [Programming Historian Guide to Mallet](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet)


## Exploring big data
- Google Books [Ngram Viewer](https://books.google.com/ngrams)

<div style="max-width:854px"><div style="position:relative;height:0;padding-bottom:56.25%"><iframe src="https://embed.ted.com/talks/lang/en/what_we_learned_from_5_million_books" width="854" height="480" style="position:absolute;left:0;top:0;width:100%;height:100%" frameborder="0" scrolling="no" allowfullscreen></iframe></div></div>

## Having fun with text generators
- [Talk to Transformer](https://talktotransformer.com/)