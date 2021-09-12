<h1> Hand-in: short report, DAT250, LAB 2 </h1>

<h4> Link to code for experiments 1 and 2</h4>

github for experiments 1:

https://github.com/andreasAabo/Software-Technology-Experiment-1


<br>

github for experiments 2:

https://github.com/andreasAabo/Software-Technology-Experiment-2

---

<h3> Technical problems </h3>

In this experiment I had several problems.

The first problem I encountered was when I tried to import the project into IntelliJ. I knew that I would be using eclipselink, but hoped maven installed all the needed tools for me. I did not manage to get the project running as expected when launching it from IntelliJ. To resolve this, I ended up just importing the project into eclipse, where everything worked as expected from the start.

I also had problems with persisting entities into the database. This was caused by multiple issues. I had made a mistake with the many to many relationship in the Address class. I also thought it was possible to map ArrayList's to the database. Resolved the ArrayList issue with instead using List objects. 

It also took me some time to understand I needed to add the classes to the presitence.xml scheme. Resolved this by eventually adding the classes needed in the xml scheme.



---

<h3> How I inspected the database tables </h3>

To inspect the database tables, I use Adpache Derby. More precise after installing Apache Derby like the tutorial described, I can go into the bin folder ```C:\...\db-derby-10.15.2.0-bin\bin```, from my command line, and use the command 'ij'.

Then I need to connect to my database. the following command connects derby to the database:

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

<br>

***How can you check that the object links are saved correctly in the database?***

Ideally, I should probably have made some JUnit-tests, and made sure that the objects put into the database, also could be retrieved and maintained the correct relationship.

The manual way of making sure the links are correctly saved in the database, will be to look at the tables that I inspected above, and especially track the different foreign keys. For example, Max Musterman with id, 1, is connected to CreditCard, 3 and 4, which have the correct values in the table, that way I know that the relationship works as expected. This can be done with all the relationships.


---

<h3>  Pending issues with this assignment  </h3>

Not really a big issue, but I noticed 30 minutes before the deadline that the limit and balance values have been mixed up for the CreditCard table. This comes from me putting the arguments limit and balance in incorrect order in the function creatCreditCard in the EntityCreator class. So, when I inputted the values in Main class, line 41, I assumed they were in the order number, balance, limit. Not number, limit, balance. Choose not to change the tables since there was little time left and the mistake is quite small.

