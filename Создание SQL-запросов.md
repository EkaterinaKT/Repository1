# Создание SQL-запросов на https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_in

### БД Products
1. В таблице Продукты (Products) выбраны все записи с ценой (Price) выше или равно 60 и отсортированы по столбцу Идентификатор поставщика  (SupplierID)
```
SELECT * FROM [Products]
WHERE Price >= 60
ORDER BY SupplierID;
```
![Products 1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Products_1.png)

2. В таблице Продукты (Products) выбраны столбцы  Название продукта (ProductName), Идентификатор поставщика  (SupplierID), Идентификатор категории (CategoryID), Цена (Price), затем полученная таблица отфильтрована, чтобы  Идентификатор поставщика и Идентификатор категории были равны 1 и отсортирована по Идентификатору поставщика  
```
SELECT ProductName, SupplierID, CategoryID, Price FROM [Products]
WHERE SupplierID = '1'
  AND CategoryID = '1'
GROUP BY ProductName;
```
![Products 2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Products_2.png)

3. В таблице Продукты (Products) выбраны столбцы  Название продукта (ProductName), Идентификатор поставщика  (SupplierID), Идентификатор категории (CategoryID), Цена (Price), затем полученная таблица отфильтрована, чтобы Идентификатор категории был равен 3, а цена больше 15 и отсортирована по Идентификатору поставщика  
```
SELECT ProductName, SupplierID, CategoryID, Price FROM [Products]
WHERE CategoryID = '3'
and Price > 15
ORDER BY SupplierID;
```
![Products 3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Products_3.png)
### БД Shippers
1. В таблице Грузоотправители (Shippers) выбраны записи исключая Имя отправителя (ShipperName) 'United Package', оставшиеся сгруппированы по Идентификатору отправителя (ShipperID)
```
SELECT * FROM [Shippers]
WHERE ShipperName NOT IN ('United Package')
GROUP BY ShipperID;
```
![Shippers 1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Shippers_1.png)
2. В таблице Грузоотправители (Shippers) записи сгруппированы по Имени отправителя (ShipperName)
```
SELECT * FROM [Shippers]
GROUP BY ShipperName;
```
![Shippers 2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Shippers_2.png)

3. В таблице Грузоотправители (Shippers) отобраны записи исключающие телефон (Phone) - (503) 555-9931 и Имя отправителя  (ShipperName) - Speedy Express
```
SELECT * FROM [Shippers]
WHERE Phone NOT IN ('(503) 555-9931')
and ShipperName NOT IN ('Speedy Express');
```
![Shippers 3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Shippers_3.png)

### БД Suppliers
1. В таблице Поставщики (Suppliers) выбраны записи без стран 'Germany', 'USA', 'UK', 'Japan', 'Italy', 'France' и отсортированы по городам (City)
```
SELECT * FROM [Suppliers]
WHERE Country NOT IN ('Germany', 'USA', 'UK', 'Japan', 'Italy', 'France')
ORDER BY City;
```
![Suppliers 1](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Suppliers_1.png)
2. В таблице Поставщики (Suppliers) выбраны записи по 'Germany' отсортированные по городам (City)
```
SELECT * FROM [Suppliers]
WHERE Country = 'Germany'
GROUP BY City;
```
![Suppliers 2](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Suppliers_2.png)
3. В таблице Поставщики (Suppliers) выбраны столбцы по странам (Country), городам (City), Имени контакта  (ContactName), Телефону (Phone) отсортированы по убыванию в столбце Страны и по возрастанию по столбцу Города
```
SELECT Country, City, ContactName, Phone FROM [Suppliers]
ORDER BY Country DESC, City
```
![Suppliers 3](https://repos.21-school.ru/students/MT10.ID_1261488/Team__TL__laquitar_student.21_school.ru_.M_J_GlsNRkmdbtKu5q_CRw/MT10-1/-/raw/pictures/src/Suppliers_3.png)








