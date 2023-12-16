---
title: "APIs 101: The What, Why, and How of Application Programming Interfaces"
seoTitle: "APIs 101: The What, Why, and How of Application Programming Interfaces"
seoDescription: "It provides an overview of Application Programming Interfaces (APIs), explaining what they're, why they're essential, and how they're used."
datePublished: Mon Apr 24 2023 03:12:49 GMT+0000 (Coordinated Universal Time)
cuid: clgu9jdj600020ajv6bqkgblt
slug: apis-101
canonical: https://medium.thetechnologist.in/apis-101-the-what-why-and-how-of-application-programming-interfaces-c36a28fa0672
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/hGV2TfOh0ns/upload/44fac32475b0dc1fa5fd96e24d89b4a1.png
tags: software-development, development, apis

---

APIs, or Application Programming Interfaces, are a group of protocols, processes, and tools that let different software programmes talk to each other and work together.

APIs are basically a bridge that lets two apps “talk” to each other and share data and functions without any problems. For example, when you use a weather app to check the news, the app probably uses an API to pull data from a weather service and show it to you in a way that is easy to understand.

APIs let two programmes talk to each other by outlining a set of rules and formats that both programmes must follow. This usually includes sending and receiving requests and responses in a standard format, such as JSON or XML.

APIs can be made for different reasons, such as giving access to data, enabling functionality like payment processing or authentication, or letting third-party developers build on top of current platforms. Overall, APIs are very important because they make it possible for software systems to work together and integrate, which is very important in today’s digital world.

APIs can be put into different types based on how they work and what they are used for. One popular type is the web API, which is made to be used over the internet and is accessed using HTTP requests. Web APIs are often used to give access to online services like social media sites, e-commerce sites, and cloud-based apps.

The operating system API is another type of API. It is made for apps that run on a certain operating system, such as Windows, macOS, or Linux. Operating system APIs let applications talk to the hardware and software parts of the system, like file systems, networking protocols, and device drivers.

Most APIs are made with a certain computer language or framework, like Java, Python, or Node.js. They can also be built using special API design patterns, such as REST (Representational State Transfer) or GraphQL.

Last but not least, it’s important to note that APIs can be made for both internal and external use. Internal APIs are used within a company to make it possible for different tools and departments to talk to each other. On the other hand, external APIs are made so that third-party developers can use them to build apps that work with current platforms and services.

Overall, APIs are a very important part of modern software development. They allow developers to make powerful, connected apps that are easy to use. As technology keeps getting better, APIs are only going to become more important, so any coder or tech enthusiast needs to know about them.

# **Types of APIs**

There are many different kinds of APIs. Each one is made for a specific task and has its own unique features. These are some of the most popular kinds of APIs:

## **RESTful APIs**

REST, which stands for “Representational State Transfer,” is a common way to build web services. RESTful APIs are made to be simple and lightweight. To access and change data, you use HTTP calls. They usually don’t have any state, which means that each request has all the information it needs to be completed. RESTful APIs are used by a lot of web and mobile app developers.

A RESTful API is something like the Twitter API. With HTTP requests, developers can use the Twitter API to view and change data on the Twitter platform. For example, a developer could use the Twitter API to look for tweets that contain a certain keyword, get information about a user’s followers, or post a new tweet to a user’s account.

For developers to use the Twitter API, they must first get an API key and use OAuth to verify their calls. Once they have been verified, they can make HTTP requests to the Twitter API endpoints, which return data in JSON format. For example, a developer could send a GET request to the following location to look for tweets with a certain keyword:

```xml
https://api.twitter.com/1.1/search/tweets.json?q=<keyword>
```

Where **“keyword”** is the word you want to find. The Twitter API will then send back a JSON response with information about the tweets that match, such as the tweet’s text, the person who sent it, and the date and time it was sent.

Overall, the Twitter API is a well-known example of a RESTful API. Developers from all over the world use it to build apps and services that work with Twitter.

**Request:**

