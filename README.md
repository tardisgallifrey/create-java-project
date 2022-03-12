# Bash Script to create Java project

<p>I enjoy programming in Java, and wantd to create executable JAR files.  However, 
I was having the worst difficulty trying to get <code>jar</code> to work.  I did not wish to learn 
Maven or Gradle or any other IDE for Java.  I am completely comfortable with <code>javac</code>.<p>

<p>My solution came from the website <a href="https://dzone.com/articles/java-8-how-to-create-executable-fatjar-without-ide">Create an Executable Fat JAR On Your Command Line</a>.  
When I followed his instructions to the letter on building a correct Maven folder structure and resource files, <code>jar</code> 
finally worked.</p>

<p>I quickly realized that I could use <code>bash</code> to script out all the things I did and have a one step command to create new projects.  Took me an evening to get it going, but it works well and still produces a <code>*.jar</code> file.  In addition, as I use Visual Studio Code as my text editor/IDE, it recognizes the folder system as a valid Java Project.</p>

<p>Proper usage is to call the program with a project name on the command line:</p> 
<code>create-java-project mynewjavaprojectname</code>. 
<p>This project name becomes the top level folder and fills in the appropriate basic references in the script files.  These can be modified later, but this gets you started.  Failure to use an argument on the command line will fail the script with a message.</p>

<p>At the top level of the project there are two additional "bash" scripts: <code>javacompile</code> and <code>jar-it</code>. 
These two scripts perform the tasks of compiling your ".java" files into classes according to your package name and building 
the "jar" file from those classes. These are the most critical and extreme caution should be taken if you try to modify them.</p>

<h3>As always, you may use and/or modify this script as you wish, but there are no warranties of any kind.  Use at your own risk.</h3>