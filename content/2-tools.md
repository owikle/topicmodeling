---
title: Tools
nav: true
---

# Tools

{:.pt-4}
There are various tools that can be used to employ topic modeling, including Python and R. Here, we'll discuss a program called [Mallet](http://mallet.cs.umass.edu/){:target='_blank'}

---
{:.pb-3}

## Mallet

- Command-line tool

- Easy to run with this tutorial: [Programming Historian Guide to Mallet](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet){:target='_blank'}

##### Under the Hood: Latent Dirichlet Allocation
{:.pb-2}

Mallet uses an algorithm called Latent Dirichlet Allocation (LDA) that works in this way:

- You assign the algorithm the number of topics (X) you want it to produce, and the number of times (Z) you want it to run on your documents

- The model then goes through each of your documents and randomly assigns each word to one of X topics

- After the first iteration, you have some pretty terrible topics

- But luckily you've assigned the model to iterate Z times! (This is the important part...)

- The model runs Z times, each time assessing the probability that Word A appears in each topic, and the probability that Topic B appears in each document

- After so many iterations, the model gets pretty good at clustering words that are likely to appear near each other across all the documents in your corpus

- Your end-product is a list of these clusters (or "topics"), and a data file containing the percentage of each topic's presence in each of your documents

{:.pt-3}
#### Still Confused? Want to Know Specifics?
{:.pb-2}

{% capture jockers %}
- Matt Jockers's Topic Modeling "Fable" ([LDA Buffet](http://www.matthewjockers.net/2011/09/29/the-lda-buffet-is-now-open-or-latent-dirichlet-allocation-for-english-majors/)) is a really great, non-technical entry into how LDA works.

- David Blei invented LDA. Check out his article [Introduction to Probabilistic Topic Models](https://m-cacm.acm.org/magazines/2012/4/147361-probabilistic-topic-models/fulltext?mobile=true) in *Communications of the ACM* for further information about the algorithms LDA uses.
{% endcapture %}
{% include card.md text=jockers %}

---
{:.pb-3}

## Modifying Your Output

- **Stopword List**: 
A stopword is a word (usually a commonly-used word) that an application has been programmed to ignore. 
Usually, stopword lists contain common words such as a, an, the, and, to, from, etc. 
Sometimes, it can be useful to add common words like person names or place names, depending on what your research question is. Stopword lists are customizable, allowing the researcher to remove words such as character or place names from the analysis. 

- **Parameters**:
Change the number of iterations, topics, and other more complex parameters (see [Mallet Documentation](http://mallet.cs.umass.edu/topics.php) for more details)

---
{:.pb-3}

## Other Tools

- [Overview Docs](https://www.overviewdocs.com/), online tool designed for journalists to sort through huge data sets
- [jsLDA](https://mimno.infosci.cornell.edu/jsLDA/), facilitates in-browser topic modeling using LDA

---
{:.pb-3}