# JS-Dictionar

This is a dynamic dictionary created in JavaScript, it was initially created for the auxiliary language Sambahsa Mundialect, but you can use this project for any other language. Here are the advantages of this software:
* It can be used online or offline _(everything is just in one HTML file)_
* Searchs are done in both ways, you don't need create, for example, a Spanish-English dictionary and a English-Spanish one, just one version is enough
* It has a very permissive license, so you don't need to worry a lot with legal things
* The software is very simple, so if you have a basic knowledge of web development, you can make your onw customizations

Click [here](https://hmslima.github.io/JS-Dictionar/) to test this dictionary. _This project is part of a big one, that's why I provide only the English-Sambahsa dictionary, the versions in other languages are available in the main project._

# For those who want to use this dictionary, here is a small tutorial

You don't need to be a programmer to make your onw dictionary using my software, but a very basic knowledge of HTML and CSS would allow you to customize the dictionary.

1. Download the latest version of this dicionary in the [release page](https://github.com/hmslima/JS-Dictionar/releases).

2. Your dictionary must be in a text file. Each line of your dicionary must be in this format: the entry, a TAB space, the definition. Let's see an example
: 

.

    [...]
    bla bla bla	yada (talking)    
    blagh	bless ( vtr )    
    blaghmen	priest (who blesses; sb)    
    blaghmonium	priesthood (sb)    
    blah	blow (vtr )
    [...]

Maybe you cannot see the TAB spaces, but they are there. See the very same list from above, but with the TAB spaces replace by a →.

    [...]
    bla bla bla→yada (talking)    
    blagh→bless ( vtr )    
    blaghmen→priest (who blesses; sb)    
    blaghmonium→priesthood (sb)    
    blah→blow (vtr )
    [...]

_I am not sure if I was clear, but you cannot use the character "→" to separete the entries from the definitions, I only used it for didatic purposes. Also observe that the presence of normal spaces, punctuations and special characters are permitted, they don't affect the system, only TAB spaces._

3. The list of words lies inside a DIV called _"listOfWords"_. Just replace the existent list for your own list of words.
:

.

    <div id="listOfWords">
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    à la	à la 
    AAA dienchi	triple-A battery   
    ab	by (agent; can turn to “af” before “h”); ab- (verbal prefix) = away, off 
    aba	homespun (sb ) 
    abad	eternity ( sb) 
    
    [...]
      
    zwaujece	setback (sb) ( defeat ) 
    zwayako	suppository ( sf ) 
    zygote	zygote
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    </div>


The lines `<!--------------------------------- ----------------------------------->` are there to help you to find the limits of the list.

Yeah, the existent list is very big, the English-Sambahsa dictionary has more than 19,000 entries. That's why I suggest you to use a good text editor for making this replacement, I use [Geany](https://www.geany.org/), but other text editors are good too. By the way, be careful to not replace any part of the code. Let's see an example where you replace the Sambahsa-English dictionary for an English-Esperanto one. The result should be this:

    <div id="listOfWords">
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    A	indefinite article, not used in Esperanto
    Aback, to take	surprizi
    Abaft	posta parto
    Abandon	forlasi
    
    [...]
      
    Zoology	zoologio
    Zoophyte	zoofito
    Zouave	zuavo.
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    <!--------------------------------- ----------------------------------->
    </div>

4. If you've done everything that I said and saved the file, your dictionary is working, but the job is not done yet.

5. At the beginning of the file, search for `<title>`, we will edit the title of the document, the one that appears on the tab of your browser. Put the title of your dictionary between `<title>` and `</title>`. Be careful to not "eat" any part of the code, for example, a new title should be `<title>Esperanto-Angla Vortaro</title>`, not `<title>Esperanto-Angla Vortaro/title>`.

6. Now roll down until the bottom of the file, there you'll edit the content of the DIV `<div id="title">[...]</div>`, this title is the one that really appears in the page.

7. Enjoy, if you have any question, let me know in the [Issues Page](https://github.com/hmslima/JS-Dictionar/issues).
