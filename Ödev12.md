1. Film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
```
SELECT COUNT(*) FROM film
where length > (SELECT AVG(length)  FROM film)
```

2. Film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
```
SELECT COUNT(*) FROM film
WHERE rental_rate = (SELECT MAX(rental_rate) FROM film)
```

3. Film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

```
SELECT * FROM film
WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) AND replacement_cost = (SELECT MIN(replacement_cost) FROM film)
```

4. Payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
```
SELECT customer.first_name, customer.last_name FROM customer
INNER JOIN payment on customer.customer_id = ANY
(SELECT customer_id FROM payment 
GROUP BY customer_id 
ORDER BY COUNT(payment.customer_id) DESC
LIMIT 3)
LIMIT 3
```


[Patika Dev Profilim](https://app.patika.dev/adamblue)

www.patika.dev
