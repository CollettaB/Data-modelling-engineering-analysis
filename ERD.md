card_holder as ch
----
id PK INT
name VARCHAR(255)

credit_card as cc
----
card PK VARCHAR(255)
cardholder_id INT FK >- ch.id

merchant
----
id PK INT
name VARCHAR(255)
id_merchant_category INT FK >- mc.id

merchant_category as mc
----
id PK INT
name VARCHAR(255)

transaction
----
transaction_id PK INT
date TIMESTAMP
amount FLOAT
card VARCHAR(255) FK >- cc.card
id_merchant INT FK >- merchant.id

![image](https://user-images.githubusercontent.com/79147539/148004337-423dbffd-7e75-4791-b542-e95fade96916.png)
