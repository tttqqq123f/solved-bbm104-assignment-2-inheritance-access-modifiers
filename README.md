Download Link: https://assignmentchef.com/product/solved-bbm104-assignment-2-inheritance-access-modifiers
<br>
Object-oriented programming has advantages such as modeling problems with less complexity and more code reuse. In this experiment, you will observe these advantages by using inheritance mechanism which is an important property of object-oriented programming. By the help of this experiment, you will learn the concept of inheritance, relationships among classes by using object references, control of multiple instances of classes, access modifiers in Java.

<h1>2           Useful Information</h1>

Under this section you will find some introductory information about the OOP concepts you might use in the project. Please make your own research for more information.

<h2>2.1         Inheritance</h2>

Object-oriented programming (OOP) covers software in terms similar to those that people use to describe real-world objects. It takes advantage of class relationships, where objects of a certain class, such as a class of vehicles, have the same characteristics cars, trucks, little red wagons and roller skates have much in common. Inheritance is one of important property of OOP. OOP takes advantage of inheritance relationships, where new classes of objects are derived by absorbing characteristics of existing classes and adding unique characteristics of their own. In Java, a class (called the derived class or subclass) extends from another class (called the base class or super class).

Figure 1: A hierarchy of Vehicle class

In Figure 1, vehicle class hierarchy is seen. Vehicle class is super class of all other classes. Derived classes which are Cars and Trucks have certain common properties; all have engine, wheels, horns etc. Thus they can be grouped under a Class called Vehicles. Apart from sharing these common features, each Derived Class has its own particular features – Cars use petrol while Trucks use diesel.

<strong>2.1.1        Method Overriding</strong>

When a class extend another class, the subclass can use the super class’ methods. However sometimes the subclass should change the behavior of a method which provided by super class. The method implementation in the subclass overrides (replaces) the implementation in the super class. The method in the subclass and its corresponding method in the super class method have the same name, parameters and the same return type. That is called method overriding.

<h2>2.2         Method Overloading</h2>

Method overloading is another important concept of OOP. When programmers need more than one method with the same functionality, they don’t have to declare new methods with different names for each one. By using method overloading feature, they declare each methods with same name but with different signatures (different argument list, argument types or orders). <em>System.out.println() </em>is an example of overloading method in Java. This method takes float, int, double or String as arguments.

<h2>2.3         Access Modifiers</h2>

In Java, there are three access modifiers which provide access levels for classes and members of classes: private (visible to the class only), protected (visible to the package and all subclasses) and public (visible to the everywhere). The default is visible to the package.

<h1>3           Experiment</h1>

This section contains four subsections. The first section introduces the problem that you need to solve and gives its details. In the second subsection, the content of reports are described. The constraints are given in the third subsection. Information about the submission is given in the last subsection.

<h2>3.1         Problem Definition</h2>

In this experiment, you are supposed to develop a simple Movie Database System similar to IMDB. You are responsible for using inheritance mechanism and access modifiers in Java programming language. The system will process several data input files and will generate results of commands which will be read from a command input file. All input files will be error free only syntactically. The requirements and rules for the system are given below:

<ul>

 <li>The system includes information about people and films.</li>

 <li>Each Person has name, surname, country and a unique id. A person in the system could be either Artist or User.</li>

 <li>Each User has a unique id, name, surname and country.</li>

 <li>There are three kinds of Artist: Performer, Director and Writer. Each Director has a unique id, name, surname, country and agent where he/she works. Each Writer has a unique id, name, surname, country and writing style/type.</li>

 <li>There are also three types of Performers which are Actor, ChildActor and StuntPerformer. Each Actor has a unique id, name, surname, country and height. Each ChildActor has a unique id, name, surname, country and age. Each StuntPerformer has a unique id, name, surname, country, height and real actors’ ids.</li>

 <li>There are four types of films in the system: Feature Film, Short Film, Documentary and TV Series. Each film (Feature Film, Short Film, Documentary and TV Series) has a rating score which calculated from users’ average rating scores for that film. A unique film id, film title, language, runtime, country, directors of a film and cast are common in all film types.</li>

 <li>Feature Films have a release date, budget, writers of movie and film genre in addition to the common data.</li>

 <li>A Short Film has a release date, writers and genre in addition to the common data. A Short Film’ runtime should be less ( or equal) than 40 min.</li>

 <li>Documentaries have only a release date in addition to the common film data.</li>

 <li>TV Series have start date and end date of series, number of seasons, number of episodes, genre of series and writers in addition to the common film data. A film may have more than one directors, writers, performers and genres in this system. A comma will be used to separate these data.</li>

