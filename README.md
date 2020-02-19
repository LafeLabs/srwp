# Self Replicating Web Page

All code on this page can be edited in situ using the [code editor](editor.php).  The main page is index.html as is standard on the Web.  Index.html reads the markdown file [README.md](README.md) and uses the javascript library showdown.js to convert the [markdown](https://en.wikipedia.org/wiki/Markdown) to html and put it in a simple text format.  Two php scripts, [fileloader.php](php/fileloader.txt) and [filesaver.php](php/filesaver.txt), are used to save and load files on the server from the client side using javascript which accesses these programs with [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest), and these are what enable [editor.php](php/editor.txt) to edit all the files. Dnagenerator.php scans the files on the web page and saves them as a JSON file in [data/dna.txt](data/dna.txt).  All php scripts are stored in plain text in the php directory as php/*.txt so that they can be read from the open Web as well as edited without losing functionality while they are edited(enabling editor.php to edit php/editor.txt without breaking itself).  The php script text2php converts all the text files in php into php files in the main web directory which can then be run.  Replicator.php is a php script which references the global url for data/dna.txt and uses it to fetch all the individual files from a server anywhere on the open web, copying them to the local directory wherever the php script replicator.php exists. 

    programs:
        index.html
        README.md
        data/dna.txt
        dnagenerator.php
        editor.php
        fileloader.php
        filesaver.php
        text2php.php


To replicate this page, put copy the code at [php/replicator.txt](php/replicator.txt) into a file called replicator.php in the main web directory of a web server.  Then point a browser to [address of your web server]/replicator.php.


