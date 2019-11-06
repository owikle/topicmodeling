---
title: Activity
nav: true
---

{% capture text %}
**Topic Modeling Activity** 
- Topic modeling in-browser with [jsLDA](https://mimno.infosci.cornell.edu/jsLDA/)
    - Explore a sample corpus of <a href="../data/austen.zip">Jane Austen texts</a>
        - Click on the link above, unzip the downloaded file. Inside you'll find a text file of Austen's corpus, along with a stopword list. Upload both of these files to jsLDA. 
    - You can also try it with your own corpus. Just make sure your text file is formated correctly:
        - One document per line, with each document consisting of `[doc ID] [tab] [label] [tab] [text...]`
        - If you need to get rid of line breaks in your text, try the following regex:
            - Find `([\n\r])+`
            - Replace a space
{% endcapture %}
{% include alert.md text=text color=secondary %}

Don't be afraid to fail or get bad results. Topic modeling is exploratory, and sometimes you have to play around with it before you know what settings work best for your project.


{% capture text %}
**Reflection Time** 
- What insights, if any, do these tools provide?
- Are there patterns or in/consistencies?
    - Do you trust these patterns? Could you verify their accuracy somehow?
- How might your 'read' groups of words?
- What keywords or patterns did you pursue and why?
- What are the values/limitations of 'not reading' this way?
{% endcapture %}
{% include alert.md text=text color=secondary %}

LDA and its relatives are valuable exploratory methods, but I’m not sure how much value they will have as evidence.
For one thing, they require you to make a series of judgment calls that deeply shape the results you get (from choosing stopwords, to the number of topics produced, to the scope of the collection).
The resulting model ends up being tailored in difficult-to-explain ways by a researcher’s preferences.