</ul>

<strong>3.1.1         The Way of Execution</strong>

The program will be executed with four command line arguments:

&lt;people_file&gt;&lt;films_file&gt;&lt;commands_file&gt;&lt;output_file&gt;

Usage example:

<em>&gt;</em><strong>javac Main.java</strong>

<em>&gt;</em><strong>java Main people.txt films.txt commands.txt output.txt</strong>

There are three types of data input files and one output file. All the file names will be taken as program arguments. The format of each file is given below.

<strong>3.1.2       People File</strong>

There are six different recording samples in this file. These are:

DIRECTOR:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;NAME&gt;&lt;tab&gt;&lt;SURNAME&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;AGENT&gt;

WRITER:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;NAME&gt;&lt;tab&gt;&lt;SURNAME&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;TYPE&gt;

ACTOR:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;NAME&gt;&lt;tab&gt;&lt;SURNAME&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;HEIGHT&gt;

CHILDACTOR:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;NAME&gt;&lt;tab&gt;&lt;SURNAME&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;AGE&gt;

STUNTPERFORMER:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;NAME&gt;&lt;tab&gt;&lt;SURNAME&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;HEIGHT&gt;&lt;tab&gt;

&lt;ACTOR1ID,…,ACTORnID&gt;

USER:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;NAME&gt;&lt;tab&gt;&lt;SURNAME&gt;&lt;tab&gt;&lt;COUNTRY&gt;

An exemplar people file is shown in Figure 2. As shown in Figure 2, the person type is specified at the beginning of each line, and then attributes are given according to the person type, separated by tab characters.

<strong>3.1.3        Films File</strong>

Since there are four different film types in this system, there are also four different record samples in this file.

FeatureFilm:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;TITLE&gt;&lt;tab&gt;&lt;LANGUAGE&gt;&lt;tab&gt;&lt;DIRECTOR1ID,..,DIRECTORnID&gt;

&lt;tab&gt;&lt;LENGTH&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;PERFORMER1ID,..,PERFORMERnID&gt;&lt;tab&gt;&lt;GENRE1,…,

GENREn&gt;&lt;tab&gt;&lt;RELEASEDATE&gt;&lt;tab&gt;&lt;WRITER1ID,…,WRITERnID&gt;&lt;tab&gt;&lt;BUDGET&gt;

ShortFilm:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;TITLE&gt;&lt;tab&gt;&lt;LANGUAGE&gt;&lt;tab&gt;&lt;DIRECTOR1ID,…,DIRECTORnID&gt;

&lt;tab&gt;&lt;LENGTH&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;PERFORMER1ID,…,PERFORMERnID&gt;&lt;tab&gt;&lt;GENRE1,…,

GENREn&gt;&lt;tab&gt;&lt;RELEASEDATE&gt;&lt;tab&gt;&lt;WRITER1ID,…,WRITERnID&gt;

Documentary:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;TITLE&gt;&lt;tab&gt;&lt;LANGUAGE&gt;&lt;tab&gt;&lt;DIRECTOR1ID,…,&lt;DIRECTORnID&gt;

