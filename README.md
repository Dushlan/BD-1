# BD-1
1) Выберите из таблицы orders все заказы
   
SELECT * FROM orders

![image](https://github.com/user-attachments/assets/cf106e88-c5b3-4647-b5e7-209f2e81ab6e)

2) Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in

SELECT * FROM orders WHERE STATUS IN('cancelled', 'in_progress', 'delivery') 

![image](https://github.com/user-attachments/assets/9934fc1e-e74d-406d-8a7d-de77b2fddbcb)

Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".

SELECT * FROM orders WHERE STATUS IN('cancelled', 'new') 

![image](https://github.com/user-attachments/assets/e8c6486c-fd79-4db8-aff1-ecaf88bffbd5)

Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count).
Вывести нужно только номер (id) и сумму (sum) заказа.

SELECT id, sum FROM orders WHERE products_count > 3;

![image](https://github.com/user-attachments/assets/906266e5-b8aa-4b9f-906b-2726be0de2b5)

1) Выберите из таблицы orders 3 самых дешевых заказа за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/12f5e71b-2f89-4f61-b995-deb5cfa40a7d)

SELECT * FROM orders WHERE STATUS != 'cancelled' ORDER BY sum ASC LIMIT 3

2) Выберите из таблицы orders 2 самых дорогих заказов за всё время.
Данные нужно отсортировать в порядке убывания цены.
Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/28beb440-e205-4cd9-8590-1af4974019c4)

SELECT * FROM orders WHERE STATUS != 'cancelled' ORDER BY SUM desc LIMIT 2

3) Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

   ![image](https://github.com/user-attachments/assets/98060558-228f-40af-96c8-743e70c3f4d1)

   INSERT INTO orders (id, products, sum) VALUES (6, 4, 8000)

4) Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.

![image](https://github.com/user-attachments/assets/193b7397-5905-4543-9cf7-7f0367b535e7)

INSERT INTO products (id,NAME,COUNT,price) VALUE (7, 'VR очки',2,70000)

5) В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

![image](https://github.com/user-attachments/assets/bd874452-8356-4239-8053-59dd284e8d6e)

UPDATE products SET NAME='PS5' WHERE NAME='IMAC'
