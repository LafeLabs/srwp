# The Organic Web: Self-replicating Web Pages

## Internal Links:

[scrolleditor.html(edit README file)](scrolleditor.html)

[editor.php(code editor)](editor.php)

[../(link up a level from this page)](../)

[fork.html(create and delete pages below this one)](fork.html)

[data/dna.txt(list of files to replicate)](data/dna.txt)

[data/dnasource.txt(global web address of files to replicate)](data/dnasource.txt)

[replicator.php code(copy/paste this to replicate this page)](php/replicator.txt)

## files

### php scripts:

 - editor.php(in-browser editor which can edit all files. It uses the javascript library ace.js for syntax highlighting and the programs filesaver.php and fileloader.php to access the server side filesystem)
 - filesaver.php(save file to serverside file system)
 - fileloader.php(load file from serverside file system)
 - dnagenerator.php(read the directories to gather the files to produce dna.txt file)
 - mkdir.php(create a new directory on the server below the current one, and put a replicator.php script into it)
 - rdelete.php(recursively delete a directory, removing all files and sub directories as well)
 - text2php.php(php files are edited in raw text form, then are all copied to php using this script so that editor.php can edit itself without breaking itself)
 - replicator.php(The script that replicates the whole system)

### html pages:

 - index.html(by default this uses fileloader.php to fetch the README.md file, which it converts to html using the showdown.js javascript libary)
 - fork.html
 - scroll.html(just displays README.md, using JavaScript library showdown.js)
 - scrolleditor.html(text editor to edit README.md)
 - calculator.html(an example of a simple application: a web calculator)

### Other files:

 - README.md(this is the main text for the page, which can always be read with scroll.html if index.html is another app or document of some kind)
 - dna.txt(JSON file with list of all files for replicator.php to copy)
 - dnasource.txt(url of alternate page to copy from, can be copy/pasted from dna.txt link on any other page)

## Replication 

The most basic way to replicate, which I strongly encourage all readers to try is to go to the second link here at srwp.xyz and create a new instance as a subdirectory.  One does this by clicking on the link for fork.html, entering the name of the new page in the input, hitting enter, then clicking through the links to get to the new page(which will replicate using replictor.php).  Now edit the new page by clicking on the link to scrolleditor.html, edit the file, and click the link on the left side of the screen to get back to see your page.  You have now created a whole new instance of the software, with its own self-contained and self-editing code!  Now to complete the life cycle you can delete this by clicking on the link to go back up to the parent directory, then clicking again on the link to fork.html. You should now see your directory listed.  If you don’t, try reloading the browser a couple of times for the files to update.  Then click the button marked “DELETE MODE ON” and the word “DELETE” should appear next to your new page.  Click on that, and refresh the page a couple times and you’ll see it’s gone.  

All instances are replicated with a program called replicator.php, which uses a file called dna.txt to fetch all the files needed to run an instance.  These are a collection of html, javascript and php programs as well as some Geometron data which make up a copy of this whole webpage.  

The Github repository from all this is generated is:

[https://github.com/lafelabs/srwp/](https://github.com/lafelabs/srwp/)

To run the replicator, copy the code in [this file](https://raw.githubusercontent.com/LafeLabs/srwp/master/php/replicator.txt) or use the [local copy of the file here](php/replicator.txt) to a file called replicator.php in whatever directory on the server you want to copy srwp. Run that file by pointing your browser to [your server url]/replicator.php, then click on the link you see.  After that you can click on the "fork" icon and navigate down to "symbol/" and click on that replicator as well to replicate the Geometron symbol creation page.

To start a new web server get free web hosting at [infinityfree.net](https://infinityfree.net/) or [000webhost](https://www.000webhost.com/) or buy a domain and get paid hosting at a company like [dreamhost](https://www.dreamhost.com/), or get a [Raspberry Pi](https://www.raspberrypi.org/), install [Apache and php](https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md) on it and do the same copying of replicator.php.  Build a Raspberry Pi terminal with a screen, keyboard, mouse and power supply(this can be bought as a kit or built up from a pi motherboard and found components from other systems), put it on a local WiFi network, figure out the IP address of it, and link to that from local networks to make physically local Page only available on local wifi. 

To get to web directory, copy replicator.php, run it, change permissions, and get your local IP address use the following commands from the terminal:

    cd /var/www/html
    sudo rm index.html
    sudo curl -o replicator.php https://raw.githubusercontent.com/LafeLabs/srwp/master/php/replicator.txt
    php replicator.php
    sudo chmod -R 0777 *
    hostname -I

Once you have a IP address of a local server, put a link to that address on some global server so that without remembering the IP address or putting it in manually you can go to an existing server and just click to get to the local one.  If this is in a public place and you wish to share, you can then paint some physical thing with the address of the global page (www.yournewdomain.xyz), and edit the main top level scroll of that page to have the link to the local server be at the top, with some clear description or image(a picture of the physical server is not a bad idea).  

The longer term road map for the network is to install server clusters locally in every basement of every library, school, town hall, church, coffee shop and office park, locally owned by the people in that local community who get value from it.  Ultimately this can completely replace the centralized Internet, with physical hardware all controlled by the people who benefit from that network in the local physical world near those servers.

To create a new fork of the code, go to a UNIX command line with PHP installed, go into a new directory which is linked to a new github repository, copy replicator.php into that directory, run the program, then start php's built in web server as follows and type from the command line:


    curl -o replicator.php https://raw.githubusercontent.com/LafeLabs/srwp/master/php/replicator.txt
    php replicator.php
    php -S localhost:8000

and navigate your browser to localhost:8000, then edit using editor.php, change references in replicator.php to your new repo address, and replicate from the new fork by changing the code in replicator.php.  Note that php code needs to be made live by cliking on txt2php.php from editor.php.  This will work on macos or linux with very minimal effort, and requires adding the Ubuntu command line or installation of [MAMP](https://www.mamp.info/en/) to work on Windows 10.  

Edit the code for any page in the Art Factory using the *editor*, another thing all instances have:

[editor.php](editor.php)

When you have created your own modifications of the code, push that to your own Github repository and change the links in replicator.php to links to the global link to the raw text for your own dna.txt file and symbol/php/replicator.txt in your new repository and all future instances will be generated from your code instead of this instance.  Any php files you edit using editor must be converted from .txt to .php by running text2php.php by clicking on the link to that program from the Editor.  If you add new files, you can add them to dna.txt by clicking dnagenerator.php.  Note that *all* files in the system can be edited. 

To learn the skills needed to [hack](https://en.wikipedia.org/wiki/Hacker_culture) the code to your purposes, you need to learn JavaScript, HTML, and some PHP, all of which are best learned from [https://www.w3schools.com/](https://www.w3schools.com/).


## Principles of the Organic Web

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




