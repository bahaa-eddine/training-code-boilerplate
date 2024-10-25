# Sequence Diagram

```mermaid
sequenceDiagram
    Actor Customer
    participant Frontend
    participant Backend
    participant Database

    Customer ->> Frontend: Select product
    Frontend ->> Backend: Add product to cart
    Backend ->> Database: Update cart with selected product
    Customer ->> Frontend: View cart
    Customer ->> Frontend: Place order
    Frontend ->> Backend: Send order details
    Backend ->> Database: Save order
    Backend ->> Frontend: Confirm order
    Frontend ->> Customer: Show confirmation
```