# Grocery Taxi

## Goal
* Provide REST API (and basic web UI) to connect grocery consumers and couriers who will carry food from stores to consumers.

### Use cases
* Register as a consumer

> User should be able to register as a consumer providing minimal information (name). OAuth integration (Google, GitHub, Facebook) is required.

* Register as a courier

> User should be able to register as a consumer providing minimal information (name). OAuth integration (Google, GitHub, Facebook) is required.
* Create an order

> Consumer should be able to create an order by selecting items (from the list predefined in DB). Order should be in ‘draft’ state until consumer confirms it.
> Consumer should be able to edit draft orders.
> Consumer should be able to confirm an order. After this action order must not be editable. Order is ‘open’ as the result of the action.

* View orders

> Any courier should be able to see open orders.
> For each order approximate price should be calculated (using item prices from DB) and shown with the order.
> Orders should be sortable by price.

* Pick an order

> Courier should be able to pick an order from list.
> After this action order receives ‘in progress’ state and should not be visible to other couriers. Consumer should be able to see order state.

* Close an order
> Courier and consumer should be able to close an order (with confirmation from both). Closed orders should be visible to consumer and courier.
### Technologies
**Java, Spring Boot, PostgreSQL, Thymeleaf, JUnit, Swagger, Jenkins, Docker**

### Roadmap
1. Create a project template, integrate Spring Boot
2. Implement registration
3. Create infrastructure (Jenkins, environment)
4. Implement order management

### Additional features:
● Introduce geo features: collect consumer address during registration and save it in DB;
show distance from current courier location to this ‘destination’ in order list; sort orders
by distance
● Introduce monitoring with Graphite / Grafana
● Perform load test

