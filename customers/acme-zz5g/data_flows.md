# Data Flows

How requests and data move through the system.

- frontend -> productcatalogservice
- frontend -> cartservice
- cartservice -> redis
- checkoutservice -> paymentservice
- checkoutservice -> shippingservice
- checkoutservice -> emailservice
