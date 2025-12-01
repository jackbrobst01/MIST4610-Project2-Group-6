# MIST4610-Project2-Group-6

## Team Members:
1. Jack Brobst jdb54521@uga.edu @jackbrobst01
2. Zeb Stone zgs18605@uga.edu
3. Wade Pirkl wjp82580@uga.edu
4. Bradley Gabriel btg02951@uga.edu

## Scenario Description:

The task for our project is to design and build a database for an online retail company. The main focus of the database is the Customer entity, who can browse products, add products to their cart, and purchase the items. Some of the other entities consist of Product, Cart, Order, Payment, Shipper, and Address, which all work together to help track the shopping process. The goal was to design this model in a way that represents how an e-commerce store would work in real life. After creating the model, we populated it with data to represent business activity and then made 5 complex SQL queries to answer questions with the data that real managers would find helpful.

## Data Model:

Our model is based on an online retailer that sells products through an e-commerce platform. Customer, the main entity, stores information about each person who visits our online shop. Each customer can store multiple addresses for their shipping/billing accounts, but addresses cna only be linked to one customer (one to many). Each customer can also have one cart to store what they are shopping for and keep products in the cart while browsing. This is represented by the one-to-one between Cart and Customer.

Cart_Item serves as a bridge between Cart and Product, allowing a cart to hold many products and keep track of how many products are in each cart. Once a customer confirms their purchase, a record is kept in the Order Entity. Each order is linked to the customer who made it. An order can have many products, which is represented by the Order_item table and forms a many-to-many relationship between the two.

Payment is connected to Order through a one to one relationship representing how each order only has one payment and visa versa. The Shipper entity is also connected to Order through a one to one and stores information about the name and how the item was shipped (ground, air, 2-day, etc). Since one shipper can handle many orders, there is a one-to-many relationship between Shipper and Order.

The Product table stores basic product details such as name and price and is linked to the Category table, which groups products into logical sections such as “Electronics” or “Home.” It is connected to the Category entity through a one to many because a product can only be associated with one category, but categories can have many products. Category has a recursive relationship with itself because certain categories can have subcategories.

Review allows customers to leave feedback on a certain product and holds a one to many relationships from Customer and Product. Coupon allows customers to use discounts when purchasing, so there is a one to many relationship with Order. Inventory tracks the amount or quantity of a certain product we have in stock, forming a one to one relationship with Product. 

Return holds information about which items have been returned, such as reason, stautus, and the amount of the refund. It connects to order through a one to many because a single order may have one or many returns if a customer returns one item at a time for multiple returns. Supplier stores data about the vendors who deliver our products creating a one to many relationship wth Product. 

Overall, the data model represents the main functions and systems of an online shopping center, including browsing items, adding products to a cart, purchasing, and shipping, all while storing information about the customer, like a real-world situation.

<img width="1261" height="1002" alt="MIST Project 2 data model" src="https://github.com/user-attachments/assets/f97eab12-f7c4-499b-99de-623aa54d46d1" />


## Data Dictionary:
<img width="1147" height="643" alt="image" src="https://github.com/user-attachments/assets/6037ad49-3c62-4900-93e9-20153086a84b" />
<img width="1152" height="826" alt="image" src="https://github.com/user-attachments/assets/e8a3dcfc-5684-44b1-80c4-d07ca4c32d10" />
<img width="1153" height="885" alt="image" src="https://github.com/user-attachments/assets/a7ed8374-16e3-4aa9-9564-4f2fd939025b" />
<img width="1148" height="1179" alt="image" src="https://github.com/user-attachments/assets/663e7989-b801-455c-8cf3-c36ac893527f" />
<img width="1165" height="738" alt="image" src="https://github.com/user-attachments/assets/e44b042c-048f-4497-b8ff-44410bb4e09e" />
<img width="1151" height="1044" alt="image" src="https://github.com/user-attachments/assets/28683260-3bcc-425f-ba30-5dc1d6f7507f" />
<img width="1145" height="1246" alt="image" src="https://github.com/user-attachments/assets/4e08c584-1247-48a7-926f-f509e5c831a4" />
<img width="1149" height="1198" alt="image" src="https://github.com/user-attachments/assets/159dc902-b449-40af-be82-008931b9c6a8" />
<img width="1181" height="837" alt="image" src="https://github.com/user-attachments/assets/de272872-3e20-4eb8-acd5-285da162cd89" />
<img width="1166" height="504" alt="image" src="https://github.com/user-attachments/assets/1efde322-4b96-462d-9427-828101637167" />
<img width="1166" height="1095" alt="image" src="https://github.com/user-attachments/assets/928d9218-d5b0-4ccf-9257-d06c5e611369" />
<img width="1140" height="590" alt="image" src="https://github.com/user-attachments/assets/4e36f834-7a0e-4130-bb4e-056fe8fe332c" />
<img width="1183" height="719" alt="image" src="https://github.com/user-attachments/assets/dd8e4314-e83d-4b89-becd-38b8332754ed" />
<img width="1142" height="920" alt="image" src="https://github.com/user-attachments/assets/b14446a6-0c9d-4797-bb43-69e7fbf67467" />
<img width="1158" height="832" alt="image" src="https://github.com/user-attachments/assets/a9272926-ed05-4b95-bb91-542feff7c752" />

