# Self Replicating Web Page

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




