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

<!-- TODO: add guide to change what tasks show up in the task view. -->
<!-- TODO: add guide to Format code !!!-->
<!-- TODO: add guide to quickly move between objects by their relationship to each other. -->
    <!-- TODO: add guide for using F3-->
    <!-- TODO: add guide for using F4-->
    <!-- TODO: add guide to build a callback tree for methods and objects.-->
    <!-- TODO: add guide to go back in editor switching Alt+LEFT-->
<!-- TODO: add guide to searching in files, the project, the workspace. Should also include info on searching for objects, and other types of items. -->
<!-- TODO: add guide to Refactor. -->
    <!-- TODO: add guide to rename a variable as an introduction to the refactor menu.-->
<!-- TODO: add guide to Debugging - this article covers debuggin well enough that most of these items do not need to be covered. http://www.vogella.de/articles/EclipseDebugging/article.html#advanced_class -->
    <!-- TODO: add guide to add breakpoints-->
        <!-- TODO: add guide to create an exception breakpoint. -->
        <!-- TODO: add guide to add a class load breakpoint. -->
        <!-- TODO: add guide to create a variable watchpoint. -->
        <!-- TODO: add guide to create a method breakpoint. -->
        <!-- TODO: add guide to create a line breakpoint. -->
            <!-- TODO: add guide to change the line breakpoint to only break when true or value changes. -->
<!-- TODO: add guide to step through code.-->
    <!-- TODO: add guide to F5 -->
    <!-- TODO: add guide to F6 -->
    <!-- TODO: add guide to F7 -->
    <!-- TODO: add guide to F8 -->
    <!-- TODO: add guide to Hover on variables for values.-->
    <!-- TODO: add guide to click on the stack trace to go to that line in code. -->
    <!-- TODO: add guide to look at variables-->
        <!-- TODO: add guide to add a detail formatter. -->
<!-- TODO: add guide to mylyn tasks -->
    <!-- TODO: add guide to Creating -->
    <!-- TODO: add guide to activating -->
    <!-- TODO: add guide to open a file and de-activate -->
    <!-- TODO: add guide to editors close...-->
    <!-- TODO: add guide to activate and all editors that were open when the task was de-activated will now be open once again. -->
<!-- TODO: add guide to perspectives? and views ?-->
<!-- TODO: add guide to general shortcuts to switch between views and editors Ctrl+F6 and Ctrl+F7 -->
