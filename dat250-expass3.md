<h1> Hand-in: short report, DAT250, LAB 3 </h1>


<h3> Technical problems </h3>

All my problems in this experiment came from verifying the integrity of the MongoDB packages.

The main issue was that when I copied SHA256 signature of the latest version of MongoDB Community Edition:


```
ed1cc2eee23f4fb9cc7f70867e29d7c9a1e1af1d9b4aa917d247a4921c4ffd7e  mongodb-windows-x86_64-5.0.3-signed.msi
```

I stored it as a txt file and not .sha256. This created the issue where this error message came instead of what I wanted:

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

![Bulk overwrite](assets/ex3/bulk_overwrite.png?raw=true)



<br>

<h3> Relevant results obtained during Experiment 2 </h3>

![map example 1](assets/ex3/mapEx.png?raw=true)

![map example 2](assets/ex3/mapEx2.png?raw=true)

<h4> My operation </h4>

I  map reduced the original table to a table that shows the quantity of each sold item, the price for each item, and in total how much the item has sold for. This is useful since we can now see clearly which item creates the most income.

![map my code](assets/ex3/terminal_ex3.png?raw=true)

![db_ex3](assets/ex3/db_ex3.png?raw=true)

***Code used to solv this task***

```js
// 1
var mapFunction3 = function() {
    for (var idx = 0; idx < this.items.length; idx++) {
       var key = this.items[idx].sku;
       var qty_price = { qty: this.items[idx].qty, price: this.items[idx].price };
       emit(key, qty_price);
    }
};

// 2
var reduceFunction3 = function(keySKU, countObjVals) {
    reducedVal = { qty: 0, price: 0 };
    for (var idx = 0; idx < countObjVals.length; idx++) {
        reducedVal.qty += countObjVals[idx].qty;
        reducedVal.price = countObjVals[idx].price;
    }
    return reducedVal;
 };

// 3

var finalizeFunction3 = function (key, reducedVal) {
    reducedVal.totalPrice = reducedVal.qty * reducedVal.price;
    return reducedVal;
  };


// 4
db.orders.mapReduce(
    mapFunction3,
    reduceFunction3,
    {
      out: { merge: "total_price_for_each_item" },
      query: { ord_date: { $gte: new Date("2020-03-01") } },
      finalize: finalizeFunction3
    }
  );

db.total_price_for_each_item.find().sort( { _id: 1 } )
```


---

<h3>  Pending issues with this assignment  </h3>

I have no pending issues that I am aware of.

