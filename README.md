Exercise 1: Basic Model Creation and CRUD

Create a new Rails API project named "product_api".
`rails new product_api --api`

Objective: Understand basic model creation and perform CRUD operations using Rails console.

Tasks:

Generate a Product Model: Attributes - name:string, price:decimal
`rails g model Product name:string price:decimal`

Perform CRUD Operations:

Create a new product with the following attributes:
- Product 1
  name: "Apple"
  price: 1.99
`product1 = Product.create(name: "Apple", price: 1.99)`
  
- Product 2
  name: "Orange"
  price: 2.99
`product2 = Product.create(name: "Orange", price: 2.99)`

- Product 3
  name: "Banana"
  price: 3.99
`product3 = Product.create(name: "Banana", price: 3.99)`

- Product 4
  name: "Grapes"
  price: 4.99
`product4 = Product.create(name: "Grapes", price: 4.99)`

- Product 5
  name: "Pineapple"
  price: 5.99
`product5 = Product.create(name: "Pineapple", price: 5.99)`

Get all products.
`Product.all`

Get the product with the id of 3.
`Product.find(3)`

Get product by name "Apple".
`product1 = Product.find_by(name: "Apple")`
but also
`Product.find_by(name: "Apple")` works

Update the product's name of 'Apple to "Lime".
`product1.update(name: "Lime")`

Delete the product with the id of 1.
`Product.find(1).delete`

Delete all products whose price is greater than 3. Use the where method.
`Product.where("price > 3").delete_all`
- .delete_all - deletes all records that match the condition
- .delete - will only delete the first record found

