# Eclipse Tips Guide#

## Note on Eclipse Menus##
Eclipse menus (both the right-click menu and the menu at the top of the application) change all of
the time. They change when you have different views active, and they also change when you select 
different items within the view. For example the _Java..._ option under the _Search_ menu is not 
available when in a text editor, but is available when you are in the Java editor. Take care to 
look and re-look at the items in the menu every time you change selections, editors, views, or 
the general context in any way. This will help you to know what options are available for all of 
the views, editors, etc.

## Eclipse Help##
Eclipse comes with a very extensive guide to using eclipse please spend the time to read it. This 
guide can be accessed from the _help > Help Contents_ menu.  
![Accessing the Eclipse User guide](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseHelpMenu.png)  
When the help window is open on the left there is a tree of topics. To start with read the part 
titled _Workbench User Guide_ this guide talks about the general mechanisms of eclipse, such as 
perspectives and views. Once you have read that go on to read _Java development user guide_ this 
guide focuses on programming in Java with the Eclipse tool.  
![Read first](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseHelp.png)  

In addition to these great help files that introduce the new user to eclipse we also have tips and 
tricks sections for really pushing what you can do with the tool. You can access the tips and tricks 
directly through the help menu (_Help > Tips and Tricks..._).  
![Accessing the tips and tricks](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseTipsAndTricks.png)  
There will be another menu that pops up asking which category of tips and tricks you would like 
to view. Choose _Eclipse Java Development Tools_ (or explore if you like).  
![Choosing the tips and tricks category](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseTipsAndTricksChooser.png)  
The Eclipse tips and tricks are really compact so I will go through a few of them to get the new
user more familiar with a few of the _must know_ items.  

## Content Assist##
One of the most frequently used features of Eclipse is content assist. When typing content assist pops 
up on the side to make guesses at what you are typing, or to fill the roles of methods you are 
invoking. You can manually call content assist by pressing the Ctrl+SPACEBAR keys (Mac might be 
APPLE+SPACEBAR). This works wonders when you combine it with the camel case feature, I will show you.

Suppose you would like to create a variable for an InputStreamReader. It is not really a lot to type
but when all of the names for classes are this long it quickly becomes both a bother and time consuming.
Instead of typing the entire thing out lets type all of the capital letters _ISR_ and then hit the 
content assist shortcut (Ctrl+SPACEBAR).  
![Content assist at work](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseContentAssist.png)  	
Look at that! Eclipse suggests two classes based on those capital letters. What it suggests is a 
function of what is on your classpath and what is visible to the context of the code block you are 
writing in. Isn't this great?

## Warnings and Errors##
Another really useful tool in eclipse is the ability to customise the way Eclipse warns you about your 
code. Lets say that you really hate it when someone accesses a static member from an instance and you 
would like to get an error instead of a warning when this is found in code. Well you can change Eclipse 
to do that I will show you how.

