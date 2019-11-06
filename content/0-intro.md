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
- **Text Mining**: A general term encompassing several different types of automated discovery using a body of texts. Topic modeling is a type of text mining.

- **Topic**: (Discourse/theme): A group of words that have a high likelihood of clustering together.

- **Document**: A discrete unit of text. This can be a blog post, a book chapter, a book, a journal article, a diary entry, etc. For topic modeling, you determine what a document is depending on the nature of the corpus or the kind of results you're looking for. 

    - Because topics arise from documents, it is wise to think carefully about how to segment your data: For example, if your text is 25,000 emails, do you treat each one as a document?  All emails by a specific author as a single document?  The choices you make at this stage will directly affect your outcomes and the way you interpret them.

{:.pt-2}
- **Corpus**: A collection of documents ("body of text"). 
{% endcapture %}
{% include card.md text=terms header="Terms to Know" %}

{:.pt-3}
#### Basics of Topic Modeling:

- Text mining that allows the user to identify patterns in a corpus of texts
    - **Input**: text documents 
    - **Output**: several clusters of words that appear in the documents
- Groups words across the corpus into clusters of words, or "topics" based on those words' similarity and dissimilarity
- Sometimes topics are easy to identify (for example: "navy, ship, captain"). Other times they're more ambiguous.

---
{:.pb-3}

