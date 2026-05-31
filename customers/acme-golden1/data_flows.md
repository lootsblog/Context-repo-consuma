# Data Flows

How requests and data move through the system.

- frontend -> cartservice -> redis
- frontend -> productcatalogservice -> json file
- frontend -> currencyservice -> European Central Bank
- checkoutservice -> paymentservice -> credit card info
- checkoutservice -> shippingservice -> shipping cost estimates
- checkoutservice -> emailservice -> order confirmation email
- recommendationservice -> productcatalogservice -> product list
