<h1> Hand-in: short report, DAT250, LAB 2 </h1>

<h4> Link to code for experiments 1 and 2</h4>

github for experiments 1:

https://github.com/andreasAabo/Software-Technology-Experiment-1


<br>

github for experiments 2:

https://github.com/andreasAabo/Software-Technology-Experiment-2

---

<h3> Technical problems </h3>

In this experiment i had sevreal problems.

The first problem i encountered was when i tried to import the project into Intellij. I knew that would be using eclipselink, but hoped maven installed all the needed tools for me. I did not manage to get the project running as expected when launching it from Intellij. To resolve this I ended up just importing the project into eclipse, where everything worked as expected from the start.

I also had problems with presisting enteties into the database. This was caused by multiple issues. I had made a mistake with the many to many reltiohip in the Address class. I also thought it was possible to map ArrayList's to the database. Resolved the ArrayList issue with instead using List objects. 

It also took me some time to undestand i needed to add the classes to the presitence.xml scheme. Resolved this by eventually adding the classes needed in the xml scheme.



---

<h3> How I inspected the database tables </h3>

To inspect the database tables, I use Apache Derby. More prescise after installing Apache Derby like the tutorial descibed, I can go into the bin folder ```C:\...\db-derby-10.15.2.0-bin\bin```, from my command line, and use the command 'ij'.

Then i need to connect to my database. the following command connects derby to the database:

```connect 'jdbc:derby:C:\Users\andre\Skole\DAT250\DAT250_JPA\eclipselink\jpa-basic/db'; ```

From here I can inspect every table with simple SQL commands:


```SELECT * FROM PERSON;```

![Select Person](assets/ex2/selectPerson.png?raw=true)


```SELECT * FROM ADDRESS;```

![Select Address](assets/ex2/selectAddress.png?raw=true)


```SELECT * FROM CREDITCARD;```

![Select CreditCard](assets/ex2/selectCreditCard.png?raw=true)


```SELECT * FROM BANK;```

![Select Bank](assets/ex2/selectBank.png?raw=true)


```SELECT * FROM PINCODE;```

![Select Pincode](assets/ex2/selectPincode.png?raw=true)


```SELECT * FROM JND_PER_ADR;``` and
```SELECT * FROM JND_ADR_PER;```

![Select Joined table Person address](assets/ex2/manyToMany_per_adr.png?raw=true)



```SELECT * FROM JND_PERSON_CARD;```

![Select Joined table person card](assets/ex2/JND_PER_CARD.png?raw=true)


```SELECT * FROM JND_BANK_CARD;```

![Select joined table bank card](assets/ex2/JND_BANK_CARD.png?raw=true)


```SHOW TABLES;```

![SHOW TABLE](assets/ex2/showtables.png?raw=true)

---

<h3>  Pending issues with this assignment  </h3>

I believe I managed to solve everything.


