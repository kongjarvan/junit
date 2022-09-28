# Junit 학습 - 배포를 위해서!

### 1. 테이블 생성
```sql


create table product(
product_id int primary KEY auto_increment,
product_name varchar(20) NOT null,
product_price INT NOT null,
created_at TIMESTAMP NOT null
);


create table customer(
customer_id int primary KEY auto_increment,
username varchar(20) NOT null,
password varchar(20) NOT null,
created_at TIMESTAMP NOT null
);


create table orders(
order_id int primary KEY auto_increment,
customer_id INT NOT null,
product_id INT NOT NULL,
created_at TIMESTAMP NOT null
);


```


### 2. 더미데이터 생성

```sql


insert into customer(username, PASSWORD, created_at) VALUES('ssar', '1234', NOW());
insert into customer(username, PASSWORD, created_at) VALUES('cos','1234', NOW());
insert into product(product_name, product_price, product_qty, created_at) VALUES('바나나', 3000, 98, NOW());
insert into product(product_name, product_price, product_qty, created_at) VALUES('딸기', 3000, 100, NOW());
insert into orders(customer_id, product_id, created_at) VALUES(1, 1, NOW());
insert into orders(customer_id, product_id, created_at) VALUES(2, 1, NOW());


```