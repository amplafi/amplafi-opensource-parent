#TestNG Guide#
For new eclipse users

##Before You Start##
Make sure that you have the [testng plugin installed on Eclipse](https://github.com/amplafi/amplafi-tools/blob/master/README.md).
The instructions are in the section marked **Install these Eclipse Plugins**. 

These rules apply to all of the amplafi projects when looking for tests.
1. Every project has its tests in a separate source folder called _test_.
2. The test source folder packages parallel the main code packages.

![Test class Structure within projects.](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/testngGeneral.png)

##Testing a Class##
One of the most useful reasons to run a test in eclipse is to use the eclipse 
debugger to find out why it does not pass. Running tests in the debugger is 
easy and takes only a few steps.

1. Open the test class file.
2. Turn on the brakepoints you want to use for this debug session.
3. On the menu choose run > debug as > TestNG test

![Running a testNG test from a class](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/testngDebugAs.png)

The debugger should suspend at the first enabled breakpoint it encounters. 
From here you can perform all of the familiar debugging actions.

##Testing an Entire Project#
To validate changes that you have made to a project all tests must complete 
without failure. To do this drop to your favorite command line tool and change 
your working directory to the project's directory and run:
<div>mvn test </div>
When the test completes there will be a summary of the test results  
![Summary](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/testngProject.png)

##Testing  All of the Opensource Projects for Amplafi##
The only difference between running the tests for a single project and all of 
the projects is the directory you start the command in. So to run the tests for 
all of the projects drop into your favorite command line tool and change your 
working directory to the amplafi-opensource-parent directory. Then run the same 
command as above (mvn test). If the tests are successful then you will be greeted 
with a screen similar to the one below.  
![Successfully ran tests for all projects using maven.](https://github.com/amplafi/amplafi-opensource-parent/raw/master/readme-images/testngAllProjects.png)

You can also run maven from eclipse with the [m2e plugin](http://www.eclipse.org/m2e/).

For more information on using testNG in the eclipse environment take a look at 
the [testNG Eclipse Guide](http://testng.org/doc/eclipse.html).