&lt;tab&gt;&lt;LENGTH&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;PERFORMER1ID,…,PERFORMERnID&gt;&lt;tab&gt;&lt;RELEASEDATE&gt;

TVSeries:&lt;tab&gt;&lt;ID&gt;&lt;tab&gt;&lt;TITLE&gt;&lt;tab&gt;&lt;LANGUAGE&gt;&lt;tab&gt;&lt;DIRECTOR1ID,…,DIRECTORnID&gt;

&lt;tab&gt;&lt;LENGTH&gt;&lt;tab&gt;&lt;COUNTRY&gt;&lt;tab&gt;&lt;PERFORMER1ID,…,PERFORMERnID&gt;&lt;tab&gt;&lt;GENRE1,…, GENREn&gt;&lt;tab&gt;&lt;WRITER1ID,…,WRITERnID&gt;&lt;tab&gt;&lt;STARTDATE&gt;&lt;tab&gt;&lt;ENDDATE&gt;&lt;tab&gt;&lt;SEASONS&gt;

&lt;tab&gt;&lt;EPISODES&gt;

An exemplar film file is given in Figure 3. In this file, the film type is specified at the beginning of each line, and then attributes are given according to the film type, separated by tab characters.

Figure 3: Sample films file

<strong>3.1.4        Commands File</strong>

All data input files (people and films) will be processed according to the commands which will be given in a commands file. The command file contains 12 types of commands whose definitions and formats are given below.

<ol>

 <li>A user can rate a film so that film will be saved to his/her rate list. Rating score must be between 1 and 10 integers.</li>

</ol>

<strong>RATE</strong><em>&lt;</em>tab<em>&gt;&lt;</em>USERID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>FILMID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>RATINGPOINT<em>&gt;</em>

<ol start="2">

 <li>It’s possible to add a new Feature Film to the system.</li>

</ol>

<strong>ADD</strong><em>&lt;</em>tab<em>&gt;</em><strong>FEATUREFILM</strong><em>&lt;</em>tab<em>&gt;&lt;</em>ID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>TITLE<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>LANGUAGE<em>&gt;&lt;</em>tab<em>&gt;</em>

<em>&lt;</em>DIRECTOR1ID,…, DIRECTORnID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>LENGTH<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>COUNTRY<em>&gt;&lt;</em>tab<em>&gt;</em>

<em>&lt;</em>PERFORMER1ID,…,PERFORMERnID<em>&gt; &lt;</em>tab<em>&gt;&lt;</em>GENRE1,…,GENREn<em>&gt;&lt;</em>tab<em>&gt;</em>

<em>&lt;</em>RELEASEDATE<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>WRITER1ID,…,WRITERnID<em>&gt;&lt;</em>tab<em>&gt; &lt;</em>BUDGET<em>&gt;</em>

<ol start="3">

 <li>Details of a film are displayed by using below command.</li>

</ol>

<strong>VIEWFILM</strong><em>&lt;</em>tab<em>&gt;&lt;</em>FILMID<em>&gt;</em>

<ol start="4">

 <li>A user can list all films which he/she rated so far.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>USER</strong><em>&lt;</em>tab<em>&gt;&lt;</em>USERID<em>&gt;&lt;</em>tab<em>&gt;</em><strong>RATES</strong>

<ol start="5">

 <li>A user can edit a film which he/she rated before.</li>

</ol>

<strong>EDIT</strong><em>&lt;</em>tab<em>&gt;</em><strong>RATE</strong><em>&lt;</em>tab<em>&gt;&lt;</em>USERID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>FILMID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>NEWRATINGPOINT<em>&gt;</em>

<ol start="6">

 <li>A user can remove one of his/her rated films.</li>

</ol>

<strong>REMOVE</strong><em>&lt;</em>tab<em>&gt;</em><strong>RATE</strong><em>&lt;</em>tab<em>&gt;&lt;</em>USERID<em>&gt;&lt;</em>tab<em>&gt;&lt;</em>FILMID<em>&gt;</em>

