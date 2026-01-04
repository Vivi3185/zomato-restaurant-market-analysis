# DAX Measures – Zomato Restaurant & Market Analysis

This document lists key DAX measures used in the Power BI report.

---

## 1. Total Restaurants
Counts total number of restaurants.

```DAX
Total Restaurants = 
COUNTROWS(zomato)
```

## 2. Overall Average Rating
Calculates average customer rating across all restaurants.


```DAX
Overall Average Rating = 
AVERAGE(Zomato[rate (out of 5)])
```

## 3. Online Order %
Percentage of restaurants offering online ordering.


```DAX
Online Order % = 
DIVIDE(
    CALCULATE(
        COUNTROWS(zomato),
        zomato[online_order] = "Yes"
    ),
    COUNTROWS(zomato)
)
```

## 4. Table Booking %
Percentage of restaurants offering table booking.


```DAX
Table Booking % = 
DIVIDE(
    CALCULATE(
        COUNTROWS(zomato),
        zomato[table booking] = "Yes"
    ),
    COUNTROWS(zomato)
)
```


## 5. Average Cost for Two
Average dining cost for two people.


```DAX
Average Cost for Two = 
AVERAGE(zomato[avg cost (two people)])
```

---