```json
GET /1.1/search/tweets.json?q=OpenAI HTTP/1.1
Host: api.twitter.com
Authorization: OAuth oauth_consumer_key="API_KEY_HERE", oauth_nonce="NONCE_HERE", oauth_signature="SIGNATURE_HERE", oauth_signature_method="HMAC-SHA1", oauth_timestamp="TIMESTAMP_HERE", oauth_token="ACCESS_TOKEN_HERE", oauth_version="1.0"
```

In this case, the request is a GET call to the Twitter API’s **/1.1/search/tweets.json** endpoint, with the **“OpenAI”** value for the *“q”* parameter. The API key, access code, and signature, which are needed by OAuth to verify the request, are all in the Authorization header.

```json
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Content-Encoding: gzip
Transfer-Encoding: chunked
Connection: keep-alive

{
    "statuses": [
        {
            "created_at": "Fri Apr 22 22:26:42 +0000 2022",
            "id": 152720976303154432,
            "text": "OpenAI develops an AI-based search engine for scientific papers. \n\nhttps://t.co/nUw7Vz4rxn https://t.co/L1e6RdVMyS",
            "user": {
                "name": "The Verge",
                "screen_name": "verge",
                "location": "New York",
                "followers_count": 3052462,
                "profile_image_url_https": "https://pbs.twimg.com/profile_images/877903823133704194/Mqp1PXU8_normal.jpg"
            }
        },
        {
            "created_at": "Thu Apr 21 18:03:08 +0000 2022",
            "id": 152677070096312576,
            "text": "OpenAI has released GPT-3 API for general availability. \n\nhttps://t.co/8oKbEBq3xq https://t.co/KZiyLJv1aD",
            "user": {
                "name": "TechCrunch",
                "screen_name": "TechCrunch",
                "location": "San Francisco, CA",
                "followers_count": 12254647,
                "profile_image_url_https": "https://pbs.twimg.com/profile_images/1289914286217108481/eSTgfWCa_normal.jpg"
            }
        },
        ...
    ],
    "search_metadata": {
        "completed_in": 0.046,
        "max_id": 0,
        "max_id_str": "0",
        "next_results": "?max_id=152720976303154431&q=OpenAI&count=10&include_entities=1",
        "query": "OpenAI",
        "count": 10,
        "since_id": 0,
        "since_id_str": "0"
    }
}
```

In this case, the answer is a JSON object with a list of tweets that meet the search query “OpenAI.” Each tweet is shown as an object with characteristics like the date it was made, its ID, and the text it contains. The answer also includes information about the search, like how long it took to finish and how to get more results.

Overall, this is just a simple example of what a request and answer might look like when using a RESTful API like the Twitter API. The exact format and structure of requests and responses will depend on the API.

## **SOAP APIs**

SOAP, which stands for “Simple Object Access Protocol,” is an older way to build web services. SOAP APIs are more complicated than RESTful APIs, and they send and receive data through XML messages. Most of the time, they are stateful, which means that they keep a process going between the client and the server. SOAP APIs are less popular than RESTful APIs, but they are still used in enterprise applications and legacy systems.

Here’s an example of what an eBay API SOAP call and response might look like:

```plaintext
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:urn="urn:ebay:apis:eBLBaseComponents">
   <soap:Header>
      <urn:RequesterCredentials>
         <urn:eBayAuthToken>EBAY_AUTH_TOKEN_HERE</urn:eBayAuthToken>
      </urn:RequesterCredentials>
   </soap:Header>
   <soap:Body>
      <urn:GetUserRequest>
         <urn:RequesterCredentials>
            <urn:eBayAuthToken>EBAY_AUTH_TOKEN_HERE</urn:eBayAuthToken>
         </urn:RequesterCredentials>
         <urn:UserID>EBAY_USER_ID_HERE</urn:UserID>
      </urn:GetUserRequest>
   </soap:Body>
</soap:Envelope>
```

