# Bamazon

## Description

This is an Amazon-like storefront utilizing my MySQL and node skills. The app will take in orders from customers and deplete stock from the store's inventory. This app requires the MySQL and Inquirer npm packages in order for it to work. THe app needs them for data input and storage

The application presents two interfaces: **customer** and **manager**.



### Customer Interface

The customer interface allows the user to view the current inventory of store items: item IDs, descriptions, department in which the item is located and price. The user is then able to purchase one of the existing items by entering the item ID and the desired quantity. If the selected quantity is currently in stock, the user's order is fulfilled, displaying the total purchase price and updating the store database. If the desired quantity is not available, the user is prompted to modify their order.

- When the bamazonCustomer.js file is run, the customer is shown the current inventory and asked what product they would like to puchase. They must input the item ID and how many they would like to purchase.
	
	- If the product is in stock, it tells the customer and places their order. It will display their total and exit the app.
		- ![image of customer placing order](/images/customer_order_placed.png)
	
	- The database will then be updated to reflect the current inventory, minus what the customer just purchased.
		- ![image of updated db](/images/customer_stock_updated.png)
	
	- If the product is not in stock, the app will inform the user and prompt them with the current inventory again.
		- ![image of out of stock](/images/customer_not_enough_stock.png)



### Manager Interace

The manager interface presents a list of four options, as below. 

	? Please select an option: (Use arrow keys)
	❯ View Products for Sale 
	  View Low Inventory 
	  Add to Inventory 
	  Add New Product
	  
- The **View Products for Sale** option allows the user to view the current inventory of store items: item IDs, descriptions, department in which the item is located, price, and the quantity available in stock. 
	- ![image of manager products for sale](/images/manager_view.png)

- The **View Low Inventory** option shows the user the items which currently have fewer than 100 units available.
	- ![image of manager low inventory](/images/manager_low.png)

- The **Add to Inventory** option allows the user to select a given item ID and add additional inventory to the target item. This inventory update will also be shown in the database
	- ![image of manager update inventory](/images/manager_update_inventory.png)
	- ![image of manager update inventory](/images/manager_db_updated.png)

- The **Add New Product** option allows the user to enter details about a new product which will be entered into the database upon completion of the form. The new item will be visable in the database after updating.
	- ![image of manager add item](/images/manager_add.png)
	- ![image of manager add item](/images/manager_db_add.png)

