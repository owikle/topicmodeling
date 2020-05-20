---
title: Tools
nav: true
---

# Tools

{:.pt-4}
There are various tools that can be used to employ topic modeling, including Python and R. 
Here, we'll discuss a program called [MALLET](http://mallet.cs.umass.edu/){:target='_blank'} and the statistical model it uses.

---
{:.pb-3}

## MALLET

- Natural language processing toolkit
- Command line tool
- Easy to run with this tutorial: [Programming Historian Guide to MALLET](https://programminghistorian.org/en/lessons/topic-modeling-and-mallet){:target='_blank'}

{:.pt-3}
##### Under the Hood: Latent Dirichlet Allocation
{:.pb-2}

MALLET uses an algorithm called [Latent Dirichlet Allocation](http://jmlr.csail.mit.edu/papers/v3/blei03a.html){:target='_blank'} (LDA) that works in this way:

- Begin by gathering a set of documents you want to model

- Assign the algorithm the number of topics (X) you want it to produce, and the number of iterations (Z) you want it to run on your documents

- The model then goes through each of your documents and randomly assigns each word to one of X topics

- After the first iteration, you have some pretty terrible topics

- But luckily you've assigned the model to iterate Z times! (This is the important part...)

- The model runs Z times, each time assessing the probability that Word A appears in each *topic*, and the probability that Topic B appears in each *document*

- After so many iterations, the model gets pretty good at clustering words that are likely to appear in similar contexts across all the documents in your corpus

- Your end-product is a list of these clusters (or "topics")...

{% include figure.html img="topics.png" width="100%" caption="List of Topics" %}

...and a data file containing the percentage of each topic's presence in each of your documents:

{% include figure.html img="distribution.png" width="100%" caption="Percentage of Each Topic" %}

{% include figure.html img="model.jpg" width="100%" caption="David M. Blei, <a href='https://m-cacm.acm.org/magazines/2012/4/147361-probabilistic-topic-models/fulltext?mobile=true'>Probabilistic Topic Models</a>" %}

{:.pt-3}
#### Still Confused? Want to Know Specifics?
{:.pb-2}

{% capture jockers %}
- Matt Jockers's Topic Modeling "Fable" ([LDA Buffet](http://www.matthewjockers.net/2011/09/29/the-lda-buffet-is-now-open-or-latent-dirichlet-allocation-for-english-majors/){:target='_blank'}) is a really great, non-technical entry into how LDA works.

- David Blei invented LDA. Check out his article [Introduction to Probabilistic Topic Models](https://m-cacm.acm.org/magazines/2012/4/147361-probabilistic-topic-models/fulltext?mobile=true){:target='_blank'} in *Communications of the ACM* for further information about the algorithms LDA uses.
{% endcapture %}
{% include card.md text=jockers %}

---
{:.pb-3}

## Modifying Your Output

- **Stopword List**: A stopword is a word (usually a commonly-used word) that an application has been programmed to ignore. 
Usually, stopword lists contain common words such as a, an, the, and, to, from, etc. 

    - Sometimes, it can be useful to add common words like person names or place names, depending on what your research question is. 
    Stopword lists are customizable, allowing the researcher to remove words such as character or place names from the analysis. 

{:.pt-2}
- **Parameters**: Change some aspects of how the MALLET program is running (number of iterations, topics, and other more complex parameters) to achieve a different output (see [MALLET Documentation](http://mallet.cs.umass.edu/topics.php){:target='_blank'} for more details)

---
{:.pb-3}

## Other Tools

- [Overview Docs](https://www.overviewdocs.com/){:target='_blank'}, online tool designed for journalists to sort through huge data sets
- [jsLDA](https://mimno.infosci.cornell.edu/jsLDA/){:target='_blank'}, facilitates in-browser topic modeling using LDA

---
{:.pb-3}