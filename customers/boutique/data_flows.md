# Data Flows

How requests and data move through the system.

- frontend -> cartservice -> Redis
- frontend -> productcatalogservice
- frontend -> currencyservice
- frontend -> checkoutservice -> paymentservice -> shippingservice -> emailservice