## 5 Queries:
1. This insight enables managers to identify natural product pairings that customers frequently buy together, which can guide decisions on selling strategies, promotional placement, and personalized product recommendations.
<img width="1000" height="1051" alt="q1" src="https://github.com/user-attachments/assets/f9b023c3-1b6b-4b4f-912e-e7c9eeef4090" />

2. The results help managers recognize the organization’s most valuable customers, determine which buyers may be losing interest, and shape loyalty, retention, and marketing strategies based on customer spending behavior and engagement patterns.
<img width="1035" height="991" alt="q2" src="https://github.com/user-attachments/assets/8d310841-1e16-42b4-9419-410a3ba57427" />

3. This information supports managerial decisions by highlighting which product categories and shipping partners drive the most orders and revenue, helping managers evaluate performance, optimize shipping partnerships, and ensure that service levels align with profitability goals.
<img width="600" height="400" alt="q3" src="https://github.com/user-attachments/assets/4c79b8f9-4b8b-4614-8e3c-35d7fd024ba2" />
<img width="400" height="700" alt="q3a" src="https://github.com/user-attachments/assets/b1ff111f-cb35-4d8f-85c5-b9d56c26a487" />

4. Understanding how many products customers add to their carts but never purchase allows managers to detect potential revenue loss, diagnose friction in the shopping or checkout process, and implement targeted remarketing or UX improvements to increase conversions.
<img width="600" height="600" alt="q4" src="https://github.com/user-attachments/assets/a2280591-4930-4889-b1a1-9afd5803f684" />
<img width="400" height="1200" alt="q4a" src="https://github.com/user-attachments/assets/60dd59ec-d557-4852-b627-daa38a3a9936" />

5. 
 
## Metabase Visualizations:
<img width="1050" height="500" alt="revenue" src="https://github.com/user-attachments/assets/827bd7bf-54fd-4696-ba17-4f4cdcf7f1e7" />
<img width="1050" height="500" alt="sales" src="https://github.com/user-attachments/assets/35bb40c5-e77d-4d3b-8e26-c1de421425bb" />
<img width="1100" height="500" alt="rating" src="https://github.com/user-attachments/assets/e3c14d4e-78ba-4e21-bd33-fbee8a5b4309" />

Total Revenue per Category:

* Purpose: To show how much total revenue each product category generates, based on the sum of all order-item sales.
* Relevance: This chart helps managers quickly see which categories drive the most money for the business. Management can decide where to invest more resources, which categories may need promotions, and where margins may be improved. It also highlights categories that may be underperforming relative to expectations or inventory levels.

Number of Sales per Category:

* Purpose: To measure how many orders include products from each category.
* Relevance: A high order count indicates strong customer demand, even if the category’s revenue is not the highest. Management can identify which categories are growing in popularity and which ones may need marketing support. Comparing order volume with revenue also reveals whether some categories sell many small orders or fewer big-ticket items — crucial for pricing, bundling, and inventory decisions.

Average Customer Review Rating per Category:

* Purpose: To show the average customer review rating for products in each category.
* Relevance: This chart provides insight into customer satisfaction and product quality. Categories with high revenue but low ratings may require attention — poor customer experience can harm repeat purchases. Conversely, categories with high ratings can be leveraged for brand value or upsell opportunities. This chart helps management prioritize quality improvements, customer support initiatives, and product development.

## Database Information:

