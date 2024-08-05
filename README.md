# howlcode
A simple command-line driven HTML+HTMX+AlpineJS Generator for various backends
Version 0.8

Please consider a donation: https://paypal.me/sabufrancis

Started: 27th July 2024
Last Update: Aug 5, 2024

Read this README file fully, please!
====================================

Website: https://howlcode.com Docs: https://docs.howlcode.com

The official repository is here https://github.com/square-foot/howlcode

What is it?
===========
HOWL = Hypermedia on Whatever You'd Like 
See https://htmx.org/essays/hypermedia-on-whatever-youd-like/ 

This nifty utiliy generates the initial files for HTML+HTMX+AlpineJS for 
many different back-ends, using simple "HOWL Generator Packages" 


Why was it written?
==================
I wanted one common springing point to rapidly create HTML+HTMX+AlpineJS 
based SaaS for various different back-ends. Also, I got tired of the nested 
tree structure of HTML -- and when you add attributes for HTMX and AlpineJS, 
you get lost in the forest of the HTML trees! (pun intended!)


What is a HOWL Generator Package?
=================================
One HOWL Generator package is written as a set of files, inside a specific sub-folder 
of "HowlGenerators". You can create such a package yourself. A few are on the 
Github respository made for such packages.

Read the docs at https://docs.howlcode.com 

Each such HOWL Generator Package will assist Howl Code to generate the required HTML and 
some skeletal server code for the routes that HTMX needs. 

There are no real limits on the kind of HOWL Generator Packages that can be written.
This system should cater to quite a lot of back-ends. I have written a few. 
I am sure eventually, the community will provide a lot more HOWL Generator Packages.

How to use Howl Code?
====================
This is a command-line program that works on Windows. It is 32 bit so should work on WINE 
based installations too. Run it from a Windows Console (cmd) without any arguments, and 
it should explain the arguments that you need to supply. Read the docs too (Link at top)

Can Plain HTML files be created?
================================
Yes. Just give the directive 'onlyhtml' (without the apostrophe, and on one line) 
in that Howl Generator Package's howl.cfg  Such a package should be available in this 
archive where you got this executable. Note that in this case you would need to 
manually create the back-end code; if your definitions have HTMX attributes. If you 
do not use HTMX attributes; then this can be an excellent static site generator. 

But I have a build-tool for my backend. How do I integrate Howl Code?
=====================================================================
You can write a batch file 'init.bat' in each Howl Generator Package. Do whatever 
you need to do with your build-tool from within that batch file. The batch file 
is given 2 arguments: The current build folder you gave using the -dirbuild argument 
and the name of folder of the Howl Generator Package are both sent to that batch file. 

What are the caveats?
=====================
This was written using Visual Prolog 5.2 -- an old compiler. It does NOT accept 
spaces inside pathnames. So please install this on a path that does NOT have spaces.
The working folder from where the program is executed is the place where it 
finds other directories you specify.

In the definition file, commas are sacred. It is used to identify various parts 
of the HTML element definition. Do NOT use commas within the strings themselves
as that would break the parser. This will be improved in the future.

Where is the source code?
=========================
As the code was written in Visual Prolog 5.2, open-sourcing this really cannot help 
anyone as that compiler does not exist anywhere anymore. But maybe, if there is 
enough demand and I get good feedback, I'll consider open sourcing this. 

I hope to get enough donations for this. If not; I may be forced to charge a good 
amount for a future and provide an improved version at some point in time. 
Early donors who donate more than $25 USD will get whatever version upto 
Dec 31, 2025 at no additional cost. The issues they submit would get priority.

The HTML Generator Packages required for this to work, are open-sourced though. 
See my repositories at https://github.com/square-foot

What is the license?
====================
See the file LICENSE.txt 
