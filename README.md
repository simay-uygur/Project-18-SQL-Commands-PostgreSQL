# Project-18-SQL-Commands-PostgreSQL
These are assignments given in Patika Java Intermediate course.


## Tasks

- Write an INNER JOIN query to view the city and country names from the city and country tables together.
- Write an INNER JOIN query to view the payment_id from the payment table along with the first_name and last_name from the customer table.
- Write an INNER JOIN query to view the rental_id from the rental table along with the first_name and last_name from the customer table.


## QUERIES

```
--- TASK 1
SELECT * FROM country 
INNER JOIN city ON city.country_id = country.country_id;

-- TASK 2
SELECT customer.first_name, customer.last_name, payment.payment_id FROM customer
INNER JOIN payment ON payment.customer_id = customer.customer_id;

__ TASK 3
SELECT customer.first_name, customer.last_name, rental.rental_id FROM rental
INNER JOIN customer ON rental.customer_id = customer.customer_id;
 
```

### THE TABLES

#### First Table
```
country_id |                country                |     last_update     | city_id |            city            | country_id |     last_update     
------------+---------------------------------------+---------------------+---------+----------------------------+------------+---------------------
         87 | Spain                                 | 2006-02-15 09:44:00 |       1 | A Corua (La Corua)         |         87 | 2006-02-15 09:45:25
         82 | Saudi Arabia                          | 2006-02-15 09:44:00 |       2 | Abha                       |         82 | 2006-02-15 09:45:25
        101 | United Arab Emirates                  | 2006-02-15 09:44:00 |       3 | Abu Dhabi                  |        101 | 2006-02-15 09:45:25
         60 | Mexico                                | 2006-02-15 09:44:00 |       4 | Acua                       |         60 | 2006-02-15 09:45:25
         97 | Turkey                                | 2006-02-15 09:44:00 |       5 | Adana                      |         97 | 2006-02-15 09:45:25
         31 | Ethiopia                              | 2006-02-15 09:44:00 |       6 | Addis Abeba                |         31 | 2006-02-15 09:45:25
        107 | Yemen                                 | 2006-02-15 09:44:00 |       7 | Aden                       |        107 | 2006-02-15 09:45:25
         44 | India                                 | 2006-02-15 09:44:00 |       8 | Adoni                      |         44 | 2006-02-15 09:45:25
         44 | India                                 | 2006-02-15 09:44:00 |       9 | Ahmadnagar                 |         44 | 2006-02-15 09:45:25
         50 | Japan                                 | 2006-02-15 09:44:00 |      10 | Akishima                   |         50 | 2006-02-15 09:45:25
        103 | United States                         | 2006-02-15 09:44:00 |      11 | Akron                      |        103 | 2006-02-15 09:45:25
        101 | United Arab Emirates                  | 2006-02-15 09:44:00 |      12 | al-Ayn                     |        101 | 2006-02-15 09:45:25
         82 | Saudi Arabia                          | 2006-02-15 09:44:00 |      13 | al-Hawiya                  |         82 | 2006-02-15 09:45:25
         11 | Bahrain                               | 2006-02-15 09:44:00 |      14 | al-Manama                  |         11 | 2006-02-15 09:45:25
         89 | Sudan                                 | 2006-02-15 09:44:00 |      15 | al-Qadarif                 |         89 | 2006-02-15 09:45:25
         82 | Saudi Arabia                          | 2006-02-15 09:44:00 |      16 | al-Qatif                   |         82 | 2006-02-15 09:45:25

```


#### Second Table 
```
 first_name  |  last_name   | payment_id 
-------------+--------------+------------
 Peter       | Menard       |      17503
 Peter       | Menard       |      17504
 Peter       | Menard       |      17505
 Peter       | Menard       |      17506
 Peter       | Menard       |      17507
 Peter       | Menard       |      17508
 Harold      | Martino      |      17509
 Harold      | Martino      |      17510
 Harold      | Martino      |      17511
 Douglas     | Graf         |      17512
 Douglas     | Graf         |      17513
 Douglas     | Graf         |      17514
 Douglas     | Graf         |      17515
 Douglas     | Graf         |      17516
 Douglas     | Graf         |      17517
 Douglas     | Graf         |      17518
 Henry       | Billingsley  |      17519
 Henry       | Billingsley  |      17520
 Henry       | Billingsley  |      17521
 Carl        | Artis        |      17522
 Carl        | Artis        |      17523
 Carl        | Artis        |      17524
 Carl        | Artis        |      17525
 Arthur      | Simpkins     |      17526
 Arthur      | Simpkins     |      17527
 Arthur      | Simpkins     |      17528
 Ryan        | Salisbury    |      17529
 Ryan        | Salisbury    |      17530
 Ryan        | Salisbury    |      17531
 Ryan        | Salisbury    |      17532
 Ryan        | Salisbury    |      17533
 Roger       | Quintanilla  |      17534
 Roger       | Quintanilla  |      17535
 Roger       | Quintanilla  |      17536

```

#### Third Table
```
 first_name  |  last_name   | rental_id 
-------------+--------------+-----------
 Tommy       | Collazo      |         2
 Manuel      | Murrell      |         3
 Andrew      | Purdy        |         4
 Delores     | Hansen       |         5
 Nelson      | Christenson  |         6
 Cassandra   | Walters      |         7
 Minnie      | Romero       |         8
 Ellen       | Simpson      |         9
 Danny       | Isom         |        10
 April       | Burns        |        11
 Deanna      | Byrd         |        12
 Raymond     | Mcwhorter    |        13
 Theodore    | Culp         |        14
 Ronald      | Weiner       |        15
 Steven      | Curley       |        16
 Isaac       | Oglesby      |        17
 Ruth        | Martinez     |        18
 Ronnie      | Ricketts     |        19
 Roberta     | Harper       |        20
 Craig       | Morrell      |        21
 Raul        | Fortier      |        22
 Barry       | Lovelace     |        23
 Juan        | Fraley       |        24
 Pamela      | Baker        |        25
 Billy       | Poulin       |        26
 Robert      | Baughman     |        27
 Constance   | Reid         |        28
 Marie       | Turner       |        29
 Ray         | Houle        |        30
 Fred        | Wheat        |        31
 Joy         | George       |        32
 Kay         | Caldwell     |        33
 Freddie     | Duggan       |        34
 Roberto     | Vu           |        35

```