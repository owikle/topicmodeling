---
title: Introduction
nav: true
--- 

# Intro to Text as Data

Utilizing text as data requires breaking down a text into smaller units of analysis. Doing so allows us to see patterns and approach text from different points of entry.

In text analysis (also referred to as text mining), units of analysis tend to be groupings of text (broken up as discrete books, documents, poems, etc.), and words. Much of the time spent doing text analysis research is spent preparing text so that these smaller units of analyses can be accessed by the digital tools we use.

## Selecting and getting to know a corpus

**Where to find texts**
- Depending on what you're going to do with your texts, you'll need to pay attention to whether or not they are in public domain. Texts that are no longer under copyright are usually easier to use for analytical research because they have a greater likelihood of already being digitized. (Of course, this also has the effect of skewing text research in DH so that it focuses more on older literary works.) A good resource to use if you're wondering whether something is under copyright is Cornell University Library's [Copyright Information Center](https://copyright.cornell.edu/publicdomain). Currently, most works published before 1924 are in the public domain.

- [Project Gutenberg](https://www.gutenberg.org/)
    - Full text of thousands of free books. Text is usually fairly clean, but often little bibliographic information.
- [Archive.org](https://archive.org/)
    - Full texts and scans of books, lots of different download options from epub to pdf, to plain text.
- [HathiTrust](https://www.hathitrust.org/)
    - Millions of digitized books, public domain and copyrighted. Cleanliness of text varies. More advanced features require institutional membership.

{% capture text %}
**Activity: Find a Text**
1. Go to [https://archive.org/details/waldenorlifeinwo1854thor/page/n3](https://archive.org/details/waldenorlifeinwo1854thor/page/n3){:target='_blank'}, the record for an 1854 edition of Henry David Thoreau's Walden on [Archive.org](https://archive.org/)
2. Take a look at the download options on the right side of the page. At the bottom of this box, click on `SHOW ALL`
3. Click on the .txt file (`waldenorlifeinwo1854thor_djvu.txt`). This opens the text in a new tab. Select all of this text, copy it, and paste it into a new file in Visual Studio Code.
4. Save this file as walden.txt
5. Take a moment to refer back to the digitized pages of the book. How are the layout and content of the original images transformed in the text file you just created?
{% endcapture %}
{% include alert.md text=text color=secondary %}

**Getting to know your corpus**
- Text analysis allows us to look at the big picture, usually enabling us to explore broad patterns that span large bodies of text. However, this doesn't absolve you from actually having to read some of the text you are analyzing. In order to understand the outputs from the algorithms you run on your text, and to be sure that the results you are getting are actually valid, you need to be somewhat familiar with the text you are analyzing.
- See ["When you have a MALLET, everything looks like a nail"](http://sappingattention.blogspot.com/2012/11/when-you-have-mallet-everything-looks.html) for an example of what can happen when you're not familiar with your data or the tools you're using.

## Defining Units of Analysis

{% include figure.html img="letters.jpg" alt="rich text" width="75%" %}

Usually when people analyze text, they are interested in words (i.e. word frequency, order, meaning). Therefore, a primary part of preparing your text for research is making sure the words in your corpus are identifiable units of measurement. You may start your project with scanned images of book pages. What format do you need to transform this text to, and how will you accomplish that transformation?

**Thinking of Text as a "Bag of Words"**

{% capture text %}
- **Structured data**: Data with fixed fields (key/value pairs, relations)
    - Example: csv of names, phone numbers, dates, zip codes
- **Unstructured data**: Boundaries of individual items, relations between items, meaning of items are not computer-readable
    - Example: un-coded text
{% endcapture %}
{% include card.md text=text header="Structured Data vs. Unstructured Data" %}

In textual research in the digital humanities, usually we are working with unstructured data.

Below you'll find definitions and examples of [file type](#file), [OCR](#ocr), and [text cleaning](#clean)


### <a name="file">File Type</a>

{% capture text %}
Two types of computer files: **Text** and **Binary**

- **Text Files** contain bytes that represent text characters organized in lines (e.g. `a`, `B`, space, tab, line breaks, etc.). It can be opened with a text editor to see the characters.
- **Binary Files** contain bytes that are NOT text characters. It will require software (other than a text editor) that can correctly interpret the bytes. For example, a JPG image, MP3 sound file, or a ZIP compressed folder.
{% endcapture %}
{% include card.md text=text header="Text and Binary Files" %}

Usually, when talking about text files, we mean **plain text**.
It is defined by [Unicode standard](https://www.unicode.org/) as:

{% capture text %}
"Plain text is a pure sequence of character codes; plain Unicode-encoded text is therefore a sequence of Unicode character codes."
{% endcapture %}
{% include card.md text=text %}

Plain text files are text files, i.e. contain only characters like `a`, `1`, `<`, `!`, etc. 
Some characters might be "hidden" control characters, such as tabs and line breaks. 

There are tools that make the process of transferring your text to plain text easier. If you are starting with images or pdfs, optical character recognition (OCR) is a good place to start.

### <a name="ocr">OCR (Optical Character Recognition)</a>

OCR identifies printed or handwritten text characters in digital images of physical documents. Once translated by the OCR software, the characters can be recognized as text by the computer, allowing a document's content to be processed and manipulated as data.

{% capture text %}
1. **Digitization** (make high quality scans)
2. **Image preprocessing** (deskew, scale remove borders, high-pass filter)
3. **Layout detection and segmentation** (identify organization and lines of text to pass to OCR)
4. **OCR** (feature extraction)
5. **Text post-processing** (adaptive recognition, lexicons, co-occurrence, noise reduction)

(adapted from Evan Williamson's [OCR: Workflows and Data](https://osf.io/gd5ka/){:target='_blank'})
{% endcapture %}
{% include card.md text=text header="Traditional OCR Workflow" %}

**Example:**

{% include figure.html img="spider-letter.jpg" alt="spiderman fan mail" caption="Spiderman fan mail from 1978" width="75%" %}

{% include figure.html img="abbyy.jpg" alt="ocr" caption="OCR with ABBYY FineReader" width="75%" %}

{% include figure.html img="spiderman.jpg" alt="spiderman text" caption="OCR results (.txt)" width="75%" %}

**OCR Software:**

Tesseract
- Open source, ready-to-use package available: [https://github.com/tesseract-ocr/tesseract](https://github.com/tesseract-ocr/tesseract)
- Docs: [https://tesseract-ocr.github.io/](https://tesseract-ocr.github.io/)
- Wiki: [https://github.com/tesseract-ocr/tesseract/wiki](https://github.com/tesseract-ocr/tesseract/wiki)

ABBYY FineReader
- Proprietary, but commonly used: [https://www.abbyy.com/en-us/finereader/](https://www.abbyy.com/en-us/finereader/)

[Adobe Creative Cloud](https://www.adobe.com/creativecloud.html) has OCR capabilities

OCRopus/OCRopy
- Python-based, more DIY/modular, but used in research with some advancements possible with customized models: [https://github.com/tmbdev/ocropy](https://github.com/tmbdev/ocropy)
- Recent article: [http://www.digitalhumanities.org/dhq/vol/11/2/000288/000288.html](http://www.digitalhumanities.org/dhq/vol/11/2/000288/000288.html)


### <a name="clean">Text Cleaning</a>

After you've OCRd your text and transferred it to plain text format, you will likely discover errors in your new text file(s). OCR is not perfect. Especially if you are using older texts, you might encounter problems such as your s's looking like f's:

{% include figure.html img="italian.jpg" alt="italian" caption="The Italian, Ann Radcliffe (1797)" width="75%" %}

{% include figure.html img="italian-text.jpg" alt="italian text" caption="Plain text, after OCR" width="75%" %}

Or maybe your book came with a large amount of front matter that you'd like to get rid of:

{% include figure.html img="italian-front.jpg" alt="italian front matter" caption="Front matter from The Italian, first edition (1797)" width="75%" %}

Find and replace might help with some of these problems, but for others you need a stronger tool. In this case, a lot of people will use Regular Expressions. Regular Expressions are sequences of symbols and characters expressing a string to be searched for within a text. They can get very complicated and are not very intuitive, so we won't spend too much time with them now, but we'll apply a few here just to get a taste. 

{% capture text %}
**Activity: Clean Your Text With Regular Expressions**
1. Open walden.txt in Visual Studio Code (if you've misplaced it you can also download it here: <a href="../data/walden.txt">walden.txt</a>)
2. Delete the front matter
3. Click on `Edit > Find` (`cmd + F` on mac or `ctl + F` on pc) to open a search box, which should appear in the top right-hand corner of your window in Visual Studio Code
4.  On the right side of the search box, you'll see a button with this symbol: `.*`. If you hover over this button, the phrase `Use Regular Expression` appears. Click on this button

{% include figure.html img="regex1.jpg" alt="vs code search" caption="Search Box in VS Code" width="100%" %}

**Remove sets of page titles and page numbers:**
1. In the search box, type: `^[A-Z]+\.\s\d+`
    - `^` starts at the beginning of a line, `[A-Z]+` finds one or more letter characters, `\.` finds a period, `\s` finds a space, `\d+` finds one or more digits (numbers)
2. Toggle the arrow to the left of the search box. To the right of the box that says `Replace`, you'll see two buttons. One lets you replace one instance at a time, the other lets you replace all instances at once
3. To get rid of page titles with two words, add a space and another set of letter characters (`\s[A-Z]+`): `^[A-Z]+\s[A-Z]+\.\s\d+`
4. To get rid of page titles with three words, add two instances of `\s[A-Z]+`: `^[A-Z]+\s[A-Z]+\s[A-Z]+\.\s\d+`
5. Flip these parts around to get rid of instances where page titles come after page numbers: `^\d+\s[A-Z]+\.`

{% include figure.html img="regex3.jpg" alt="regex remove page titles" caption="Use regular expressions to remove redundant page titles and numbers" width="100%" %}

**Remove hyphenated words at line breaks:**
1. In the search box, type: `-\s+[\r\n]`   
    - `-` finds the hyphen, `\s+` finds one or more whitespace characters, `[\r\n]` replaces these characters and gets rid of the line break 
2. Replace all instances

{% include figure.html img="regex2.jpg" alt="regex remove hyphens" caption="Use regular expressions to remove hyphenated words" width="100%" %}

The text still isn't 100% clean, but we've managed to take out most of the page titles and consolidate hyphenated words, so our future analysis won't be skewed.

{% endcapture %}
{% include alert.md text=text color=secondary %}

**More Regular Expression Resources:**
- [Regex exercises](https://regexone.com/)
- [Regex cheat sheet](https://www.rexegg.com/regex-quickstart.html)