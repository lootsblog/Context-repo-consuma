# MEMORY — microservices-demo

_The agent's always-in-context core memory of this system._

- System: The system is a cloud-first microservices demo application, composed of 11 microservices written in different languages that talk to each other over gRPC. The application is a web-based e-commerce app where users can browse items, add them to the cart, and purchase them.
- Services: frontend, cartservice, productcatalogservice, currencyservice, paymentservice, shippingservice, emailservice, checkoutservice, recommendationservice, adservice
- Business: Online Boutique is our flagship e-commerce storefront. Checkout availability directly affects revenue and is the most SLA-critical path; the cart must survive pod restarts.
- Risk: Single point of failure for checkout: if redis-cart drops, carts fail and checkout aborts
- Risk: Brief redis-cart connection drop can cause a checkout error spike
- Decision: ADR-003: gRPC between services for typed contracts and low latency
- Decision: ADR-009: cart state externalized to Redis so cartservice stays stateless and horizontally scalable
- Decision: ADR-014: each service owns its Dockerfile; deploys are gated through Skaffold + Kustomize per environment
