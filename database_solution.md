## Level 1
select count(*) as total from customers where country = 'Germany';

---
## Level 2
select Country, count(CustomerID) as customerCount
from Customers
group by Country 
having count(CustomerID) >= 5 order by count(CustomerID) desc;

---
## Level 3

select Customers.CustomerName,
       COUNT(Orders.OrderID) as OrderCount,
       FORMAT(MIN(Orders.OrderDate), 'yyyy-mm-dd') AS FirstOrder,
       FORMAT(MAX(Orders.OrderDate), 'yyyy-mm-dd') AS LastOrder
from Customers
inner join Orders ON Customers.CustomerID = Orders.CustomerID
group by Customers.CustomerName
having COUNT(Orders.OrderID) >= 5
order by MAX(Orders.OrderDate) desc;
