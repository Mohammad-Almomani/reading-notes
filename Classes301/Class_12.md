# CRUD


## Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:

    * 100’s = Informational status codes, They typically inform the client that the header portion of the request has been received and that the server will attempt to meet the client's transmission request. 
    * 200’s = Success codes, They inform the client that their request has been granted.
    It merely means that the request satisfies all validation requirements at the moment of submitting when a request is handled asynchronously (202), not that the request was properly processed.

    * 300’s = Redirection codes, They inform the client that the requested resource is no longer available at the anticipated location.

    * 400’s = Client error codes, They all concern erroneous requests that clients sent to servers. There are various reasons for this, including timeouts, incorrect URIs, and a lack of authentication.

    * 500’s = Server error codes, They frequently point to issues with overloaded servers or servers behind proxies that are inaccessible, but occasionally they might be directly connected to client requests that result in error exceptions on the server.

2. What is a status code 202?

    Accepted, Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future.


3. What is a status code 308?

    Permanent Redirect , This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.

4. What code would you use if an update didn’t return data to a client?

    Status code 204: No Content

5. What code would you use if a resource used to exist but no longer does?

    Status codes 300's

6. What is the ‘Forbidden’ status code?

     Status code 403 Forbidden: the client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.



## Build A REST API With Node.js, Express, & MongoDB


1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?

    because it might have sensitive information's 

2. What is middleware?

    code that runs once the server gets the request but before get passed to the routs

3. What does app.use(express.json()) do?

    let the server accept json as a body inside a post element or a get element.

4. What does the /:id mean in a route?

    that mean that this is a parameter that we can access through req.params.id

5. What is the difference between PUT and PATCH?

    PATCH only update based on what the user pass, if the user passes a name, only the name will be updated, PUT will update all the information's at once

6. How do you make a default value in a schema?

    add a new options in the schema called default and git it a value

7. What does a 500 error status code mean?

    Server error that caused the actual transaction not to work

8. What is the difference between a status 200 and a status 201?

    201 mean successfully created an object, 200 mean that everything was successfully but without specifying.