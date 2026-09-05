# Bicycle Store Service Analysis

A Power BI analytics solution tracking order fulfillment, sales performance, geographic distribution, and product metrics across a multi-year operational period.

---

## Key Metrics Summary

| Metric | Value |
| --- | --- |
| **Total Orders** | 23,603 |
| **Total Quantity Sold** | 85,866 |
| **Total Price** | $30.09M |
| **Total Freight** | $915.97K |
| **Total Tax** | $2.93M |
| **Total Sales** | $33.93M |

---

## Data Model (Star Schema)

The dashboard relies on a star schema centered on `BicycleStoreFACT` connected via one-to-many relationships to dimension tables:

* **Fact Table:** `BicycleStoreFACT` (`CustomerID`, `OrderQty`, `UnitPrice`, `LineTotal`, `TaxAmt`, `Freight`, `TotalDue`, `OnlineOrderFlag`, etc.)
* **Dimension Tables:**
* `StatusDIM` (`StatusID`, `Status`)
* `TerritoryDIM` (`TerritoryID`, `Territory`, `TerritoryGroup`)
* `ProductDIM` (`ProductID`, `Product`, `ProductCategory`, `ProductSubCategory`)
* `ShipMethodDIM` (`ShipMethodID`, `ShipMethod`)
* `OrderDateDIM` (`OrderDateID`, `OrderDate`, `OrderDay`, `OrderMonth`, `OrderYear`)
* `ShipDateDIM` (`ShipDateID`, `ShipDate`, `ShipDay`, `ShipMonth`, `ShipYear`)
* `DueDateDIM` (`DueDateID`, `DueDate`, `DueDay`, `DueMonth`, `DueYear`)



---

## Dashboard Pages

### 1. Orders View (`Orders.png`)

Provides volume-based metrics, fulfillment status tracking, and regional order distributions.

* **Order Status Breakdown:** Tracks volume across status types:
* Approved: 6,371
* In Process: 6,049
* Shipped: 5,691
* Cancelled: 2,647
* Rejected: 1,845
* Backordered: 1,000


* **Orders Per Year:** Peak order volume occurred in 2013 (11,877 orders), followed by 2012 (5,563), 2014 (5,239), and 2011 (924).
* **Orders Per Territory:** Canada leads with 8,010 orders, followed by Northwest (4,238), France (3,530), UK (3,520), Germany (1,903), Australia (1,713), Southwest (658), and Central (31).
* **Products Per Category:** Distribution across product types:
* Bikes: 9,141 (38.73%)
* Components: 7,434 (31.5%)
* Clothing: 4,933 (20.9%)
* Accessories: 2,095 (8.88%)



### 2. Sales View (`Sales.png`)

Focuses on revenue trends, regional performance, and territory financial metrics.

* **Sales Per Year:** Revenue peaked in 2013 ($16.04M), growing from 2011 ($2.00M) and 2012 ($8.67M), before reaching $7.22M in 2014.
* **Sales Per Region:** North America generates 58.42% ($19.83M), Europe accounts for 36.26% ($12.31M), and Pacific represents 5.31% ($1.8M).
* **Sales Per Territory:** Canada ($11.94M) and Northwest ($6.94M) represent top revenue territories.

---

## How to Use

1. **Clone the repository:**
```bash
git clone https://github.com/HamadaX98/Bicycle-Store-Service-Analysis.git

```


2. **Open in Power BI:** Launch `Bicycle Store Service Analysis.pbix` in Power BI Desktop.
3. **Navigate:** Use the left navigation panel to switch between **ORDERS** and **SALES** views.
