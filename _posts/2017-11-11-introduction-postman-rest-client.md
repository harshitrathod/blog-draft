---
title: Introduction to Postman REST client
date: 2017-11-11T13:46:22+00:00
author: Harshit Rathod
layout: post
tags:
  - Postman
  - tutorial
---
> ### **Summary**
>
> The Postman is a feature rich REST client. Thousands of developers used it to browse, test and even documenting APIs. This post aims to provide basic information you need to start using Postman

### Introduction

Started in 2012 with the idea of REST client Postman has improved itself to support all the feature you need for API development and testing. According to officials in 2014, it has 3+ million active users. You can make HTTP requests like GET,  POST,  PUT,  DELETE from it. You can also perform automation test on your API using it. With monitoring feature, you can execute set of requests to check for its performance and response

It's available as a Chrome extension and native app build on The Electron. I recommended using the native app because Chrome extension will be deprecated soon.  You can download it from [here.](https://www.getpostman.com/apps) In this post, we will use service call [Postman Echo](https://docs.postman-echo.com/) to mock our API

&nbsp;

### Send your first request

Calling API from Postman is like a cakewalk. For simplicity, we will do a GET request to the server

{: .center}
![Screenshot of postman app while sending Request]({{ "/assets/img/postman/blog1.png" }})

  1. URL of API
  2. Request Type [GET, POST, PUT, DELETE]
  3. Send button To call the API
  4. Response Of API
  5. More information
  6. History of past API calls

##### Send Post data with Request:

{: .center}
![Post Request with Postman]({{ "/assets/img/postman/blogrequest.png" }})

While doing a POST request to the API you need to pass some data as a body. As given in the screenshot above, you can pass data while calling your API

{: .center}
![Post Request Response]({{ "/assets/img/postman/blogresonse.png" }})

### Collections

Postman provides good way to Organize your related request. It's called **Collections. **It's like folder structure so you can browse API. Also You can use collections with Test script but this will be explained later. You can create and browse Collection as displayed below

{: .center}
{% include image.html img="/assets/img/postman/createCollection1.png" title="Click New Button to Add Collection" caption="Click New Button to Add Collection" %}

{: .center}
{% include image.html img="/assets/img/postman/createcollection2.png" title="Provide Collection name and detail and then save Collection" caption="Provide Collection name and detail and then save Collection" %}

{: .center}
{% include image.html img="/assets/img/postman/createcollection3.png" title="Click On save button to add a request to the Collection" caption="Click On save button to add a request to the Collection" %}

{: .center}
{% include image.html img="/assets/img/postman/createcollection4.png" title="Add detail and select collection" caption="Add detail and select collection" %}

{: .center}
{% include image.html img="/assets/img/postman/createcollection5.png" title="Form collection tab you can access your Collections" caption="Form collection tab you can access your Collections" %}

### Example

When you have different frontend and backend team, REST API design is the most important part.  Frontend team doesn't want to refactor their code because of misunderstanding about API design. Postman solves this problem with the concept called **"Example".** You can save request/response parameter of your API as an Example. After saving your Example, You can share it with the team. You can also create a mock server with Postman mock server. frontend team can use it as an alternative to actual API

{: .center}
{% include image.html img="/assets/img/postman/e1.png" title="Click on Add Example" caption="Click on Add Example" %}

{: .center}
{% include image.html img="/assets/img/postman/e2.png" title="Add request and response detail" caption="Add request and response detail" %}

{: .center}
{% include image.html img="/assets/img/postman/e3.png" title="Access Example" caption="Access Example" %}

### Conclusion

**Postman **is a day to day tool for any developer.  Any backend developer can quickly check his API without any frontend application. Also, the developer can write test script which will help them to do impact analysis of their change on API. Frontend developer can use this as an alternative to actual API which will make them independent of backend team

&nbsp;

&nbsp;
