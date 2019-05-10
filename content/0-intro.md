---
title: Introduction
nav: true
layout: default
--- 

# Intro to Text as Data
- Bag of words
- Digital text is massively addressable at different levels of scale (Michael Witmore, "Text: A Massively Addressable Object")

## Selecting and getting to know a corpus
- Where to find texts
    - Depending on what you're going to do with your texts, you'll need to pay attention to whether or not they are in public domain. Texts that are no longer under copyright are usually easier to use for analytical research because they have a greater likelihood of already being digitized. (Of course, this also has the effect of skewing text research in DH so that it focuses more on older literary works.) A good resource to use if you're wondering whether something is under copyright is Cornell University Library's [Copyright Information Center](https://copyright.cornell.edu/publicdomain). Currently, most works published before 1924 are in the public domain.
    - [Project Gutenberg](https://www.gutenberg.org/)
        - 
    - [HathiTrust](https://www.hathitrust.org/)
- Getting to know your corpus
    - Text analysis allows us to look at the big picture, usually allowing us to explore broad patterns that span large bodies of text. However, this doesn't absolve you from actually having to read some of the text you are analyzing. In order to understand the outputs from the algorithms you run on your text, and to be sure that the results you are getting are actually valid, you need to be somewhat familiar with the text you are analyzing.
    - 
## Defining Units of Analysis
- OCR (Optical Character Recognition)

{% capture text %}
1. **Digitization** (make high quality scans)
2. **Image preprocessing** (deskew, scale remove borders, high-pass filter)
3. **Layout detection and segmentation** (identify organization and lines of text to pass to OCR)
4. **OCR** (feature extraction)
5. **Text post-processing** (adaptive recognition, lexicons, co-occurence, noise reduction)
{% endcapture %}
{% include card.md text=text header="Traditional OCR Workflow" %}



- Text cleaning (regular expressions)
