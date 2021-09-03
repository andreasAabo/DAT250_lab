<h1> Hand-in: short report, DAT250, LAB 1 </h1>

<h4> Link to the Heroku app</h4>
https://salty-forest-61050.herokuapp.com/ (Takes you to the main getting started page, from the Heroku java tutorial)


<br>

https://salty-forest-61050.herokuapp.com/hello  (Takes you to config vars example page, from the Heroku java tutorial)

<br>

https://salty-forest-61050.herokuapp.com/db (Takes you to database example page, from the Heroku java tutorial)


<h3> Technical problems </h3>
I did not have any problems during the installation of the software development environment. However, I made the assumption that Maven was already installed on my computer, since I have previously worked with Maven in IntelliJ. I Still checked that Maven was installed with the command, 
```mvn --version``` 
where the command mvn was not recognized, meaning Maven was not installed. Turns out IntelliJ has built in maven support. From there I installed Maven and added the right environment-variables (MAVEN_HOME and M2_HOME) and system path. This avoided any technical issues related to Maven when working with the Heroku platform.

---

<h3> Validated that the software development environment is working </h3>

To validate that software development environment is working I just ran these commands in the cmd:
```java --version```
To check which java version my system has installed

```mvn --version```
To check which Maven version my system has installed

```git --version```
To check which Git version my system has installed

If any of these commands gives the result "x command is not recognized", then x is not installed and added to environment or system variables.

With the technics discussed above I validated the following version are installed on my computer:

```
Java 16.0.2
Apache Maven 3.8.2
git version 2.25.1
```

As to validating that my IDE is working, I made sure that my IDE of choice, IntelliJ, was running the latest version (IntelliJ IDEA 2021.2.1). Made sure the license for students was still going. And made a small fizz-buzz java program to make sure everything worked as expected.


---

<h3> Technical problems encountered with the Heroku platform </h3>

The only issue I experienced, came from me not reading the tutorial well enough. I copy-pasted the code in "Use a database" section into Main.java, not realizing that the code shown in the tutorial already existing within Main.java. Resolved it by removing the code I added.

---

<h3>  Pending issues with this assignment  </h3>

I believe I managed to solve everything.


