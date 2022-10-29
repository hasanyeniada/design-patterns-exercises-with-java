# Online Shopping System in Java
Application includes:
 - State Design Pattern
 - Sequence Diagram

### Exercise Details & Requirements:
1. Suppose, an online store sells mix dried fruits to its customers. Customers have attributes which are id, name, address, savings, phone, email and password. Customer informations will be held in a file namely customers.json.
2. Orders have id, tracking number, customer id, customer name, weight, shipping address, date shipped, date delivered, product price, cargo price, total price and state attributes. Orders that are delivered to its customer successfully will be recorded into a file namely orders.json.
3. State diagram of the order is given below in diagram.png. The order will be set in each state incrementally and the next state is determined according to the following specifications:

Saved:
- id, tracking number, customer id, customer name, shipping address and weight will be set. Id will be the next number of the latest recorded order’s id. Tracking number will be a 6-figure number that is created randomly. Weight will be specified by customer.
Placed:
- A delivery distance will be created randomly between 100-500. Cargo price will be calculated by taking 0.53 TL per km in delivery distance. Product price will be calcultaed by taking 55 TL per kg in weight.
Charged:
- The total price of the order is set.
- If the savings of customer smaller than the total price of the order, the next state will be Placed.
Shipped:
- Planned and real shipping duration in days will be generated randomly between 1-10.
- When realShippingDurationInDays – plannedShippingDurationInDays > 7, it means that Error: Not shipped.
- When the error condition above does not hold, date shipped will be set.
Delivered:
- Planned and real delivery duration in days will be generated randomly between 3-12.
- When realDeliveryDurationInDays – plannedDeliveryDurationInDays > 8, it means that Error: Lost in shipping
- If the above error condition does not hold, date delivered of the order will be set.
  
1. Store has the following responsibilities:
    Charge customer
    Cancel payment
    Ship order
    Deliver order
2. Customer has the following responsibilities:
    Save order
    Submit order
    Cancel order
    Delete order
3. Implement a class namely Shopping, which shows the state change of order by making a customer place an order. The methods of the customer and the store will help determining the next state of the order.
4. Customers will register to the system by providing their informations. When they register, their information will be written to the corresponding customers file.
5. Customers will login to the system by providing their registered mail address and password.
6. Remember to update the savings of a customer when she/he is charged or cancels the order.