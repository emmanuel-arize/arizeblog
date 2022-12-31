---
layout: Excel-post
title: Excel IF Function
author: Emmanuel Arize
category: Excel

---
In this tutorial I will be illustrating how to use EXCEL IF function. The IF function is one of the most used functions in Excel which returns values based on a **true** or **false condition**.The condition here is referred to as logical_test and the function has the following syntax.

```
=IF(logical_test, [value_if_true], [value_if_false])
```

For example, =IF(A2=100,"High","Low") says IF(A2= 100, then return High, otherwise return Low).

Let now look at the worksheet below

<br>
<img class="w3-center" src="{{'assets/images/Excel/if1.jpg'|relative_url}}">
<br>
Using the preceding the figure above let now rate the sales amount as **high** if sales amount is equal or greater than 100 or low using if less than 100 using the if function.

Let name cell C1 AS **Sales Rating**,

<br>
<img class="w3-center" src="{{'assets/images/Excel/if2.jpg'|relative_url}}">
<br>

 1. Select the cell **C2**
 2. Type **=IF**
 3. Double click the IF command


 <br>
 <img class="w3-center" src="{{'assets/images/Excel/if3.jpg'|relative_url}}">
 <br>

 4. Specify the condition B2>=100
 5. Type ,
 6. Specify the value "High" for when the condition is TRUE
 7. Type ,
 8. Specify the value "Low" for when the condition is FALSE
 9. Type )
 10. Hit enter

 <br>
 <img class="w3-center" src="{{'assets/images/Excel/if4.jpg'|relative_url}}">
 <br>

Since the value in cell B2 is greater than 100, the condition is true so the function returns "High".

<br>
<img class="w3-center" src="{{'assets/images/Excel/if5.jpg'|relative_url}}">
<br>

Click on cell C2 and drag it down to populate the other cells as shown below,
<br>
<img class="w3-center" src="{{'assets/images/Excel/if6.jpg'|relative_url}}">
<br>


### Nested IF Function
Using the IF function it is also possible to use an IF statement as a TRUE or FALSE value inside another IF function and in this way you can test for more than one condition within one function and return more than two results. Let illustrate this with an example.

In this example we are rating the sales amount as **high** if THE amount is equal or greater than 150 and **Medium** if greater than or equal 100 but less than 150 and **low** otherwise using nested if function.

Let name cell D1 AS **Sales Rating 2** and in cell D2 type,

```
=IF( B2>=150, "High",
     IF(B2>=100,"Medium","Low")
    )
```
<br>
<img class="w3-center" src="{{'assets/images/Excel/if7.jpg'|relative_url}}">
<br>

Click on cell D2 and drag it down to populate the other cells as shown below,
<br>
<img class="w3-center" src="{{'assets/images/Excel/if8.jpg'|relative_url}}">
<br>
