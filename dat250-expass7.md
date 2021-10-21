<h1> Software Technology Experiment 7 report, DAT250 </h1>


<h3> Links to the different experiments </h3>

***Link to all the experiments***

https://github.com/andreasAabo/Software-Technology-Experiment-7


<br>

The code for each experminet can be found in the same folder:

```/src/main/java```

---

<h3> Technical problems </h3>

Most of the experiments went smoothly, though is had to do some trouble shooting when installing RabbitMQ. When i first installed the program i did not run the installtion files as an administrator, which caoused issues. This was resolved with resintallion RabbitMQ and Erlang as adminsitrator.

Furthermore the third experminet gave me some issues when doing the first testing of Worker and NewTask class. This was caused by the doWork method that throws InterruptedException. Error message:
```
java: unreported exception java.lang.InterruptedException; must be caught or declared to be thrown
```
Fixed the error message from the doWork method with implementing the try-catch version of doWork that was shown in the end of the Work Queues Tutorial.

Lastly I had some issues with getting alle the commands in the console to work. Some of this confusion was caused by the tutorial using ```$CP```, while Windows users need to use ```%CP%``` and some confusion came from not knowing where the .jar files where supposed to be placed and not knowing how set up a classpath. Most of these issues resolved them self after getting more experienced with the diffrent commands.

---

<h3>  Pending issues with this assignment  </h3>

I believe I managed to solve everything.
