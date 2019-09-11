# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

- SELECT p.productName, c.categoryName from [products] as p inner join categories as c on p.categoryId = c.categoryId

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

- SELECT o.orderid, s.shippername, o.orderdate FROM [Orders] as o inner join shippers as s on o.shipperid = s.shipperid where o.orderdate < '1997-01-09' order by o.orderdate desc

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

- SELECT od.orderid, p.productname, od.quantity FROM [OrderDetails] as od inner join products as p on od.productid = p.productid where orderid = 10251 order by p.productname

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

- SELECT o.orderId, c.customername as Customer, e.lastname as 'Employee (last)' FROM [Orders] as o inner join customers as c on o.customerid = c.customerid inner join employees as e on o.employeeid = e.employeeid

### (Stretch) Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

\*

### (Stretch) Display OrderID and a column called ItemCount that shows the total number of products placed on the order. Shows 196 records.

\*