1. Open the preferences menu (_Window > Preferences_).  
![preferences menu](https://github.com/amplafi/amplafi-tools/raw/master/readme-images/openPreferences.png)
2. Navigate to the errors/warnings section (_Java > Compiler > Errors/Warnings_).
3. Expand _Code Style_ if it is not already.
4. Change the option marked "Non-static access to static member" to say _Error_ instead of _Warning_.
5. Click OK and you are done, the workspace will update with your new preferences.
![errors/warnings](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseErrorsWarnings.png)

Did you notice all of those items marked _Ignore_? Perhaps there is something that Eclipse is not telling you.
Spend some time in this menu and really get to know what reporting options you have. It might be worth it to 
turn all of these items marked _Ignore_ to _Warning_ so you can see all of the options in action.

## Debugging with Eclipse##
There are already two great guide for this. Please read them.  
[Eclipse Help](http://help.eclipse.org/helios/index.jsp?topic=/org.eclipse.jdt.doc.user/gettingStarted/qs-13.htm)  
[Java Debugging with Eclipse - by Lars Vogel](http://www.vogella.de/articles/EclipseDebugging/article.html#advanced&#x005Fclass)

### Stepping Through Code###
While stepping through code there are some keyboard shortcuts.

* F5 Steps into code
* F6 Steps over code
* F7 Steps out of code (answers "oops, I stepped in how do I get out?")
* F8 Runs to the next breakpoint

### Viewing variables###
In the _Variables_ view, highlighting a variable will render it with the objects toString() method.
Sometimes this method overridden, or sometimes it doesn't display the information you would like. You
can create a new detail formatter to change how that type of object is rendered without changing code in
the program. Use the links below and read more on Detail formatters.  
[Great guide to detail formatters](http://eclipser-blog.blogspot.com/2007/10/tips-trick-for-debigging-in-eclipse.html)  
[Great detail formatter for Document Object Model (DOM) nodes](http://www.howardism.org/Technical/Eclipse/Eclipse_Detail_Formatter.html)

## Format Code Automatically##
Did you know that you can format code automatically? Yes, I will show you how it works 
(the reasons for using formatters are illustrated in 
[this article](http://www.semanticdesigns.com/Products/Formatters/)). 

First make sure that you are using the correct formatter for the project that you are working on 
(for Amplafi this is illustrated in the 
[README](https://github.com/amplafi/amplafi-tools/blob/master/README.md) 
for the [amplafi-tools](https://github.com/amplafi/amplafi-tools) project, look under the heading 
_Configure Eclipse_).

Look at the following code  
![Unclean formatting](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseCodeUnformatted.png)  
To format this code you can simply hit _Ctrl+SHIFT+F_, and this will format the entire document. 
If you prefer you can format just the offending code by selecting it first, and then using the 
above keyboard shortcut. After using the formatter the code now might look something like this.  
![Clean code](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseCodeFormatted.png)

### Format Code when Saving###
Eclipse also comes with the option to automatically format your code when you save a file. To do this 
open the preferences and go to _Java > Editor > Save Actions_ and change the options as follows.  
![Format on save](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseFormatCodeOnSave.png)

Notice That I chose to only format the lines edited. If you were to format all lines, then changes that 
you made on the commit will be unclear because nearly every line could have formatting changes. If it looks 
like another user is not formatting properly then get that user to fix the formatting (this way they will 
know there formatter is not set correctly).

Sometimes you still just want to fix the formatting yourself, 
if  you insist then don't waste your time with one file. You can right click on the project and format the 
entire thing at once.  
![Format a Project](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/eclipseFormatProject.png)

When you do this then make sure you have a clean project (no changes from last commit) and then commit 
right after formatting with no other changes. This will help others to know that the functionality of 
the code hasn't changed (it also helps if you put a clear message in for the commit like "Ran code 
formatter on the project.").  

## Walking in Code##
Walking or moving through code is not really a linear process. Methods are called, objects are created, 
and many other things occur that don't happen on the next line in the file. To help with this Eclipse 
has created a powerful set of tools to traverse code.

Note: For the next bit of examples, the context that Eclipse will use is the cursor position.

### F3 - Open Declaration###
Use F3 to go to the declaration of an item. For an instance variable this is where the type 
is defined. For a method this is where the method signature is defined (which is an interface 
in some cases) For a class this is where the class is defined. This is explained well in the 
[Eclipse Help](http://help.eclipse.org/galileo/topic/org.eclipse.jdt.doc.user/gettingStarted/qs-Navigate.htm)

### F4 - Open Type Hierarchy###
Use F4 to open the type hierarchy of an object. The type hierarchy tells you what the 
inheritance tree looks like as well as known subclasses (will not include objects not on the 
classpath). This is already explained very well on the [Eclipse Help](http://help.eclipse.org/galileo/topic/org.eclipse.jdt.doc.user/gettingStarted/qs-6.htm)

### Ctrl+Alt+H Call Hierarchy###
Use Ctrl+Alt+H to look at a list of all the other object and methods that use the method in 
question. This view is best explained in the [Eclipse Help](http://help.eclipse.org/galileo/topic/org.eclipse.cdt.doc.user/reference/cdt_u_call_hierarchy_view.htm)
(this guide was written for the C and C++ editors, but applies to Java as well).

### The Back Button (and Forward)###
Each time you use a traversal mechanism in Eclipse Where you were is saved (much like a 
web browsers history). By pressing _Alt+LEFT_ or _ALT+RIGHT_ you can traverse this history 
(also like the back and forward buttons in a web browser). So there is really know worry 
about loosing your place as you use these code traversal shortcuts.

As a side note _Ctrl+Q_ will take you to your last edit location and counts as a forward 
movement (doesn't clear your history but adds to it).

### Searching Code###
Sometimes while looking through code there is a need to search the project for keywords, 
objects and files. This [Eclipse Help](http://help.eclipse.org/galileo/topic/org.eclipse.jdt.doc.user/gettingStarted/qs-11.htm) 
has a great guide to using the search tool.

## Mylyn Tasks##
The Mylyn Task tool allows users to collect tasks from multiple sources and activate/update 
them from within eclipse. Read the [Mylyn guide](http://wiki.eclipse.org/Mylyn_User_Guide)
to understand how it works.

It also helps with workflow. Suppose you are working on an issue/bug and you attention is 
needed to do something else within the eclipse environment (like your boss walks in with a 
hot need to have something specific fixed). Argh! Close your currently opened views and 
editors to deal with this, then reopen them later. Mylyn saves this hassle by saving the 
state of your editors when you de-activate a task and bringing that state back when the 
task is reactivated.

Using [extensions](http://wiki.eclipse.org/Mylyn/Extensions) 
this tool can support any bug/issue tracking mechanism (and the one you use is likely 
already supported).

## Keyboard Shortcuts##
I have found a [wallpaper](http://www.hackergarten.net/wallpaper/EclipseCanoo1440x900.png)
that allows users to quickly view a lot of the most used, default eclipse shortcuts.

Some that I use most often are:

* Content Assist - Ctrl+SPACEBAR
   * Suggests context sensitive content completion
* Switching Views (Next View) - _Ctrl+F7_
   * Switches between Views such as Package Explorer, Editor, and Outline.
   * Previous View is _SHIFT+Ctrl+F7_
* Switching Editors (Next Editor) - _Ctrl+F6_ or _Ctrl+PAGE_UP_
   * Switches between Editors such as different Java files or XML files
   * Previous Editor is _SHIFT+Ctrl+F7_ or _Ctrl+PAGE_DOWN_
* Activate Editor - _F12_
   * Brings the Editor into focus
* Open Type - _SHIFT+Ctrl+T_
   * Opens a dialog to find a Java type and open it without the package editor (any type on the classpath).
* Open Resource - _SHFT+Ctrl+R_
   * Opens a dialog to find a file (within the workspace)
* Open Member - _Ctrl+O_ (that is the letter o not a zero)
   * Opens a dialog to find a member in the current editor
   * If you type _Ctrl+O_ again then it will expand to show inherited members as well
* Go To Line - _Ctrl+L_
   * Opens a dialog to move the cursor to a different line in the active editor

There are tons of shortcuts in Eclipse, browse the Internet to find out what other people are using.