<ol start="7">

 <li>List all the TV Series in the system.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>FILM</strong><em>&lt;</em>tab<em>&gt;</em><strong>SERIES</strong>

<ol start="8">

 <li>List all the films from a specified country.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>FILMS</strong><em>&lt;</em>tab<em>&gt;</em><strong>BY</strong><em>&lt;</em>tab<em>&gt;</em><strong>COUNTRY</strong><em>&lt;</em>tab<em>&gt;&lt;</em>COUNTRY<em>&gt;</em>

<ol start="9">

 <li>List all the films released before a specified year.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>FEATUREFILMS</strong><em>&lt;</em>tab<em>&gt;</em><strong>BEFORE</strong><em>&lt;</em>tab<em>&gt;&lt;</em>YEAR<em>&gt;</em>

<ol start="10">

 <li>List all the films released after a specified year.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>FEATUREFILMS</strong><em>&lt;</em>tab<em>&gt;</em><strong>AFTER</strong><em>&lt;</em>tab<em>&gt;&lt;</em>YEAR<em>&gt;</em>

<ol start="11">

 <li>List all the films in descending order and categorized according to film rating degrees.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>FILMS</strong><em>&lt;</em>tab<em>&gt;</em><strong>BY</strong><em>&lt;</em>tab<em>&gt;</em><strong>RATE</strong><em>&lt;</em>tab<em>&gt;</em><strong>DEGREE</strong>

<ol start="12">

 <li>List all the artists from a specified country and display in a categorized order.</li>

</ol>

<strong>LIST</strong><em>&lt;</em>tab<em>&gt;</em><strong>ARTISTS</strong><em>&lt;</em>tab<em>&gt;</em><strong>FROM</strong><em>&lt;</em>tab<em>&gt;&lt;</em>COUNTRY<em>&gt;</em>

Figure 4: Sample commands file

<strong>3.1.5        Output File</strong>

The output of the commands will be printed to the specified output file. Each command’s output will include the command itself as read from the command file and the result (error message if necessary) of its execution. The general format of the output file is shown below:

&lt;COMMAND&gt;

&lt;NEWLINE&gt;

&lt;RESULT&gt;

&lt;NEWLINE&gt;

&lt;_______________________________________________&gt;

Detailed format of<em>&lt;</em>RESULT<em>&gt; </em>(mentioned above in the general format) output for each command type is given below (WS represents Whitespace).

<ol>

 <li><em>Film rated successfully</em></li>

</ol>

<em>Film type:&lt;WS&gt;&lt;FILMTYPE&gt; Film title:&lt;WS&gt;&lt;TITLE&gt;</em>

If there is not any user or film with specified ID the <em>&lt;</em>RESULT<em>&gt; </em>should be as follows:

<em>Command Failed</em>

<em>User ID:&lt;WS&gt;&lt;USERID&gt;</em>

<em>Film ID:&lt;WS&gt;&lt;FILMID&gt;</em>

If the specified film was already rated by the given user, then there should be a warning message as follows:

<em>This film was earlier rated</em>

<ol start="2">

 <li><em>FeatureFilm added successfully</em></li>

</ol>

<em>Film ID:&lt;WS&gt;&lt;FILMID&gt; Film title:&lt;WS&gt;&lt;TITLE&gt;</em>

If there is already a film with specified <em>&lt;</em>FILMID<em>&gt; </em>or if there is not any specified director, writer or performer in the system, the <em>&lt;</em>RESULT<em>&gt; </em>should be as follows:

<em>Command Failed</em>

<em>Film ID:&lt;WS&gt;&lt;FILMID&gt;</em>

<em>Film title:&lt;WS&gt;&lt;TITLE&gt;</em>

<ol start="3">

 <li>If specified film is Feature Film or Short Film the result will be as follows:</li>

</ol>

<em>&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;)</em>

