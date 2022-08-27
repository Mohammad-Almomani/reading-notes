# APIs




1. What does REST stand for?

    Roy Fielding proposed Representational State Transfer 

2. REST APIs are designed around a resources.


3. What is an identifier of a resource? Give an example.

    A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

    >HTTP
    https://adventure-works.com/orders/1

4. What are the most common HTTP verbs?

    The most common operations are GET, POST, PUT, PATCH, and DELETE.

5. What should the URIs be based on?

    nouns (the resource)

6. Give an example of a good URI.

    >HTTP
    https://adventure-works.com/orders // Good


7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

    web APIs that expose a large number of small resources, avoid it its bad thing

8. What status code does a successful GET request return?

    status code 200 


9. What status code does an unsuccessful GET request return?

     404 (Not Found)

10. What status code does a successful POST request return?

    status code 201

11. What status code does a successful DELETE request return?

    status code 204


