VERSION 1:



CUSTOMERS

has  all customer information -- also called customer dimension table -- contains all details related to a customer who has registered to the website

unique id

name

address

phone

age

gender

email



PRODUCTS

has a product's information -- also a dimension table

product id

name

description

price





CATEGORIES

not sure this is a pretty simple table that can be included in the product table itself or maybe it can be used when the inventory is huuuge

category id

name

description as well

(also a dimension table)



ORDERS --- fact table!!!!

order id

customer id

total amount? not sure about this one

order time



ORDER\_ITEMS ---- fact table

product id

category id in front of the product id (this is also redundant i feel)

quantity

customer id

order id

price of each item (kind of redundant since it is already present in product id)





PAYMENTS -- also a fact table

customer id

payment id

mode of txn

time of payment

discount

tax

gst or whatever idk

order id

payment status

billing address



SHIPMENTS --- fact table

shipment id

customer id

order id

payment id

shipping address





RETURNS  --- fact table

customer id

order id

payment id

shipping id

return address

refund amount



\---------------------------------------------------------------------------------------------------------------------



VERSION 2:



CUSTOMERS

\---------

customer\_id

first\_name

middle\_name

last\_name

address\_line\_1

address\_line\_2

address\_line\_3

city

state

pincode

country

phone

date\_of\_birth

gender

email

created\_at

updated\_at

status (active/inactive)





PRODUCTS

\--------

product\_id

product\_name

description

price

cost ( price is at what amount a product is sold and cost is at what it is bought by a business)

category\_id

brand

created\_at

updated\_at

status





CATEGORIES

\---------

category\_id

category\_name

description



ORDERS

\---------

order\_id

customer\_id

total\_amount

order\_datetime

order\_status (delivered/returned/not\_delivered)

created\_at

updated\_at



ORDER\_ITEMS

\---------

order\_item\_id  --- x number of product y --- keeping a singular line is better to handle returns re-orders 

order\_id

product\_id

quantity

unit\_price

discounnt\_amount

tax\_amount





PAYMENTS

\---------

payment\_id -- payment on our side

mode\_of\_txn (cash/online/card)

order\_id

payment\_amount

txn\_reference  -- used for identifying the payment on gateway side

payment\_datetime

payment\_status



SHIPMENTS

\---------

shipment\_id

order\_id

shipping\_address

carrier  -- who is delivering

tracking\_number

shipment\_status

shipped\_at

delivered\_at





RETURNS

\-------

return\_id

order\_item\_id

return\_reason

return\_status

return\_date

return\_address

refund\_amount



