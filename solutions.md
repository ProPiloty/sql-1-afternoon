#Table - person // Complete

1.
create table person(
    id serial primary key not null,
    name varchar(120) not null,
    age int not null,
    height_in_cm int,
    city varchar(120),
    favorite_color varchar(40)
);

2.
insert into person(favorite_color, city, height_in_cm, age, name)
values('color-value', 'city-value', 'height-value', 'age-value', 'name-value');

select *
from person;

3.
select *
from person
order by height_in_cm desc;

4.
select *
from person
order by height_in_cm asc;

5.
select *
from person
order by age desc;

6.
select *
from person
where age > '20';

7.
select *
from person
where age = '20';

8.
select *
from person
where age >= '20'
and age <= '50';

9.
select *
from person
where age not in (27);

10.
select *
from person
where favorite_color not in ('red');

11.
select *
from person
where favorite_color not in ('red', 'blue');

12.
select *
from person
where favorite_color in ('orange', 'green');

13.
select *
from person
where favorite_color in ('orange', 'green', 'blue');

14.
select *
from person
where favorite_color in ('yellow', 'purple');

#Table - orders

1.
create table orders(
	person_id serial primary key,
    product_name varchar(120),
    product_price int,
    quantity int
);

2.
insert into orders(person_id, product_name, product_price, quantity)
values('person-value', 'product-value', 'price-value', 'quantity-value');

3.
select *
from orders;

4.
select sum(quantity)
from orders;

5.
select product_price * quantity
from orders

6.
select product_price * quantity
from orders
where person_id = 'id-value';

#Table - artist

1.
insert into artist(name)
values ('name-value');

2.
select *
from artist
order by name desc
limit 10;

3.
select *
from artist
order by name
limit 5;

4.
select *
from artist
where name like 'Black%';

5.
select *
from artist
where name like '%Black%';

#Table - employee

1.
select first_name, last_name
from employee
where city in ('Calgary');

2.
select birth_date
from employee
order by birth_date asc
limit 1;

3.
select birth_date
from employee
order by birth_date desc
limit 1;

4.
select *
from employee
where reports_to in ('2');

5.
select count(*)
from employee
where city in ('Lethbridge');

#Table - invoice

1.
select count(*)
from invoice
where billing_country in ('USA');

2.
select *
from invoice
order by total desc
limit 1;

3.
select *
from invoice
order by total asc
limit 1;

4.
select *
from invoice
where total > 5;

5.
select count(*)
from invoice
where total < 5;

6.
select count(*)
from invoice
where billing_state in ('CA', 'TX', 'AZ');

7.
select avg(total)
from invoice;

8.
select sum(total)
from invoice;
