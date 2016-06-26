FINT89 - Statement of Account
*****************************

.. image:: fint89.PNG
    :align: center
    :scale: 50%
    :alt: FINT89 window

Overview
---------
FINT89 - Statement of Accounts is used to monitor the outstanding balances from customers or to the vendors.

Purpose
-------
* View Statement of Account for Customer / Vendor / Accounts
* Print the 'Oustanding Statement' for Customer / Vendor / Account balances

Filters and Shortcuts
---------------------
The module includes a few mandatory filters to define the account parameter, and a few additional filters that have an impact on how the report is displayed.

.. image:: fint89_filters.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Filters

* **CC** - The company.
* **BA** - The business area.
* **A.T.** - The account type.
* **Cust/Vend/Acc.** - The customer / vendor / account number for which we need to view the transaction. This contains an adjacent dropdown menu which defines whether the customer / vendor or account statement is being searched.
* **Start Date** - The start date for the transactions for which we want to see the outstanding report.
* **Base Data** - The date which will form the basis for calculation of age breakdown.
* **G/L Acct.** - In some cases, the transactions for customer / vendor are posted to different GL accounts. In such cases, this fitler can be used to select a branch of transactions for the customer / vendor.
* **Reporting Currency** - Defines the currency at which the statement of account is displayed. This filter also contains an adjacent dropdown which provides a choice between the home currency and other currency (which needs to be defined explicitly).
* **Period** - This dropdown defines how the Start Date is interpreted. Options available are 'Invoice Date', 'Document Date' and 'Due Date'. Based on the selection, the period for transactions is interpreted and the search results displayed.
* **Ageing Slot** - The age breakdown provided by the module can be customized by defining different period ranges in the master configuration. This filter provides the list of all available ageing slots.
* **Cheque Criteria** - This filter defines if the PDC transactions are to be included or excluded from the statement of account. This can be done via selection from the adjacent dropdown.
* **Open Sales Order** - By default the statement of account only displays sales invoices (LI / EI / CI)  in the listing. However, if the open sales orders (that are pending for tranformation to invoice) are to be included in the statement of account, this checbox can be ticked.

Viewing the Statement of Account
---------------------------------

* Select the desired Company and Business Area.

As the module is used to view statement of accounts for either of 'Customer', 'Vendor' or 'Account', we will look at next step for each of the cases individually:

Customer Account
^^^^^^^^^^^^^^^^
* Select 'Customer' as the droption option from Cust / Vend / Acc.
* Click on the magnifying glass icon inside the Cust / Vend / Acc input. This brings up an additional dialog for selection of the required customer account.

.. image:: fint89_custsearch.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Filters

As seen in the screenshot above, the dialog provides filters like 'Customer' (customer number), 'City' and 'Name' (any part of the company name can be entered here enclosed by '%'s. For example: to search for Jizan, we can use '%JIZAN%').

Once the desired customer is found, we can double click on the row for the customer or select the entire row and click the 'OK' (seen as checkmark icon) button.

Vendor Account
^^^^^^^^^^^^^^
* Select 'Vendor' as the droption option from Cust / Vend / Acc.
* Click on the magnifying glass icon inside the Cust / Vend / Acc input. This brings up an additional dialog for selection of the required vendor account.

.. image:: fint89_vendsearch.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Filters

As seen in the screenshot above, the dialog provides filters like 'Customer' (vendor number), 'City' and 'Name' (any part of the company name can be entered here enclosed by '%'s. For example: to search for Jizan, we can use '%JIZAN%').

Once the desired vendor is found, we can double click on the row for the vendor or select the entire row and click the 'OK' (seen as checkmark icon) button.

View the Statement
^^^^^^^^^^^^^^^^^^

* Change the additional filters as required and make sure that all mandatory fields are filled.
* Press the 'F3' button or click the 'Search' button.

.. image:: fint89_csearch.PNG
	:align: center
	:scale: 80%
	:alt: Date Shortcuts

Understanding the Result Table
------------------------------
The search result now displays the information related to the selected customer / vendor / account in three different result grids: Matched Invoices, Unmatched Doc List and Ageing Breakdown.

Matched Invoices
^^^^^^^^^^^^^^^^
The first result grid 'Matched Invoices', displays all documents that are already matched (in other words, already settled via payment or any other transaction). 

