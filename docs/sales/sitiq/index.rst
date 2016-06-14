SITIQ - Item Enquiry
********************

.. image:: sitiq.png
    :align: center
    :scale: 50%
    :alt: SITIQ window

Overview
---------
SITIQ is the abbreviated word for Sales Item Enquiry. The module was initiated to centralize the most common operations from the shop side like 'Creation of Sales Orders', 'Transfer of Stocks (Intra and Inter Company)' together with the stock status report. Comprehensive details on the purpose of the module has been discussed in the following section.

Purpose
-------
* Central view of the inventory across multiple plants, with quick access to 'Sales History', 'Purchase History' & 'Item Master'
* Shortcut to creation of sales orders
* Creation of transfer orders (within the same plant or among different plants)

Filters and Shortcuts
---------------------
The module includes filters primarily aimed at narrowing down the list of items fetched by the system.

.. image:: sitiq_filters.PNG
	:align: center
	:scale: 75%
	:alt: SITIQ window

* **Company** - Company for which the information is to be displayed.
* **Plant** - The plant for which the information is to be displayed.
* **Location1** - This button opens up a dialog to filter for the Warehouses available to the selected plant and company. Multiple selections can be made.

.. image:: filter_location.PNG
	:align: center
	:scale: 75%
	:alt: SITIQ window

* **Material** - Filter that accepts the Material Code as input.
* **Material Name** - This is the filter which accepts the material name (or part of it) as input.

	.. note:: This is the most common filter used in the transaction, and can be used as a handy shortcut to quickly find items.

	* Any part of the name can be used. For example: 'cool water' when searching for 'DAVIDOFF COOL WATER (L) EDT 100 ml'
	* The system automatically convers blank spaces to '%' allowing easy search. For example 'cool water 100' will yeild results with all cool water items of size 100ml. Similarly 'c w 100' would yeild the results of items which have c, w and 100 characters in them.

* **Plant2** - This is used when the inventory data is to be compared against multiple plants. If this field is provided, the system shows results for both plant 1 and plant 2, in separate columns. Also, the inter plant selling price is shown if defined.
* **Location2** - This is the filter for warehouses that belong to Plant2. Similar to Plant1, multiple selections can be made.
* **Customer** - This filter is more of a parameter to the process of creating sales orders. In case prices have been customized per user, this filter determines which price is shown in the SP (Selling Price) field of the result table.

In addition to the filters discussed above, there are checkbox filters that controls the visibility of information in SITIQ.

.. info:: These checkboxes might not be available to all users because of the access rights.

* **List Stock Materials?** - If the checkbox is selected, the system only displays items which we currently have in stock in the selected plant / warehouse. To view all items, simply uncheck this checkbox.

.. _checkbox_salqty:
* **Incl. SalQty** - The sales orders created in canias do not reflect in the inventory side untill the delivery note is created and the items are issued out. In this case, the default list shown in SITIQ would display full stock of items, without considering those already created sales orders. This checkbox allows the user to view the net stock for items (available stock - stocks used in current sales orders). Click the checkbox to view Net Quantity, and remove the checkmark to view Gross Quantity.
* **Change Price?** - This button is a support to the process 'Changing System Selling Price'. Clicking the button shows an additional column in the result table for editing of the system selling prices.
* **Enable Cost** - This checkbox serves as user access control for display of cost related information for the item. If this checkbox is selected, the fourth tab in the lower section of the screen becomes active. This tab displays weighted average cost rate for the item that is currently selected in the result table.

.. image:: sitiq_costinfo.PNG
	:align: center
	:scale: 75%
	:alt: SITIQ window

* **Show Stock** - This checkbox serves as user access control for display of stocks across all companies and plants in canias. If this checkbox is selected, the first tab in the lower part of screen becomes active. This tab displays the availability of selected item from the result set in all plants and warehouse.

Searching for Items
-------------------
* Enter the required filter criterias in the filter boxes. Most commonly the filters would be entered in the 'Description' field where any part of the name of the item is entered.
* Press the 'F3' button or click the 'Search' button.

.. image:: sitiq_search.PNG
	:align: center
	:scale: 75%
	:alt: SITIQ window

Depending on the search filters provided, the system looks up the stock information and lists them in the result window.

Understanding the Result Table
------------------------------
The result table in SITIQ displays key information related to the item, which as been discussed below:

.. image:: sitiq_result.PNG
	:align: center
	:scale: 75%
	:alt: SITIQ window

* **Description** - This column displays the name of the Material.
* **STK** - The second column displays the available stock for the items. The result in this column varies with the filter checkbox 'Incl. SalQty' as described here - :ref:'Checkbox - Incl Sal. Qty <checkbox_salqty>'

Creating Sales Orders
---------------------
This section describes how the sales order can be created.

Creating Transfer Orders
------------------------
This section describes how the transfer orders can be created.