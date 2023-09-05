## Basic Overview

the code has 3 classes,

1. Products- For fetching the products from contentful, products can be also be fetched from products.json file.

2. UI- This class is used for displaying everything on the website.

3. Storage- For storing the products on the website and products in the cart in local storage.

### Functioning of different methods

MAIN of the code

- As soon as the Website loaded, we create two new objects, ui and products from classes UI and Products.
- Then we call setupAPP function from ui class.
- After that we call getProducts function from products class, then displayProducts function from the ui class and then saveProducts function from the storage class.
- After fetching the products, displaying them and storing them in local storage, we call getBagButton function and after that cartLogic function.

1. UI
   a. setupAPP()

   - This method is setting up the cart by using the cart array and calling the getCart function from storage.
   - Then after receiving the products in the cart array from getCart method, it calls setCartValues and populateCart.
   - On clicking the cart icon you can see the cart because of showCart method.
   - On clicking the close icon you can remove the cart because of hideCart method.

   b. setCartValues()

   - This method sets the cart total and the amount of items in the cart.

   c. populateCart()

   - This method is used to display the products in the cart using addCartItems method.

   d. addCartItems()

   - This method creates a product dynamically and displays it on the website.

   e. showCart()

   - This method adds 2 classes to make the cart visible.

   f. hideCart()

   - This method removes 2 classes to make the cart visible.

   g. displayProducts()

   - This method creates a product dynamically and displays it on the website.

   h. getBagButtons()

   - After the products got loaded on the website, we have button for each product that indicate that if the product is in the cart or can be added in the cart.
   - After that we have added the products in the cart array.
   - Saved the cart array in local storage using saveCart function.
   - Using setCartValues function updated the total amount and quantity of items in the cart.
   - Using addCartItems function we have displayed the products in the cart.

   i. cartLogic()

   - We have clearCart function here that helps us to remove all the products from the cart.
   - Then we have a common event listener for the cart content, if we click on remove button, removeItem method is called, if we click on up button then the quantity of product increases and the total amount of the cart also increases similarly for the down button

   j. clearCart()

   - Here first the product is removed from the cart array and then from the ui.

   k. removeItem()

   - This method is called when remove button is clicked or the value of product becomes less than 1 while clicking the down button to decrease the quantity of product in the cart and also when clear cart method is called.

2. PRODUCTS
   a. getProducts()

   - Here, we are fetching ht products from contentful. Destructing the the items and providing them different fields and returning a array of products.

3. STORAGE
   a. getCart()

   - This method returns the products in the cart if any if there are no products in the cart, it returns an empty array.

   b. saveProducts()

   - This methods stores all the products fetched from the contentful in local storage in a string format.

   c. saveCart()

   - This methods stores all the products in the cart array in local storage in a string format.
