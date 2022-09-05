# REST


## How I explained REST to my brother

1. Who is Roy Fielding?

    He is a smart guy helped write the first web servers, that sent documents across the internet… and then he did a ton of research explaining why the web works the way it does. His name is on the specification for the protocol that is used to get pages from servers to your browser.

2. Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?

Because they weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements.


3. What is the HTTP protocol that Fielding and his friends created?

is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you typed in and back comes a web page.

4. What does a GET do?

or instance, when you go to a web page, the browser does an HTTP GET on the URL you typed in and back comes a web page.

Web pages usually have images, right? Those are separate resources. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL.

5. What does a POST do?

If one system needs to add something to another system, it would use an HTTP verb of POST.

6. What does PUT do?

If a system wants to replace something in another system, it uses an HTTP verb of PUT,


7. What does PATCH do?

use  to do a partial update.


## API Keys

### Geocoding API
Did you get your API key?

yes, and used it class 6 lab

### Weather Bit API
Did you get your API key?
yes

### Yelp API Docs
yes

### The Movie DB API Docs

yes