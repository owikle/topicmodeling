---
title: Use
nav: true
--- 

# How to Use Topic Modeling

{:.pt-3}
- [Why Use Topic Modeling](#why)
- [Input Data and Where to Find It](#data)
- [What To Do With Your Topics](#topics)

{:.pt-4 #why}
## Why Use Topic Modeling?

- For exploration, hypothesis generation
    - Playing around with text (even if you don't know what you're doing) can be an effective way to gain a new perspective on the texts you study
    - The results may confirm your suspicions or yield surprising outputs that lead to further research
- For gaining insight into a corpus of text that is too large to read

{% capture when %}
Short answer: when interpreting large bodies of text

A very small corpus is unlikely to yield many useful or specific topics; larger corpora usually generate better results.  This is because topic modeling is a machine learning process: the more training data the modeling program has, the more refined its topics become over time. 

However, just because you *can* use topic modeling doesn't necessarily mean you should. If you're thinking seriously about whether it's useful for your project, check out Matthew Kirschenbaum’s [The Remaking of Reading: Data Mining and the Digital Humanities](https://www.csee.umbc.edu/~hillol/NGDM07/abstracts/talks/MKirschenbaum.pdf) and Stephen Ramsay’s book, [Reading Machines](https://www.press.uillinois.edu/books/catalog/75tms2pw9780252036415.html).
{% endcapture %}
{% include card.md title="When Does Topic Modeling Work Best?" text=when %}

---
{:.pb-3 #data}

## Input Data and Where to Find It

Before you start topic modeling, you'll need to make sure you have the right type of data in the correct formats.

{:.pt-3}
#### Text as a "Bag of Words":
{:.pb-2}

{% capture text %}
- **Structured data**: Data with fixed fields (key/value pairs, relations)
    - Example: csv of names, phone numbers, dates, zip codes
- **Unstructured data**: No computer-readable structure or relationships between units of analysis
    - Example: un-coded text
{% endcapture %}
{% include card.md text=text header="Structured Data vs. Unstructured Data" %}

Topic modeling utilizes unstructured data, in the form of **plain text** files:

**Plain text** files are text files, i.e. contain only characters like `a`, `1`, `<`, `!`, etc. 
(Some characters might be hidden control characters, such as tabs and line breaks.) 
Having text in this simple format enables it to be manipulated as data.

{% capture sites %}
- [Project Gutenberg](https://www.gutenberg.org/){:target='_blank'}
    - Full text of thousands of free books. Text is usually fairly clean, but often little bibliographic information.
- [Archive.org](https://archive.org/){:target='_blank'}
    - Full texts and scans of books, lots of different download options from epub to pdf, to plain text.
- [HathiTrust](https://www.hathitrust.org/){:target='_blank'}
    - Millions of digitized books, public domain and copyrighted. Cleanliness of text varies. More advanced features require institutional membership.
- [DH Toychest](http://dhresourcesforprojectbuilding.pbworks.com/w/page/69244469/Data%20Collections%20and%20Datasets){:target='_blank'}
    - Varied textual data compiled, cleaned, and organized by Alan Liu. These are good sets to use when you're learning how to explore and experiment with topic modeling or any other type of text analysis.
{% endcapture %}
{% include card.md text=sites header="Where to find plain text files for topic modeling:" %}

{:.pt-3}
#### Getting to Know Your Corpus
{:.pb-2}

As a type of 'distant reading,' topic modeling allows us to look at the big picture, enabling us to explore broad patterns that span large bodies of text.

However, **this doesn't absolve you from actually having to read some of the text you are modeling**:
In order to understand the outputs from the algorithms you run on your text (and to be sure that the results you are getting are actually valid), you need to be somewhat familiar with the text you are modeling.

- See ["When you have a MALLET, everything looks like a nail"](http://sappingattention.blogspot.com/2012/11/when-you-have-mallet-everything-looks.html) for an example of what can happen when you're not familiar with your data or the tools you're using

{:.pt-3}
#### Preparing Your Texts (cleaning, formatting, separating)
{:.pb-2}

Selection and cleaning of corpora can be the most time- and labor-intensive aspects of topic modeling, and topic modeling outcomes depend on the quality and volume of data in the corpus: 
You'll want to make sure your documents' text is clean enough that you can interpret the topics that are produced. See this site's [Resources](/resources) page for text cleaning techniques and tools.

Decide what you want your "document" to be (paragraph, chapter, letter, book, etc.), and split up your text accordingly.

---
{:.pb-3 #topics}

## What To Do With Your Topics

{:.pt-3}
#### Interpret
{:.pb-2}

Example Topics: 

`heard thought see looked look countenance made man good voice told called heard round knew spoke rose make looking began`

`night door long appeared passed light place hand heard present eyes time gave fear found person air sound left young`

See Ted Underwood, [Topic Modeling Made Just Simple Enough](https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/){:target='_blank'}:

{:.mx-4}
"I want this technique to point me toward something I don’t yet understand, and I almost never find that the results are too ambiguous to be useful. The problematic topics are the intuitive ones — the ones that are clearly about war, or seafaring, or trade. I can’t do much with those."

{:.pt-3}
#### Visualize
{:.pb-2}

Make graphs using Excel or [Tableau](https://www.tableau.com/){:target='_blank'}

{% include figure.html img="figure-06.png" alt="graphing topics" width="100%" %}

{:.pt-3}
#### Examples
{:.pb-2}

- Robert Nelson, [Mining the Dispatch](http://dsl.richmond.edu/dispatch/pages/intro){:target='_blank'}
- Cameron Blevins, [Topic Modeling Martha Ballard's Diary](http://www.cameronblevins.org/posts/topic-modeling-martha-ballards-diary/){:target='_blank'}
- [Journal of Digital Humanities 2.1 (winter 2012)](http://journalofdigitalhumanities.org/2-1/){:target='_blank'}

---
{:.pb-3}