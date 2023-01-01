CSU Linux Visual Studio Code Guide
============

Most teachers here at CSU will recommend that you use some version of a client manager to set up you remote connection with CSU's remote linux server. While this option is completely fine and can be helpful to work with the software your professor is comfortable with, it does has it's drawbacks. The main issue I saw with using a client manager such as [MobaXTerm](https://mobaxterm.mobatek.net/download.html), [BitVise](https://www.bitvise.com/ssh-client-download), or [puTTY](https://www.putty.org) is that you are limited to the tools that are local to that server. For example, your Text Editors will stay [nano](https://www.nano-editor.org/docs.php) or [Vim](https://www.vim.org/docs.php) which for most Computer Science Students can be a pain to start on. Also, as you progress in your coursework and on to courses like CIS 345 you will ne to manage and view multiple files at once, which I found extremely hard to do with the default setup. 

This should be a comprehensive guide to help you set up Visual Studio Code as your Client Manager for any CSU Linux needs. If you have any questions please reach out to my contact information that is located both above and below. If this is helpful to you please consider giving my repo a :star: and sharing it! Cheers!

## Visual Studio Installation and Setup 

As we will be using VScode as our preferred way to log in spirit and grail the first thing we need to do is install it to our local machine. Please click [here](https://code.visualstudio.com/download) to be redirected to the VScode download page. From here select the correct download for the current operating system on your device (Windows, MacOS, or Linux). 

Assuming this is your first time using VScode consider taking the time to check our my other guide on my GitHub titled [Starting VScode Guide]() to help with learning how to use this widely verbose Text Editor! 

To make sure we are set up to connect to our remote server we will be using one extension to assist us with that process. To download our needed extension, either click [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) or open your extensions tab in VSCode and type "Remote - SSH" in. Proceed to download the extension to your machine! 

For the time being we are all ready for our next steps! 

## Setting Up SSH keys

Our next step will be setting up a public SSH key from our machine to CSU's server so we no longer need to log in using our password. This gives VSCode the ability to open up your session directly. 

For this step there are some differences based on the OS that you are running. Below I will have both MacOS and Windows detailed, as those are what I am familiar with. If you are running linux I assume that the commands used within our MacOS instruction will work as we are using very basic commands that they both share. 

### MacOS



2nd paragraph. *Italic*, **bold**, and `monospace`. Itemized lists
look like:

  * this one
  * that one
  * the other one

Note that --- not considering the asterisk --- the actual text
content starts at 4-columns in.

> Block quotes are
> written like so.
>
> They can span multiple paragraphs,
> if you like.

Use 3 dashes for an em-dash. Use 2 dashes for ranges (ex., "it's all
in chapters 12--14"). Three dots ... will be converted to an ellipsis.
Unicode is supported. ☺



An h2 header
------------

Here's a numbered list:

 1. first item
 2. second item
 3. third item

Note again how the actual text starts at 4 columns in (4 characters
from the left side). Here's a code sample:

    # Let me re-iterate ...
    for i in 1 .. 10 { do-something(i) }

As you probably guessed, indented 4 spaces. By the way, instead of
indenting the block, you can use delimited blocks, if you like:

~~~
define foobar() {
    print "Welcome to flavor country!";
}
~~~

(which makes copying & pasting easier). You can optionally mark the
delimited block for Pandoc to syntax highlight it:

~~~python
import time
# Quick, count to ten!
for i in range(10):
    # (but not *too* quick)
    time.sleep(0.5)
    print i
~~~



### An h3 header ###

Now a nested list:

 1. First, get these ingredients:

      * carrots
      * celery
      * lentils

 2. Boil some water.

 3. Dump everything in the pot and follow
    this algorithm:

        find wooden spoon
        uncover pot
        stir
        cover pot
        balance wooden spoon precariously on pot handle
        wait 10 minutes
        goto first step (or shut off burner when done)

    Do not bump wooden spoon or it will fall.

Notice again how text always lines up on 4-space indents (including
that last line which continues item 3 above).

Here's a link to [a website](http://foo.bar), to a [local
doc](local-doc.html), and to a [section heading in the current
doc](#an-h2-header). Here's a footnote [^1].

[^1]: Footnote text goes here.

Tables can look like this:

size  material      color
----  ------------  ------------
9     leather       brown
10    hemp canvas   natural
11    glass         transparent

Table: Shoes, their sizes, and what they're made of

(The above is the caption for the table.) Pandoc also supports
multi-line tables:

--------  -----------------------
keyword   text
--------  -----------------------
red       Sunsets, apples, and
          other red or reddish
          things.

green     Leaves, grass, frogs
          and other things it's
          not easy being.
--------  -----------------------

A horizontal rule follows.

***

Here's a definition list:

apples
  : Good for making applesauce.
oranges
  : Citrus!
tomatoes
  : There's no "e" in tomatoe.

Again, text is indented 4 spaces. (Put a blank line between each
term/definition pair to spread things out more.)

Here's a "line block":

| Line one
|   Line too
| Line tree

and images can be specified like so:

![example image](example-image.jpg "An exemplary image")

Inline math equations go in like so: $\omega = d\phi / dt$. Display
math should get its own line and be put in in double-dollarsigns:

$$I = \int \rho R^{2} dV$$

And note that you can backslash-escape any punctuation characters
which you wish to be displayed literally, ex.: \`foo\`, \*bar\*, etc.
