# API Gateway

![API Gateway](https://miro.medium.com/v2/resize:fit:720/format:webp/1*M7Tc4AXdM9_EHWw_7OD6FQ.jpeg)

We have API management tools that help create a bridge between a client and the backend services. As the name gateway itself suggests, this is an entry point to get into the system so that the clients can have a well-tailored API. Apart from these, an API gateway is responsible for authentication, [monitoring](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Logging%2C%20Monitoring%2C%20and%20Alerting), [load balancing](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Load%20Balancing), [caching](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Caching), throttling, [logging](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Logging%2C%20Monitoring%2C%20and%20Alerting), etc. With the APIs provided by different [microservices](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Microservices), the clients can easily interact with multiple kinds of services.

The main purpose of an API gateway is to create an entry point that lets the clients in the system work with various features. Some common examples of API gateways are Amazon API Gateway, Apigee API Gateway, Azure Gateway, Kong API Gateway, etc.

## Features of API Gateway

- [Service Discovery](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Service%20Discovery)
- [Reverse Proxy](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Proxies)
- [Caching](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Caching)
- [Load Balancing](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Load%20Balancing)
- [Logging](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Logging%2C%20Monitoring%2C%20and%20Alerting), Tracing
- Retry and [circuit-breaking](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Circuit%20Breaker)
- [Rate Limiting](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Rate%20Limiting) and Throttling
- Versioning
- Routing
- IP Whitelisting or blacklisting
- Authentication and Authorization
- API composition
- Security

## Advantages

- The client code is simplified.
- Some features like [monitoring](https://github.com/pragyaasapkota/System-Design-Concepts/tree/master/Logging%2C%20Monitoring%2C%20and%20Alerting), analytics, tracing, etc.
- The internal structure of an API is encapsulated.

## Disadvantages

- The configuration operations are challenging.
- Performance might be affected.
- A single point of failure can cause problems to find out.
- Scaling should be done properly to avoid bottlenecks.

## BFF Pattern

BFF stood for Backend for Frontend and was first introduced by Sam Newman. It can be defined as a pattern where we create separate backend services for a specific frontend interface. We can implement a BFF pattern if we wish to avoid customizing a single backend service for multiple interfaces.

However, the output might sometimes differ from the format of the front end. We can have the front end loaded with some logic to reformat the data so that the BFF can be used to shift some logic to the intermediate layer.

The pattern also gets the formats and sends the data after receiving it from the service. GraphQL is an excellent example of BFF performance.

There are some conditions where it would be a great deal if the BFF pattern is used.

- If you want to optimize the backend to meet the expectations of a specific client.
- If we need to customize general-purpose backends to accommodate multiple interfaces.
- If the general-purpose backend must be maintained with substantial development overhead.
