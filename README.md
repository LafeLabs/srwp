# Self Replicating Web Page

## Replication instructions

1. Get a new web host set up by either getting free web hosting on [https://infinityfree.net/](https://infinityfree.net/) or [https://www.000webhost.com/](https://www.000webhost.com/) or buying  a domain and getting paid hosting on [https://www.dreamhost.com/](https://www.dreamhost.com/) (code proven to work on Dreamhost), or [setting up a Raspberry Pi with Apache and php](https://www.raspberrypi.org/documentation/remote-access/web-server/apache.md).  Buy domains with non standard extensions like ".xyz", and make them specific to a physical place like name-of-river-banks.xyz and finding unused domains for a couple dollars becomes trivial.  Or replicate down in the directory tree here by using [fork.html](fork.html)
2. Create a new file in the main Web directory of your new web page called replicator.php.  Open the file, and copy/paste the code from [the file php/replicator.txt on this server](php/replicator.txt), save it and close it.
3. Navigate a browser to [the web address of your new web server]/replicator.php, wait, and click on the link that appears.  You should now be at a new instance of this whole web page and seeing this document again.
4. To make the *next* instance of the page be a copy of the new instance instead of its ancestor, open the [code editor editor.php](editor.php), edit this document by editing README.md, change the format of the page by editing index.html, and to point the new replicator to the new page, edit replicator.php and change the url before "[data/dna.txt](data/dna.txt)" in the code to be your new domain name's global web address.  You can then repeat all steps in this list and the whole system will replicate and evolve without reference to any centralized code base.