In this case, the request is a SOAP message that uses the SOAP envelope format and defines the eBay API namespace. The user ID of the eBay user being asked for is included in the *GetUserRequest* part of the message. In both the title and the body of the message, there is also an *eBayAuthToken* element. This element is used to verify the request.

```xml

<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:urn="urn:ebay:apis:eBLBaseComponents">
   <soap:Body>
      <urn:GetUserResponse>
         <urn:Ack>Success</urn:Ack>
         <urn:User>
            <urn:UserID>EBAY_USER_ID_HERE</urn:UserID>
            <urn:FeedbackScore>500</urn:FeedbackScore>
            <urn:RegistrationDate>2005-06-01T00:00:00.000Z</urn:RegistrationDate>
            <urn:Site>US</urn:Site>
            <urn:Status>Confirmed</urn:Status>
            <urn:SellerInfo>
               <urn:PositiveFeedbackPercent>98.8</urn:PositiveFeedbackPercent>
            </urn:SellerInfo>
         </urn:User>
      </urn:GetUserResponse>
   </soap:Body>
</soap:Envelope>
```

In this case, the answer is a SOAP message with the same format for the namespace and envelope as the request. The message has a GetUserResponse element that gives details about the requested eBay user, such as their feedback score, registration date, site, and status. The message also has an Ack part with the value “Success” to show that the request was successful.

Overall, this is just a simple example of what a SOAP request and response might look like when using an API like the eBay API. The exact format and structure of requests and replies will rely on the API being used.

## **GraphQL APIs**

GraphQL is a relatively new query language for APIs that is meant to make getting to data easier and more flexible. GraphQL APIs let clients tell the server exactly what data they need, and the server sends back only that data. This reduces the amount of data sent over the network and speeds up the service. GraphQL APIs are becoming more and more popular, especially for smartphone apps and single-page apps.

Here is an example of a GraphQL query and its corresponding response:

```json
query {
  user(id: "123") {
    name
    email
    posts {
      title
      body
    }
  }
}
```

With this GraphQL query, information about a person with the ID “123” is being asked for. It wants the user’s name, email address, and a list of their posts. It wants the title and body for each post.

**Response**

```json
{
  "data": {
    "user": {
      "name": "John Smith",
      "email": "john.smith@example.com",
      "posts": [
        {
          "title": "My First Post",
          "body": "This is the first post on my blog."
        },
        {
          "title": "Another Post",
          "body": "This is another post on my blog."
        }
      ]
    }
  }
}
```

The GraphQL response to this question would include both the user’s posts and the information that was asked for. In this case, it gives back an object with a data property that has an object that represents the person that was asked for. There are variables for the user’s name and email, as well as an array of posts. It has the title and text for each post, which is what the original query asked for.

## **WebSocket APIs**

WebSockets are a way for a client and a server to talk to each other in real time and in both directions. WebSocket APIs let clients share and receive data in real time, without polling or long-polling. WebSocket APIs are used in programmes like chat rooms, multiplayer games, and trading tools for the stock market.

Here’s an example of a WebSocket API using Node.js and the `ws`package: You can even try this in your machine. It takes less then 2 minutes.

Installation Steps

1. Open up your terminal/console.
    
2. Create a new directory for your project: `mkdir websocket-example`
    
3. Go to the directory: `cd websocket-example`
    
4. Install the `ws` package by running the following command: `npm install ws`
    

**Example Code**

```javascript
const WebSocket = require('ws');

const server = new WebSocket.Server({ port: 8080 });

server.on('connection', (socket) => {
  console.log('Client connected.');

  socket.send('Welcome to the WebSocket server!');

  socket.on('message', (message) => {
    console.log(`Received message: ${message}`);
    socket.send(`You sent '${message}'`);
  });

  socket.on('close', () => {
    console.log('Client disconnected.');
  });
});
```

This code sets up a simple WebSocket server in Node.js using the `ws`package. The server listens for connections on port `8080`. When a client connects, the server logs a message to the console and sends a welcome message to the client.

Whenever the client sends a message to the server, the server logs the message to the console and sends a response back to the client with the same message. When the client disconnects, the server logs a message to the console.

