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
