<h1> Software Technology Experiment 7 report, DAT250 </h1>


<h3> Links to the experiments </h3>


https://github.com/andreasAabo/Software-Technology-Experiment-7


<br>

The code for each experiment can be found in the same folder:

```/src/main/java```

---

<h3> Technical problems </h3>

Most of the experiments went smoothly, though it had to do some troubleshooting when installing RabbitMQ. When I first installed the program I did not run the installation files as an administrator, which caused issues. This was resolved by reinstalling RabbitMQ and Erlang as an administrator.

Furthermore, the third experiment gave me some issues when doing the first testing of Worker and NewTask class. This was caused by the doWork method that throws InterruptedException. Error message:
```
java: unreported exception java.lang.InterruptedException; must be caught or declared to be thrown
```
Fixed the error message from the doWork method by implementing the try-catch version of doWork that was shown at the end of the Work Queues Tutorial.

Lastly, I had some issues with getting all the commands in the console to work. Some of this confusion was caused by the tutorial using ```$CP```, while Windows users need to use ```%CP%``` and some confusion came from not knowing where the .jar files were supposed to be placed and not knowing how to set up a classpath. Most of these issues resolved themself after I got more experienced with the different commands.

---

<h3>  Pending issues with this assignment  </h3>

I believe I managed to solve everything.
