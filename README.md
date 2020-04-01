# Self-replicating web pages


## Abstract

Self-replication has been an obsession in technology since Von Neumann contemplated such devices at the dawn of the information age.  I describe, with links to code on Github, how to create a self-replicating web page which can spread with just a few keystrokes to any web server connected to the Internet.  A single php script called replicator.php fetches all the files using a JSON file called dna.txt.  This system differs from a virus in that first of all it only propagates with consent of the user and second of all it copies a whole working system which can do useful things and does not just infect an existing host.   The newly replicated site can be edited in situ on the new host without any login credentials and then used as the source for the next instance, allowing it to evolve and grow in the “wild” of the Internet.

## Author: Lafe Spietz
## Spring 2020

## Introduction: viral vs. organic media

Viral media has become a part of our everyday lives, for better or worse. Both good ideas and bad ideas spread in ways which are a very strong analogy with biological viruses.  Viruses consist of information which can infect a host, causing that host to replicate the information.  It is controversial whether to call a virus an organism or not--they are simple code that hacks an existing life form and uses it to make copies. In the case of something like a conspiracy theory on Facebook, an infected host person posts a meme to their Facebook wall, other people see it, believe it, and decide to the post it to their wall, which Facebook displays in other users' feeds, and thus the information propagates both in the minds of the infected people and on the databases Facebook uses to keep track of such things.  

But how does the host reproduce?  If memes on social media are like viral information infecting a host, what is the nature of that host as a life-like object?  Just like a human or a tree, social media platforms have a reproductive life cycle.  They produce vast amounts of money, much of which finds its way back into venture investments which go into new startup companies.  These companies spend money on network infrastructure and labor to build new software, and attempt to grow themselves into large enough organisms that they too can become static hosts of viral information.  

What is presented here is another type of self-replicating information: social media which can replicate from one web host to another, without a company, without employees, without a centralized code base.  Code can be modified in situ on each web server that hosts the code, then when another server is seeded from that code it replicates that new instance.  Rather than discuss the theory of this in detail, I will dive in and take the reader through a full cycle of replication and evolution, then discuss the implications in the conclusion.  

The basis of self-replicating web code is the fact that a large fraction of web servers run php scripts by default.  The whole self-repicating web page instance can consist of a collection of files of all sorts of formats such as html, php, javascript, JSON, images etc., all of which are copied using a script called replicator.php.  Replicator points to a JSON file called dna.txt which lists all the files that are getting copied. Another php script called dnagenerator.php scans all the files and creates the dna.txt file as the files change.  All of the files can be edited on the server using editor.php.  Editor.php 

Laws of the Organic Web:

- no native code(php for interaction with server side filesystem, everything else runs in browser client side)
- no passwords or logins, any who can read data from any server can edit that data
- everything can be copied by anyone who can connect to it
- everything can be deleted by anyone on the network
- everything can be edited by anyone on the network
- no databases: files exist in a directory tree, and each branch in that tree can be replicated, forked or deleted at any time
- each instance of the code is totally self-contained: the next instance can be copied from that instance with no reference to any centralized code repository.
- editing is in situ on the server in a browser, not using code editing apps or IDE's
- there is no private property in the organic web as that would hamper replication




## Code Structure

### php scripts:

 - editor.php(note this uses the javascript library ace.js)
 - filesaver.php
 - fileloader.php
 - dnagenerator.php
 - mkdir.php
 - rdelete.php
 - text2php.php
 - replicator.php

### html pages:

 - index.html
 - fork.html
 - scroll.html
 - scrolleditor.html
 - calculator.html

### Other files:

 - README.md
 - dna.txt
 - dnasource.txt

## Replication Path

1. fork, then edit, then delete
2. replicate to local hard drive, edit on localhost, push to github, replicate your code from there
3. replicate onto free web host from your github
4. replicate onto paid commercial web hosting
5. replicate onto raspberry pi local server, set up for global access or not

## The Transformative Potential of the Organic Web

self-replicating documentation of self-replicating technology as a new economic system.  Value stored in the information of replication rather than in frozen value.  This can replace money in a society where value primarily replicates instead of being created linearly from mining and labor.

apps in the OW can include:

- math
- commerce
- culture
- community building
- art
- documentation of self-replicating technology


Building decentralized resilient networks on this model can be used to create networks of creation in societies targeted by violent networks.  Violent networks thrive in closed encrypted networks based on software like Telegram as well as centralized networks like Youtube and Twitter. Youtube's power comes from its monopoly(central control).  Telegrams power comes from its ability to hide(evade central control). A totally open network based on trust gets its resiliency from the constant upkeep as people delete bad information and replicate good information. 

A sketch of the mathematics of the Organic Web as it scales.  10 billion human minds.  100 billion devices with < 10 Gbytes.  100,000 documents per human mind. By contrast there are only about 6 million wikipedia articles total.  A sketch of how complex the system can be of replication from files to files, since each page can be replicating from each other page, simply to write down the state of *just* replicator directions requires the number of pages to the power of the number of pages.  This vastly exceeds the number of protons in the Universe.  But each node can do computation and save the output of that computation and have human operators then replicate both the product of the computation and the computation code itself to any other page.  Thus the sum total of the Network of human minds editing the code and replicating it around can vastly exceed the theoretical maximum of a Turing machine.  This system holds the possibility of computation which exceeds in power that of classical computers in much the way the quantum computer does.

Future work: find people to replicate, find reasons for them to do so.  Dreamers, organizers, hackers, coders, artists, leaders, writers, anyone who wants to win the hearts and minds of others...all these people can join this dream to create self-replicating media.


## Internal links

