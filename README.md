# Self Replicating Web Page

## Internal links

- [scrolleditor.html](scrolleditor.html)
- [editor.php](editor.php)
- [../](../)
- [fork.html](fork.html)
- [data/dna.txt](data/dna.txt)
- [data/dnasource.txt](data/dnasource.txt)
- [replicator.php code](php/replicator.txt)

## External Links

- [https://infinityfree.net/ free web hosting](https://infinityfree.net/)
- [https://www.000webhost.com/ free web hosting](https://www.000webhost.com/)
- [https://www.dreamhost.com/ paid hosting, cheap domain names](https://www.dreamhost.com/)

## Code Structure(from dna.txt)

    {
    "html": [
        "README.md",
        "fork.html",
        "index.html",
        "scroll.html",
        "scrolleditor.html"
    ],
    "data": [
        "dna.txt",
        "dnasource.txt"
    ],
    "php": [
        "dir.txt",
        "dnagenerator.txt",
        "editor.txt",
        "fileloader.txt",
        "filesaver.txt",
        "mkdir.txt",
        "rdelete.txt",
        "replicator.txt",
        "text2php.txt"
    ]
    }

## Replication Path

1. Create a page on this server, below this page by clicking on the link to [fork.html](fork.html), entering the name of the new page and clicking through the links, edit that page with [scrolleditor.html](scrolleditor.html), making some trival change, then click the button on the left side to get back to the main screen.  To delete, go up a level with the link to [../](../), go back to [fork.html](fork.html), click the button to turn "delete mode" on, then click the delete button on the newly create page. You have now created a page, edited it, and deleted it.  

2. Get a new web hosting account on either a free or paid hosting service above.  All domain names should be linked to physical places, based either on the local watershed geography or local street geography, with a non-commercial ending like .xyz or .net or .org rather than .com.  On the new web hosting account you have set up, create a new file in the main web directory called replicator.php, open that file in the text editor on the server and copy the [code found here](php/replicator.txt) onto it.  Point a web browser to the web address of your new page, followed by /replicator.php, then click on the link that appears to go to your new page, and grow the page using step 1.

3. Decide what the purpose of your page is.  A page can be thought of as a generalized document which is a symbolic representation of an action, what is that action?  By default it's just replication of this page, but as with other generalized document preparation systems like the MS Office suit



Get a new web host set up by either getting free web hosting on [https://infinityfree.net/](https://infinityfree.net/) or [https://www.000webhost.com/](https://www.000webhost.com/) or buying  a domain and getting paid hosting on [https://www.dreamhost.com/](https://www.dreamhost.com/) (code proven to work on Dreamhost), or [setting up a Raspberry Pi with Apache and php](https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md).  Buy domains with non standard extensions like ".xyz", and make them specific to a physical place like name-of-river-banks.xyz and finding unused domains for a couple dollars becomes trivial.  Or replicate down in the directory tree here by using [fork.html](fork.html), entering the name of a new page, and clicking through to the replicator.  If you're adding a sub-page to this, you can back up to the previous level with [this link to ../](../).
2. Create a new file in the main Web directory of your new web page called replicator.php.  Open the file, and copy/paste the code from [the file php/replicator.txt on this server](php/replicator.txt), save it and close it.
3. Navigate a browser to [the web address of your new web server]/replicator.php, wait, and click on the link that appears.  You should now be at a new instance of this whole web page and seeing this document again.
4. To make the *next* instance of the page be a copy of the new instance instead of its ancestor, open the [code editor editor.php](editor.php), edit this document by editing README.md, change the format of the page by editing index.html, and to point the new replicator to the new page, edit [data/dnasource.txt](data/dnasource.txt), which replicator.php uses to locate the global code, to be your new domain name's global web address. TO get the global url of the dna at *this* web page instance and paste it into dnasource.txt on another server, get it from [this local link to this pages data/dna.txt file](data/dna.txt) You can then repeat all steps in this list and the whole system will replicate and evolve without reference to any centralized code base.





