<h1> Hand-in: short report, DAT250, LAB 3 </h1>


<h3> Technical problems </h3>

All my problems in this experiment came from veryfing the integrity of the MongoDB packages.

The main issue was that when I copied SHA256 signature of the latest version of MongoDB Community Edition:

```
ed1cc2eee23f4fb9cc7f70867e29d7c9a1e1af1d9b4aa917d247a4921c4ffd7e  mongodb-windows-x86_64-5.0.3-signed.msi
```

I stored it as a txt file and not .sha256. This created the issue where this error message came instead of what i wanted:

![Error Message](assets/ex3/error.png?raw=true)

I took me longer than I like to admit that to solve this issue. The solution was simply selecting ***all files*** (and not .txt) when saving the file, with the correct name.

<h4> veryfing the integrity of the MongoDB packages </h4>
![veryfing the integrity of the MongoDB packages](assets/ex3/sha256.png?raw=true)

---

<h3> Relevant results obtained during Experiment 1 </h3>

<h4> Insert Documents </h4>

![Insert Documents](assets/ex3/insert.png?raw=true)



<h4> Query Documents </h4>
![Query Documents](assets/ex3/query.png?raw=true)


<h4> Update Documents </h4>
![Update Documents](assets/ex3/update.png?raw=true)
![Update Documents 2](assets/ex3/update2.png?raw=true)


<h4> Delete Documents </h4>
![Delete Documents](assets/ex3/remove.png?raw=true)
![Delete Documents](assets/ex3/remove2.png?raw=true)



<h4> Bulk Write Operations </h4>
![Bulk Write Operations](assets/ex3/bulk.png?raw=true)
![Bulk overwrite](assets/ex3/bulk_overwrite.png?raw=true)



<br>

<h3> Relevant results obtained during Experiment 2 </h3>



---

<h3>  Pending issues with this assignment  </h3>

Not really a big issue, but I noticed 30 minutes before the deadline that the limit and balance values have been mixed up for the CreditCard table. This comes from me putting the arguments limit and balance in incorrect order in the function creatCreditCard in the EntityCreator class. So, when I inputted the values in Main class, line 41, I assumed they were in the order number, balance, limit. Not number, limit, balance. Choose not to change the tables since there was little time left and the mistake is quite small.