[scrolleditor.html(edit README file)](scrolleditor.html)

[scroll.html(view README file)](scroll.html)

[index.html(main page)](index.html)

[editor.php(code editor)](editor.php)

[../(link up a level from this page)](../)

[fork.html(create and delete pages below this one)](fork.html)

[data/dna.txt(list of files to replicate)](data/dna.txt)

[data/dnasource.txt(global web address of files to replicate)](data/dnasource.txt)

[replicator.php code](php/replicator.txt)

## External Links

[https://infinityfree.net/ free web hosting](https://infinityfree.net/)

[https://www.000webhost.com/ free web hosting](https://www.000webhost.com/)

[https://www.dreamhost.com/ paid hosting, cheap domain names](https://www.dreamhost.com/)

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

3. Decide what the purpose of your page is.  A page can be thought of as a generalized document which is a symbolic representation of an action, what is that action?  By default it's just replication of this page, but as with other generalized document preparation systems like the MS Office suit it can represent any action including learning and physical creation(instructions to make things).

4. Spread links to your page in a physical space: encode the url on some kind of physical media and give it out to people located in a geography that makes sense relative to the domain(streets and water).  The minimal example is an index with the url written on it, handed to people while saying "self replicating web page", or sitting in a place with a sign that says the same.

This system represents a generalized document which can replicate, spreading a generalized action.


## Evolution of System

- The simplest evolution of a page is just editing the README file or scroll to change what action the page is replicating
- The code editor can be used to edit the main page index.html to do *anything*: computation, communication, complex web based document creation, networking of all kinds
- The code editor can also be used to bootstrap the complexity of the system, using editor.php to add files to edit, editing the files, and hence adding arbitrary files in both client side javascript and php server side(never server side js). Also, the whole system can be cloned to the command line with php, edited, pushed to a github repo, then replicated from the raw code there.  All code can interact with local data in the data/ directory, which all other code on the Network can access
- Any node on the Network can take as its replication source any other node.  So if the Network has N nodes, the number of information flow configurations is N to the power of N. Any server can easily have 100's of nodes, and there can easily be multiple servers per person given existing scale of Internet-compatible hardware.  It is therefore conservative to estimate a minimum of 100 nodes per user. A network with 100 users thus has N of 10,000.  The size of the replication flow space is therefore on the order of 10,000 to the power of 10,000.  This is much larger than the estimated number of protons in the known universe, making it totally incomputable via classical computers.  If each node is carrying out computation using both client side and server side actions, and sharing with all other nodes in real time, all guided by the clicks of the users, who are interacting with multiple nodes simultaneously, the total computational power exceeds that of what is classically accessible in a way that is analogous to a quantum computer.
- Since the power of the Network comes from how closely users interact as well as the skill of the users in manipulating the machines, social structures must be formed which both recruit users and train them to become experts in control of these systems.  Specialization within these social structures will allow for the full range of activities required to make a functioning civilization with a minimal group of people(industrial fabrication, medicine, agriculture, water and waste treatment, shelter, communication).

## Laws of the Network

- EVERYTHING REPLICATES(every page contains replicator code to copy itself to anywhere else, to copy some other page it itself, and human instructions for copying the whole thing)
- EVERYTHING EVOLVES(any user on network can any file on any node)
- EVERYTHING DIES(any user can recursive-delete(rdelete.php) any page on any node on any server)
- EVERYTHING IS FRACTAL(any user can fork any page)
- EVERYTHING IS RECURSIVE(self-edit capability of all files including editors)
- NO MONEY(this network has no "security" and should never have any information exchange with the commercial Internet)
- NO PROPERTY(all information is replicated and deleted by default, there can be no "property" of any kind in such a network)
- NO PASSWORDS(the power of the network is derived from all users having access to all nodes at the same time, this is impossible without totally unrestricted access)
- NO LOGINS(see above)
- NO NAMES(An link to an individual can put that person at risk and should be avoided. You can't dox an egoless mind)
- NO IDENTITY(We do not replace names by pseudonyms, there truly is no identity)
- NO DATABASES(Databases are for private property and restrict the free open flow of information, we do not use them ever for any reason)
- NO CORPORATE STRUCTURE(corporations provide a target for lawsuits and regulation, in order for social structures of the Free Web to be robust they must be immune to such attacks and avoid all structures in the existing corporate legal order)
- NO EMPLOYEES(see above)
- NO FIXED CENTRALIZED DOMAIN NAMES(domain names are legal property.  We need them to start the network, but we deliberately choose them to be disposable, favoring .xyz domains and weird spellings to avoid conflict with the commercial Internet)
- NO COMMAND LINE INSTALLS ON SERVER(Servers are all treated as identical, running only simple php on the server side and saving data in human readable format, JSON by default)
- NO NATIVE APPS OR NATIVE CODE OF ANY KIND(native apps deliberately break the free flow of information and have to get past the gatekeepers of the computer industry(Apple, Microsoft, Google). We refuse to engage this system in any way other than using web browsers, and we avoid ever using Chrome for development to prevent Google from breaking the Open Web)
- ANY NODE CAN REPLICATE SOURCE FROM ANY OTHER NODE(Without the potential for totally free and instantaneous replication of code from any node to any other node we break the basic paradigm of the Free Web, and this must remain open without exception)
- FROM EACH ACCORDING TO THEIR DESIRE TO EACH ACCORDING TO THEIR DESIRE(we create things and replicate things based on an actual intention of some kind, not arbitrary rules created by a central authority.  In order for a thing to replicate, however, someone has to take positive action, requiring consent of the future replicators for a thing to replicate.  Desire is thus transmitted through the Free Network via Intent and Consent.)




