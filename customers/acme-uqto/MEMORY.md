# MEMORY — microservices-demo

_The agent's always-in-context core memory of this system._

- System: The system is a cloud-first microservices demo application, composed of 11 microservices written in different languages that talk to each other over gRPC. The application is a web-based e-commerce app where users can browse items, add them to the cart, and purchase them.
- Services: frontend, cartservice, productcatalogservice, currencyservice, paymentservice, shippingservice, emailservice, checkoutservice, recommendationservice, adservice
- Business: Online Boutique storefront; checkout is SLA-critical.
- Risk: Single point of failure in the checkout service
- Risk: Insufficient error handling in the payment service
- Risk: Insecure data storage in the email service