.. image:: fint89_matched.PNG
	:align: center
	:scale: 75%
	:alt: FINT61 Result

* **Post Date** - The date when the document was posted in the system.
* **Doc. Type** - The document type.
* **Doc. No** - The document reference for the transaction.
* **Itm. No.** - The unique line item for the transaction within the source document.
* **Sales Type** - This column displays the sales order type in case we are viewing the statement for customer and the doc type is a sales invoice.
* **Sales Doc** - This column displays the sales order number in case we are viewing the statement for customer and the doc type is a sales invoice.
* **Debit** - The debit amount of the transaction in the document currency.
* **Credit** - The credit amount of the transaction in the document currency.
* **Balance** - The net affect of the transaction in the document currency.
* **Doc Curr** - The document currency for the transaction.
* **Cheque Stat** - The status of cheque (only displayed where applicable) 
* **Dbt(Rep. Cur)** - The debit amount of the transaction in the reporting currency selected.
* **Crd(Rep. Cur)** - The credit amount of the transaction in the reporting currency selected.
* **Bal(RepCur)** - The net affect of the transaction in the reporting currency selected.
* **RepCurr** - The reporting currency selected.
* **MatchDType** - The corresponding document type with which the current transaction has been matched. 
* **MatchDnum** - The corresponding document number with which the current transaction has been matched.
* **MatchedAmnt** - The amount which has been matched (settled).

In case the source document for the transaction needs to be accessed, a quick access shortcut has been included in FINT89. Select the entire row for the transaction you wish to see the source document. Then click on the 'Show Details' button (with an aye icon). This opens up the related transaction with the document.

.. image:: matched_source.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Matched Result

UnMatched Doc List
^^^^^^^^^^^^^^^^^^
The result grid 'UnMatched Doc List', displays all documents that have not been settled yet i.e. that have not been matched in the system.

.. image:: fint89_unmatched.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Unmatched Result

* **Post Date** - The date when the document was posted in the system.
* **Due Date** - The due date for the particular transaction.
* **Doc. Type** - The document type. 
* **Doc. No** - The document reference for the transaction.
* **Itm. No.** - The unique line item for the transaction within the source document.
* **Sales Type** - This column displays the sales order type in case we are viewing the statement for customer and the doc type is a sales invoice.
* **Sales Doc** - This column displays the sales order number in case we are viewing the statement for customer and the doc type is a sales invoice.
* **Debit** - The debit amount of the transaction in the document currency.
* **Credit** - The credit amount of the transaction in the document currency.
* **Balance** - The net affect of the transaction in the document currency.
* **Cheque Stat** - The status of cheque (only displayed where applicable) 
* **Curr(Doc)** - The document currency for the transaction.
* **Dbt(Rep. Cur)** - The debit amount of the transaction in the reporting currency selected.
* **Crd(Rep. Cur)** - The credit amount of the transaction in the reporting currency selected.
* **Bal(RepCur)** - The net affect of the transaction in the reporting currency selected.
* **Curr(Rep)** - The reporting currency selected.

Similar to the matched result grid, the quick access to source documents is available via 'Show Details' button (with an eye icon). Select the entire row for the transaction for which you wish to see the source document. Then click the button. This opens up the related transaction with the document.

.. image:: unmatched_source.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 UnMatched Result

Ageing
^^^^^^
The 'Ageing' result grid provides the age breakdown of the outstanding (unmatched) transactions. The presentation of this result grid depends on the selection of the ageing slot.

.. image:: fint89_ageing.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Ageing Result

* **Total Balance** - The total outstanding amount.
* **Amount** - The total outstanding amount.
* **Breakdown - Dynamic Columns** - The additional columns in the grid are dynamically displayed based into as multiple age groups on the ageing slot's configuration.

Printing Outstanding Statement
------------------------------
Once the statement of account is generated from the module for a customer / vendor, the information can be printed to PDF / Printer. Click on the 'Print' button (displayed as printer icon) adjacent to the search button.

.. image:: fint89_print.PNG
	:align: center
	:scale: 80%
	:alt: FINT89 Ageing Result

The system generates a PDF file containing the outstanding statement and the age breakdown as seen below.

.. image:: fint89_printresult.PNG
	:align: center
	:scale: 75%
	:alt: FINT89 Ageing Result