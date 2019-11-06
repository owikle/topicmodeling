---
title: Intro
nav: true
---

# Introducing Topic Modeling

{:.pt-4}
Topic modeling is a type of Machine Learning...

{:.pt-4}
## Machine Learning (ML)

ML is the application of algorithms and statistical modeling to allow computers to "learn" from data to do a task (often overlapping or used interchangeably with Artificial Intelligence / AI).

ML tasks are broadly separated into *supervised* or *unsupervised* learning.
Supervised learning tasks typically involve feeding the algorithm a labeled training data set which is used to build a model that can then classify unknown items, making inferences based on what it knows. 
Unsupervised learning tasks involve feeding unlabeled data to an algorithm that can identify patterns and clustering in the grouping. 

---
{:.pb-3}

## Topic Modeling

Topic modeling is an example of **unsupervised machine learning**
- You supply input data but don't know the output variables
- The algorithm finds structure and groupings in your data; you apply meaning
{:.pb-3}

{% capture terms %}
- **Text Mining**: A general term encompassing several different types of automated discovery from a corpus of texts.  In common use, "text mining" often refers to topic modeling. 

- **Corpus**:  A collection of documents.  Selection and cleaning of corpora can be the most time- and labor-intensive aspects of topic modeling, and topic modeling outcomes directly depend on the quality and volume of data in the corpus. A very small corpus is unlikely to yield many useful or specific topics; larger corpora (250,000+ words) usually generate better results.  This is because topic modeling is essentially a machine learning process: the more training data the modeling program has, the more refined its topics become over time. 

- **Document**:  A discrete logical unit of text.  For topic modeling, documents can vary in length depending on the nature of the corpus or the kind of data you hope to surface.  Because topics arise from documents, it is wise to think carefully about how to segment your data.  For example, if you have 25,000 emails, do you treat each one as a document?  All emails by a given author as a single document?  The choices you make at this stage will directly affect your outcomes.
    - It’s worth noting that a “document” is defined somewhat flexibly. For example, we can call every paragraph in a book its own “document,” and run LDA over the individual paragraphs. The more often words are used together within a document, the more related they are to one another.

- **Topic**: A group of words that have a high likelihood of clustering together.  ("High" is relative, of course; we might also say "any likelihood," depending on the number of topics and the size of the corpus.)  For the purposes of topic modeling, topics are a probability distribution over words. 
{% endcapture %}
{% include card.md text=terms header="Terms to Know" %}

#### Basics of Topic Modeling

- Text mining that allows the user to identify patterns in a corpus of texts
    - **Input**: texts 
    - **Output**: several lists of words that appear in the texts
- Groups words across the corpus into clusters of words, or "topics" based on those words' similarity and dissimilarity
- Sometimes topics are easy to identify (for example: "navy, ship, captain"). Other times they're more ambiguous.
- Usually works best on large bodies of text
- Some familiarity with your text is important
    - See ["When you have a MALLET, everything looks like a nail"](http://sappingattention.blogspot.com/2012/11/when-you-have-mallet-everything-looks.html) for an example of what can happen when you're not familiar with your data or the tools you're using

---
{:.pb-3}

- **Topic Modeling**: A probabilistic technique for determining (and locating) words that are likely to cluster together as "topics" across a set of documents. It's a method of analyzing a collection of documents to infer what topics (aka discourses, or themes) might have generated them.

---
{:.pb-3}