<em>&lt;GENRE&gt;</em>

<em>Writers:&lt;WS&gt;&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>Directors:&lt;WS&gt;&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>Stars:&lt;WS&gt;&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

If specified film is Documentary; since a documentary doesn’t have writers and genre in the system, the result will be as follows:

<em>&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;)</em>

<em>Directors:&lt;WS&gt;&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>Stars:&lt;WS&gt;&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

If specified film is TV Series the result will be as follows:

<em>&lt;TITLE&gt;&lt;WS&gt;(&lt;STARTDATE&gt;-&lt;ENDDATE&gt;)</em>

<em>&lt;SEASONS&gt;&lt;WS&gt;seasons,&lt;WS&gt;&lt;EPISODES&gt;&lt;WS&gt;episodes</em>

<em>&lt;GENRE&gt;</em>

Writers:<em>&lt;</em>WS<em>&gt;&lt;</em>NAME<em>&gt;&lt;</em>WS<em>&gt;&lt;</em>SURNAME<em>&gt;</em>

<em>Directors:&lt;WS&gt;&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>Stars:&lt;WS&gt;¡NAME¿&lt;WS&gt;&lt;SURNAME&gt;</em>

<em>&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

If there is not any film with specified <em>&lt;</em>FILMID<em>&gt; </em>the <em>&lt;</em>RESULT<em>&gt; </em>should be as follows:

<em>Command Failed</em>

<em>Film ID:&lt;WS&gt;&lt;FILMID&gt;</em>

If there is not any rating votes for that film, then below warning message should be printed:

<em>Awaiting for votes</em>

<ol start="4">

 <li><em>&lt;</em>TITLE<em>&gt;</em>:<em>&lt;</em>WS<em>&gt; &lt;</em>RATINGSCORE<em>&gt;</em></li>

</ol>

If there is not any ratings of the specified user, then a warning message will be printed to the output file as follows:

<em>There is not any ratings so far</em>

If there is not any user with specified <em>&lt;</em>USERID<em>&gt; </em>the <em>&lt;</em>RESULT<em>&gt; </em>should be as follows:

<em>Command Failed</em>

<em>User ID:&lt;WS&gt;&lt;USERID&gt;</em>

<ol start="5">

 <li><em>New ratings done successfully</em></li>

</ol>

<em>Film title:&lt;WS&gt;&lt;TITLE&gt;</em>

<em>Your rating:&lt;WS&gt;&lt;NEWRATINGSCORE&gt;</em>

If there is not any user or film with specified IDs and if the user has no rating score for the specified film, then the <em>&lt;</em>RESULT<em>&gt; </em>should be as follows:

<em>Command Failed</em>

<em>User ID:&lt;WS&gt;&lt;USERID&gt; Film ID:&lt;WS&gt;&lt;FILMID&gt;</em>

<ol start="6">

 <li><em>Your film rating was removed successfully</em></li>

</ol>

<em>Film title:&lt;WS&gt;&lt;TITLE&gt;</em>

If there is not any user or film with specified IDs and if the user has no rating score for the specified film, then the <em>&lt;</em>RESULT<em>&gt; </em>should be as follows:

<em>Command Failed</em>

<em>User ID:&lt;WS&gt;&lt;USERID&gt; Film ID:&lt;WS&gt;&lt;FILMID&gt;</em>

<ol start="7">

 <li><em>&lt;TITLE&gt;&lt;WS&gt;(&lt;STARTDATE&gt;-&lt;ENDDATE&gt;)</em></li>

</ol>

<em>&lt;SEASONS&gt;&lt;WS&gt;seasons and&lt;WS&gt;&lt;EPISODES&gt;&lt;WS&gt;episodes</em>

If there is not any TV Series in the system, then a warning message will be printed to the output file as follows:

<em>No result</em>

<ol start="8">

 <li><em>Film title:&lt;WS&gt;&lt;TITLE&gt;</em></li>

