# JS-Dictionar

This is a dynamic dictionary created in JavaScript, it was initially created for the auxiliary language Sambahsa Mundialect _("dictionar" means "dictionary" in Sambahsa)_, but you can use this project for any other language. Here are the advantages of this software:
* It can be used online or offline _(everything is just in a single HTML file)_
* Searches are done in both ways, you don't need to create, for example, a Spanish-English dictionary and an English-Spanish one, just one version is enough
* It works well in small screens, like the ones of a mobile phone or tablet
* The software is very simple, so if you have a basic knowledge of web development, you can easily make your own customizations

Click [here](https://hmslima.github.io/JS-Dictionar/) to test this dictionary. _This project is part of a big one, that's why I provide only the English-Sambahsa dictionary, the versions in other languages are available in the main project._

# For those who want to use this software for their own dictionaries

You don't need to be a programmer to make your own dictionary by using my software, but a very basic knowledge of HTML and CSS would allow you to customize the dictionary.

1. Download the latest version of the English-Sambahsa dictionary in the [release page](https://github.com/hmslima/JS-Dictionar/releases).

2. Your dictionary must be in a text file. Each line of your dicionary must be in this format:

`the entry, a TAB space, the definition`

Let's see an example: 

    [...]
    bla bla bla	yada (talking)    
    blagh	bless ( vtr )    
    blaghmen	priest (who blesses; sb)    
    blaghmonium	priesthood (sb)    
    blah	blow (vtr )
    [...]

_Observe that the presence of normal spaces, punctuations and special characters are permitted, they don't affect the software, only TAB spaces._

3. The list of words lies inside a DIV called _"listOfWords"_. Just replace the existing list for yours
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

Yeah, the existing list is very big, the English-Sambahsa dictionary has more than 19,000 entries. That's why I suggest you to use a good text editor for making this replacement, I use [Geany](https://www.geany.org/), but other text editors are good too. By the way, be careful to not replace any part of the code. Let's see an example where you replace the Sambahsa-English dictionary for an English-Esperanto one. The result should be this:

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

5. At the beginning of the file, search for `<title>`, you will edit the title of the document, the one that appears on the tab of your browser, not in the page itself. Put the title of your dictionary between `<title>` and `</title>`. Be careful to not "eat" any part of the code, for example, a new title should be `<title>Esperanto-Angla Vortaro</title>`, not `<title>Esperanto-Angla Vortaro/title>`.

6. Now roll down until the bottom of the file, there you'll edit the content of the DIV `<div id="title">[...]</div>`, this title is the one that really appears in the page.

7. If you change the name of the file, you must search the line `<a href="index.html" download><input type="button" id="buttonDictionar" value="⬇"/></a>` and replace `index.html` for the new one. Let's say that now the name of the file is `vortaro_en.html`, then this line of code must be `<a href="vortaro_en.html" download><input type="button" id="buttonDictionar" value="⬇"/></a>`. The purpose of this line is to allow people to download the dictionary for offline use.

8. You can also change the language of the messages given by the software. Go to the beginning of the file and search for the line `if (lang == 0) { // Sambahsa`, there you'll see the available languages. Don't touch anything there unless you know what you doing, this part is only to see which is the number of each language. So, let's see that you are making a French-Volapük dictionary, maybe you'd like to let the interface in French, so let's say that the number of French is 3 (`else if (lang == 3) { // French`), then go to the bottom of the file and search for the line `<input type="button" id="buttonDictionar" value="»»" onclick="startSbSearch ('listOfWords', 'inputTextArea', 'result', 99);" />`, you only need to replace this `99` for `3` (`<input type="button" id="buttonDictionar" value="»»" onclick="startSbSearch ('listOfWords', 'inputTextArea', 'result', 3);" />`) in order to let the messages of the software in French.

9. Enjoy, if you have any question or found any technical problem, let me know in the [Issues Page](https://github.com/hmslima/JS-Dictionar/issues).
