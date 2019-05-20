---
title: Prep
nav: true
---

# Prep

For this workshop you will need a web browser and a text editor. See instructions below for downloading one of the cross-platform text editors that we recommend.

{% capture text %}
When working with text files (txt, html, xml, markdown, etc.) you will need a good text editor.
Word processors such as MS Word can not be used to create or edit plain text.
Windows Notepad does not handle UTF-8 encoding or UNIX line endings that are standard for cross platform applications. 
For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, a more complete text editor will be helpful for larger projects.

Open source, cross-platform suggestions:

- [Visual Studio Code](https://code.visualstudio.com/){:target='_blank'}
    - Click the Cog icon in the lower left corner > *Settings* to configure view. Use the search box to find settings. If you prefer wrapped text, set "Word Wrap" to "on".
    - For spell check, click the square extension menu icon (left side), search for "Code Spell Checker" and click install.
- [Atom](https://atom.io/){:target='_blank'}
    - Click *File* > *Settings*, then *Editor* tab to configure view. If you prefer wrapped text, check "Show Indent Guide", "Soft Wrap", and "Soft Wrap Hanging Indent" `1`.
{% endcapture %}
{% include card.md text=text header="Text Editor" %}