</ol>

<em>&lt;LENGTH&gt;&lt;WS&gt;min</em>

<em>Language:&lt;WS&gt;&lt;LANGUAGE&gt;</em>

If there is not any film for the specified country in the system, then a warning message will be printed to the output file as follows:

<em>No result</em>

<ol start="9">

 <li><em>Film title:&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;)</em></li>

</ol>

<em>&lt;LENGTH&gt;&lt;WS&gt;min</em>

<em>Language:&lt;WS&gt;&lt;LANGUAGE&gt;</em>

If there is not any film released before the specified date in the system, then a warning message will be printed to the output file as follows:

<em>No result</em>

<ol start="10">

 <li><em>Film title:&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;)</em></li>

</ol>

<em>&lt;LENGTH&gt;&lt;WS&gt;min</em>

<em>Language:&lt;WS&gt;&lt;LANGUAGE&gt;</em>

If there is not any film released after specified date in the system, then a warning mes-sage will be printed to the output file as follows:

<em>No result</em>

<ol start="11">

 <li><em>FeatureFilm:</em></li>

</ol>

<em>&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;) Ratings:&lt;WS&gt;&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

<em>ShortFilm:</em>

<em>&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;) Ratings:&lt;WS&gt;&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

<em>Documentary:&lt;TITLE&gt;&lt;WS&gt;(&lt;RELEASEDATE&gt;) Ratings:&lt;WS&gt;&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

<em>TVSeries:</em>

<em>&lt;TITLE&gt;&lt;WS&gt;(&lt;STARTDATE&gt;-&lt;ENDDATE&gt;) Ratings:&lt;WS&gt;&lt;RATINGS&gt;/10 from&lt;VOTECOUNT&gt;users</em>

All the results should be printed in descending order.

If there is not any result for a category, then a warning message will be printed to the output file for that category as follows:

<em>No result</em>

<ol start="12">

 <li><em>Directors:</em></li>

</ol>

<em>&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;&lt;WS&gt;&lt;AGENT&gt;</em>

<em>Writers:</em>

<em>&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;&lt;WS&gt;&lt;TYPE&gt;</em>

<em>Actors:</em>

<em>&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;&lt;WS&gt;&lt;HEIGHT&gt;&lt;WS&gt;cm</em>

<em>ChildActors:</em>

<em>&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;&lt;WS&gt;&lt;AGE&gt;</em>

<em>StuntPerformers:</em>

<em>&lt;NAME&gt;&lt;WS&gt;&lt;SURNAME&gt;&lt;WS&gt;&lt;HEIGHT&gt;&lt;WS&gt;cm</em>

If there is not any result for a category, then a warning message will be printed to the output file for that category as follows:

<em>No result</em>

According to these definitions a sample output file is given in Figure 5 and Figure 6. This output file is not complete. The rest will be provided to you as sample input and output on the Piazza page. Further examples which give more details will be provided at the course’s Piazza page.

Figure 5: Sample output file part1

Figure 6: Sample output file part 2

<h2>3.2         Report</h2>

The structure of report is described below:

<ul>

 <li>Cover Page</li>

 <li>Class Diagram and Solution, describe details of your solution, stating its advantages and disadvantages technically. Draw class diagram. Show attributes and method names of each class in your diagram.</li>

 <li>Comments, give feedback about problem, problem description, and solution constraints. References, give the references you used throughout your work at the end of your report.</li>

</ul>

<h2>3.3         Constraints</h2>

<ol>

 <li>The methods’ and attributes’ names should be satisfied the most common naming conventions in Java.</li>

 <li>You should model entities of the system with classes.</li>

 <li>Your design will be graded. You are expected to propose a suitable design for the problem.</li>

 <li>You should use inheritance mechanism and correct access modifiers.</li>

 <li>All the input files and output file will be taken as command line arguments.</li>

</ol>