You can test this WebSocket server by opening up multiple browser tabs and connecting to `ws://`[`localhost:8080`](http://localhost:8080). Whenever you type a message in one tab, it should appear in all the other tabs.

## **gRPC APIs**

gRPC is an open-source, high-performance system for making APIs. Protocol Buffers are used as the serialisation format. gRPC APIs have features like two-way streaming, flow control, and calls that can block or not stop. They work especially well for cloud-native apps and microservices architectures.

Here is an example of a gRPC call and a Python code response:

```python
# Example gRPC request
import product_pb2
import product_pb2_grpc

# Set up a gRPC channel to the search service
channel = grpc.insecure_channel('localhost:50051')
stub = product_pb2_grpc.ProductSearchStub(channel)

# Create a search query
query = product_pb2.ProductQuery(
    query='running shoes',
    max_results=10,
)

# Send the search query as a gRPC request to the search service
response = stub.Search(query)

# Example gRPC response
for result in response.results:
    print(result.name)
    print(result.description)
    print(result.price)
```

In this example, the `ProductQuery` message is defined in a Protocol Buffers file (`product.proto`) and compiled into Python code using the `protoc`compiler. The gRPC channel is set up to connect to the search service running on [`localhost`](http://localhost) at port `50051`.

The client creates a `ProductQuery` message and sends it to the search service using the `Search` method defined in the `ProductSearch` service. The search service processes the query and returns a `ProductResult` message containing information about the products that match the user's query.

The client then processes the response by iterating over the `results` field of the `ProductSearchResponse` message and printing out information about each product.

Each type of API has its own pros and cons, and the best API to use will depend on the needs of the application or system being built. In the end, the goal of any API is to make it easy, safe, and quick for apps to talk to each other and share data.

![](https://miro.medium.com/v2/resize:fit:1400/1*67sGHAznn58ijZ4-urTHvg.jpeg align="left")

# **How APIs are essential?**

APIs are an important part of current software development because they let different apps talk to each other and make workflows more efficient. They give different systems a way to talk to each other, share data, and do work without anyone having to do it by hand.

One of the best things about APIs is that they make it easy for developers to make flexible, reusable apps that are easy to connect to other systems. This is especially important in the software world of today, where more and more applications are made up of smaller, specialised services that work together to make a whole answer.

APIs also let developers share features with other developers or third-party apps in a safe and controlled way. This lets developers build on top of current services, which speeds up innovation and shortens the time it takes to get a product to market.

Also, APIs can make workflows more efficient by automating jobs that used to be done by hand. For instance, an API could be used to automatically get data from one system and put it into another, so that a person wouldn’t have to do it by hand. This can save time, cut down on mistakes, and make things run more smoothly overall.

In conclusion, APIs are an important part of modern software development because they allow for modular, reusable applications, make it easier to build platforms and ecosystems, and automate tasks to make processes more efficient. They are one of the most important parts of many current software architectures and are necessary for making scalable, interoperable software systems.

# **How APIs are used by developers?**

APIs can be used in many different ways by developers, based on their needs and the use case. One common use case is to add new features by building on top of current APIs instead of starting from scratch. This method can save time and effort by letting writers use code and features that have already been written instead of starting from scratch.

For example, a developer making a mobile app might use an API from a social media platform to let users log in to the app using their social media account. This would let the app use the social media site’s login system instead of making its own from scratch.

APIs are also often used to connect different systems or services to each other. For instance, a developer could use an API from a payment gateway to handle money in their app. This would let the app accept payments from various sources without having to build its own payment processing system.

APIs can also be used to get info from other systems or services and change it. For example, a developer could use an API from a weather service to get information about the weather and show it in their app.

Overall, developers use APIs in many different ways to add new features, connect different systems and services, and get data from other sources and change it. By using APIs that already exist, developers can save time and effort, cut down on development costs, and make apps that are more stable and scalable.

# **APIs best practices**

When developing and implementing APIs, developers should follow a few best practises:

![](https://miro.medium.com/v2/resize:fit:1400/1*fu-5nPXfFt1nHpV-gQyI1w.jpeg align="left")

* **Consistent API Design:** The API should be made using consistent design concepts that make it easy to understand and use. This includes giving resources, endpoints, and parameters names that are clear and easy to understand, using standard HTTP verbs, and giving detailed instructions.
    
* **Scalability:** APIs should be built with scalability in mind to make sure they can handle more traffic and data without slowing down or going offline. This means making APIs with efficient methods, limiting the amount of data returned with each request, and caching answers when possible.
    
* **Security:** When designing APIs, you should keep security in mind and make sure they are safe from common risks like cross-site scripting (XSS), cross-site request forgery (CSRF), and injection attacks. This means putting in place authentication and permission systems like OAuth and encrypting data in transit with SSL.
    
* **Versioning:** APIs should be given a version number to make sure backward support and give developers a clear way to move to a new version when the API changes. This means that the API endpoint should have a version number, that changes between versions should be documented, and that older versions should be supported for an acceptable amount of time.
    
* **Handling errors:** APIs should give developers clear error messages and status numbers that explain what went wrong and how to fix it. This means setting up error codes and messages, using HTTP status codes to show whether a request was successful or not, and giving specific error messages when a request fails.
    
* **Performance:** APIs should be made with performance in mind, so they can reply to requests quickly and effectively. This means finding the best way to get and handle data, making the fewest number of requests possible, and caching and compressing data when it makes sense.
    
* **Testing:** APIs should be fully tested before they are released to make sure they work as planned and are free of bugs and security holes. This means making test suites that cover every possible scenario and edge case, as well as using automated testing tools to make sure the API is working properly.
    

By following these best practises, developers can make APIs that are easy to use, scalable, safe, and fast. These APIs can be used to build software systems that are strong and reliable.

**Conclusion:**

To sum it up, APIs are like the matchmakers of the software world, bringing different applications and systems together for a data-sharing love fest. Without them, it would be like trying to get a cat and a dog to have a conversation — not impossible, but definitely not pretty. APIs are like magic wands for developers. They can conjure up robust and scalable applications, save time and money, and make innovation happen faster than a rabbit in a hat. From RESTful APIs to gRPC APIs, it’s like a buffet of APIs — pick and choose what suits your taste buds!

As technology keeps evolving, APIs will become the new cool kids on the block. Businesses will be like, “Hey, API, can you do this for me?” and API will be like, “Sure thing, boss. I got you covered.” Hey there, you savvy reader! Have you ever thought about how you can use APIs to make your apps or services even more awesome? Or maybe you’re just daydreaming about all the wild and crazy innovations that could come from using APIs in your industry. Either way, let your imagination run wild and see where APIs can take you! Listen up, folks! Whether you’re a tech whiz, a boss babe, or just a curious cat, knowing your way around APIs can give you some serious street cred in the digital world.

Hey, hey, hey! Why settle for a boring answer when I can give you a cool one? So, why APIs, you ask? Well, why not? They’re like the sprinkles on top of your ice cream sundae — they make everything better! Oh boy, APIs are like glitter — they get everywhere and you can never quite get rid of them! It’s like having a personal assistant who saves you time and money while building apps.

Who needs a real assistant when you have technology? These APIs are like matchmakers for apps — they bring together even the most independent and stubborn architectures to create something beautiful and innovative. Hey, have you ever stopped to ponder about the magical world of APIs while scrolling through your phone or computer? It’s like a secret society of tech wizards working behind the scenes to make everything work seamlessly. Oh boy, this little guy gets around! You can find it everywhere, from your smartphone to your smart fridge. It’s like a digital ninja, sneaking into all your devices.

I hope you had a good chuckle reading the last bit of this article because I snuck in a joke just for you. Keep reading and don’t forget to show off those pearly whites! Well, unless you’re a clown. Then it’s the makeup.

***Thanks for reading my article. I will come up with more topics so stay tuned.***