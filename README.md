# stuga

In this implementation, two code files are modified:

snippets\product-form.liquid
snippets\product-calculator.liquid

The product-form.liquid file conditionally includes the product-calculator.liquid if the product metafields include the "carton-value" namespace.

The layout and scripts for the calculation are fully contained within "product-calculator.liquid". The logic is written long-form to allow a novice user to follow and modify the calculation in case of need.

# Add or edit Shopify Metafields

Log into the Metafields Editor at:

http://metafieldseditor.herokuapp.com/home/index

Using the URL of your Shopify store and your login credentials.

Locate the product you want to edit from the list. You may sort by collection, or search by product title.

Click on the product title, then click on "Add New Metafield".

Use "carton-value" as your Namespace.
Set "per-unit" as the key.
The "Value type" needs to be string (to accommodate digits after the decimal point).
Finally, the value would be the the square footage per box (i.e., 29.28).
Click "Add" to finish.

The square footage for that product is now available to the calculator on the product detail page of the site.

Conditional display has been enabled. The calculator only shows for products that have a per unit metafield value assigned.
