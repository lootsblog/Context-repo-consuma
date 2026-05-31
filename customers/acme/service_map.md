# Service Map

## Services
- frontend
- cartservice
- productcatalogservice
- currencyservice
- paymentservice
- shippingservice
- emailservice
- checkoutservice
- recommendationservice
- adservice

## Component detail

| Component | Responsibility | Tech | Depends on | Data store |
|---|---|---|---|---|
| `frontend` | Exposes an HTTP server to serve the website. | Go | cartservice, productcatalogservice, currencyservice, checkoutservice | — |
| `cartservice` | Stores the items in the user's shopping cart in Redis and retrieves it. | C# | redis | Redis |
| `productcatalogservice` | Provides the list of products from a JSON file and ability to search products and get individual products. | Go | — | JSON file |
| `currencyservice` | Converts one money amount to another currency. | Node.js | — | — |
| `paymentservice` | Charges the given credit card info (mock) with the given amount and returns a transaction ID. | Node.js | — | — |
| `shippingservice` | Gives shipping cost estimates based on the shopping cart. | Go | — | — |
| `emailservice` | Sends users an order confirmation email (mock). | Python | — | — |
| `checkoutservice` | Retrieves user cart, prepares order and orchestrates the payment, shipping and the email notification. | Go | cartservice, paymentservice, shippingservice, emailservice | — |
| `recommendationservice` | Recommends other products based on what's given in the cart. | Python | — | — |
| `adservice` | Provides text ads based on given context words. | Java | — | — |
