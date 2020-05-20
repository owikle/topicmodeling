---
title: Activity
nav: true
---

# Topic Modeling Activity

{:.pt-4}
**Topic modeling in-browser with [jsLDA](https://mimno.infosci.cornell.edu/jsLDA/){:target='_blank'}**

Time to experiment! Download these texts and upload them to jsLDA:
- **[Frankenstein; Or, The Modern Prometheus](../data/frankenstein.zip)** by Mary Wollstonecraft Shelley (Retrieved from [Project Gutenberg](https://www.gutenberg.org/ebooks/84) and formatted for jsLDA)
- **[U.S. Presidents' Inaugural Speeches](../data/presidents.zip)** (Retrieved from [DH Toychest](http://dhresourcesforprojectbuilding.pbworks.com/w/page/69244469/Data%20Collections%20and%20Datasets) and formatted for jsLDA: all 57 inaugural speeches from Washington through Obama collected from the American Presidency Project with the assistance of project co-director John T. Woolley; assembled as individual plain-text files by Alan Liu)
- **[Lyrical Ballads, 1798](../data/wordsworth.zip)** by William Wordsworth with Samuel Taylor Coleridge (Retrieved from [DH Toychest](http://dhresourcesforprojectbuilding.pbworks.com/w/page/69244469/Data%20Collections%20and%20Datasets) and formatted for jsLDA; assembled by Alan Liu from Project Gutenberg)

Add a stopword list: [NLTK's list of english stopwords](https://gist.github.com/sebleier/554280) (you can also download this same list as a text file here: **[stopwords](../data/stopwords.zip)**)


You can also try it with your own corpus. Just make sure your text file is formated correctly:
- One document per line, with each document consisting of `[doc ID] [tab] [label] [tab] [text...]`

{:.card .card-body .card-text}
Don't be afraid to fail or get bad results. 
Topic modeling is exploratory, and sometimes you have to play around with it before you know what settings work best for your project.

---
{:.pb-3}

{% capture text %}
**Reflection Time** 
- What insights, if any, does topic modeling provide?
- What are the values/limitations of 'not reading' this way?
- How might the judgment calls you have to make (choosing stopwords, number of topics produced, scope of collection) affect your use of your results as evidence?
{% endcapture %}
{% include alert.md text=text color=secondary %}

{:.pb-3}