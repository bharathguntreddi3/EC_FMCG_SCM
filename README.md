<!-- Optimizing E-commerce in FMCG Supply Chain & Inventory Management - 

- Supplier management: Add and manage information about your suppliers, including their contact information, payment terms, and order history.

- Inventory management: Track your inventory levels and receive alerts when inventory levels fall below a certain threshold.

- Purchase orders: Create and manage purchase orders for products or raw materials from suppliers.

- Sales orders: Create and manage sales orders for products to customers.

- Reports: Generate reports on inventory levels, sales orders, purchase orders, and more.


Add  suppliers to the suppliers table.

Add  products or raw materials to the products table.

Create purchase orders for products or raw materials from your suppliers using the purchase_orders table.

Receive products or raw materials into your inventory using the inventory table.

Create sales orders for products to your customers using the sales_orders table.

Ship products to your customers and update the inventory table accordingly.

Generate reports on inventory levels, sales orders, purchase orders, and more using SQL queries.
 -->


### Relational Integrity: 


Customers(CustomerID,CustomerName,location_id) 
Foreign key location_id refers to locationid in locations; Null Not allowed 

Customer_contacts(customer_id, contact_type, contact_info) 

Location(location_id, city, state,zip) 
Inventory(Inventory_id, name, location_id) 
Foreign key location_id refers to locationid in locations; Null Not allowed 

Inventory_stocks(Inventory_id,product_id,quantity) 
Foreign key Inventory_id refers to Inventoryid in Inventories; Null Not allowed

Products(Product_id,product_name,actual_price,selling_price,expiry_date)

Suppliers (Supplier_id, supplier_name,location_id)
FOREIGN KEY location_id refers to location_id in Locations Table; Null Not allowed

Supplies (supplier_id, product_id)
FOREIGN KEY product_id refers to product_id in Products Table; Null Not Allowed
FOREIGN KEY supplier_id refers to supplier_id in Suppliers Table; Null Not allowed

Purchase_orders (purchase_id,supplier_id, product_id, purchase_quantity, unit_price, order_date, delivery_date)
FOREIGN KEY product_id refers to product_id in Products Table; Null Not allowed
FOREIGN KEY supplier_id refers to supplier_id in Supplier Table; Null Not allowed

Orders (order_id, inventory_id, order_date, product_id, selling_price, quantity_ordered)
FOREIGN KEY product_id refers to product_id in Products Table; Null Not allowed
FOREIGN KEY inventory_id refers to inventory_id in Inventory Table; Null Not allowed

Customer_orders (order_id, customer_id)
FOREIGN KEY order_id refers to order_id in orders Table; Null Not allowed
FOREIGN KEY customer_id refers to customers in Products Table; Null Not allowed

(database files online data sources)
