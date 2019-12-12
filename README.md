## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/mrashis/MySQL/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```sql
Syntax highlighted code block

select * from categories;
select distinct a.ProductName, b.CategoryName from products a, categories b WHERE a.CategoryID = b.CategoryID;
select count(distinct City) as allCities from customers;
select count(1) as City from customers;
select count(*) as City from customers;
select * from customers where City = 'London' AND CustomerID between 10 AND 70;
select * from customers where CustomerID not between 10 AND 70;
select * from customers where city between 'London' AND 'Madrid';
select * from orders where OrderDate between '1996-07-08' AND '1996-07-17';
select CustomerName, city from customers where CustomerID >= 10 AND CustomerID <= 70 AND CustomerID != 50 AND City like '%on';
select * from customers where City like '%on' AND NOT City = 'Lyon';
select * from customers where City like '%on' AND City != 'Lyon';
select * from customers where Country = 'UK' AND (City = 'London' OR City = 'Cowes');
select * from customers where Country not in ('UK', 'usa');
select * from customers where Country in (select Country from suppliers);
select * from customers order by Country desc, city asc;
select * from customers where Address is not null order by Country, city LIMIT 50;
select * from customers LIMIT 10,5;
select min(Price) as min, max(Price) as max, count(*) as total, sum(Price) as sum, round(avg(Price), 2) as avg from products;
select CustomerName, concat(Address,', ',City,', ',Country) as location from customers;
select b.ProductName, a.CategoryName from categories a inner join products b on b.CategoryID = a.CategoryID;
select customers.CustomerName, shippers.ShipperName, orders.OrderDate from ( (orders inner join customers on orders.CustomerID = customers.CustomerID) inner join shippers on orders.ShipperID = shippers.ShipperID );
select a.CustomerName, b.OrderDate from customers a left join orders b on a.CustomerID = b.CustomerID where b.OrderDate is not null;
select City, Country from customers where city = 'london' union all select City, Country from suppliers where Country = 'usa' order by city;
select City, Country from customers where city = 'london' union select City, Country from suppliers where Country = 'usa' order by city;
select Country, count(CustomerID) as totalCustomers from customers group by Country order by count(CustomerID) desc; 
select b.ShipperName, count(a.OrderID) as noOfOrders from orders a left join shippers b on a.ShipperID = b.ShipperID group by b.ShipperID;
select count(a.OrderID) as totalOrdersbyCountry, b.Country from (orders a INNER JOIN customers b ON a.CustomerID = b.CustomerID) where Country != 'USA' and Country != 'UK' group by Country having count(a.OrderID) > 10 order by Country;
select SupplierName from suppliers where exists (select products.ProductName from products where suppliers.SupplierID = products.SupplierID and products.Price < 20);
select products.ProductName from products where ProductID = any (select ProductID from order_details where Quantity >= 60);
select products.ProductName from products where ProductID = all (select ProductID from order_details where Quantity = 11);

```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mrashis/MySQL/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
