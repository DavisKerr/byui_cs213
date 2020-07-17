# CS 213 Web Engineering 1 Final Exam Study Guide

##### Table of Contents  
[OSI Stack](#OSI-Stack)  
[TCP IP](#TCP-IP)  
[Client Side](#Client-Side)  
[Server Side](#Server-Side)  

## OSI Stack

Understand the levels of the OSI stack and pay close attention to those first few layers that you've been mainly focused on in class. HTTP is a good thing to study (GET, POST, PUT, DELETE). Think about the layers in the stack. For example where TCP/IP is at in the stack in relation to HTTP.

[ISO Stack Reference](https://www.lifewire.com/osi-model-reference-guide-816289)

#### What is an OSI Stack:
- stands for Open Systems Interconnection.
- It is a model for how systems should connect and interact with each other. 
- Divides internetworking into Layers
- Layer 1:
  * 7 Application
  * 6 Presentation
  * 5 Session
- Layer 1 Explained: Handles applicaion specific reqiurements like HTTP, FTP, SSL, etc
- Layer 2:
  * 4 Transport (TCP/IP)
  * 3 Network
  * 2 Data Link
  * 1 Physical
  - Layer 2 explained: Handles primitive netweorking like routing, addressing, and flow control like TCP, IP, USB, bluetoooth, etc
- Layers work from physical and up. (see number ordering, ascending)

#### What is HTTP
- Stands for Hypertext transfer Protocol
- Works in layer one of OSI Stacks, in the application layer, after network communications are established. 
- It facilitates the fetching of resources from servers connected to the Web. 
- The browser (client) always initiates the http request. 
- HTTP is stateless, but not sessionless
- HTTP is controlled at the transport layer
- HTTP sequencing:
  1. Open a TCP connection.
  2. Send HTTP message.
  3. Read the responce sent by ther server.
  4. Close or reuse connection.

#### What are GET POST PUT and DELETE
- GET requests retrieve data froma  server at a specified resource. It is the most common use, and does not modify data.
- POST requests send data to the server to create or update a resource. 
- PUT is the same as POST except it always produces the same result.
- DELETE removes a resource at the specified URL

## TCP IP

**IPv4** (32 bits) vs **IPv6** (128 bits)

See: [IPv4 vs IPv6](https://www.juniper.net/us/en/products-services/what-is/ipv4-vs-ipv6/)

## Stylesheets

Precedence of stylesheets (internal vs external)

## Client Side

### JavaScript
Study up on the differences between PHP (server side) and JavaScript (client side). What are the major differences between the two languages and their appropriate domains?

Dynamics of a JavaScript function:

```js
  /**
   * Sum up the values in foo
   */
  function processFoo(foo) {
    // preprocessing logic goes here
    return foo.a + foo.b + foo.c;
  }
```

What exactly gets passed into the function above if it's setup as follows:

```js
  let foo = {
    a: 2,
    b: 4,
    c: 8
  }
  
  console.log(`The sum of foo is: ${processFoo(foo)}`);
```

### CSS

Having an understanding of CSS selectors is important to developing well structured and aesthetically appealing web pages. Review this spec:

(CSS Selectors)[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors]

Know what the following code is doing:

```css
@media only screen and (max-width: 480px) {
  p {
    font-family: serif;
  }
  body {
    background-color: lightgray;
  }
}
```

What is the major difference between the previous media query and this one:

```css
@media only screen and (min-width: 200px) and (max-width: 767px)  {
  p {
    font-family: serif;
  }
  body {
    background-color: lightgray;
  }
}
```

Test out this code in your browser. Create an HTML file with a body and some paragraph with text then use the Chrome browsers responsive view to see the differences.

[Testing Media Queries with Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/device-mode)

Understand what a ***viewport*** is and what it does.

Understand how search engine optimization is implemented. When the Google web crawler goes through your web code what is it doing and how does it factor in your web elements for it's own search engine algorithm? Hint: think about your page headers, title, and meta tags.

Understand how the following are effectively used on a web page: proximity, contrast, alignment, repetition.

What's the main difference between these two web elements?

```html
<input type="submit" value="Submit">
```

```html
<input type="button" value="Submit">
```

Hint: [HTML web forms with submit](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_form_submit)

### HTTP routing

When a form is submitted what goes on the query string?

Here is a good example of setting this up in HTML:

[HTML GET query string](https://youtu.be/RkFswrkkie8)

This video breaks down the backend and frontend interactions of HTTP requests. Review the differences between a GET and a POST request.

[The logic behind query strings](https://youtu.be/576WwU7xlWU)

### Document Object Model (DOM)

Review how to select elements from the DOM.

Recall that Mozilla has a really great website that covers the DOM in depth. Review this spec:

[Document](https://developer.mozilla.org/en-US/docs/Web/API/Document)

## Server Side

Have an understanding of various PHP functions and routines. Know how to open a file and read in the data. Read up on W3 schools for a bunch of examples and try some out on your Linux lab accounts for review.

Review how to print out some variables in PHP.
Say I have:

```php
$hello = hello
$world = world
```

From those variables how would I be able to produce:

"hello world"

How about

"hello my world in this galaxy"

Think about how JavaScript AJAX requests interact with PHP. Here is a phenomenal example of an AJAX fulfilled request between JS (client side) and PHP (server side):

[JS and PHP AJAX fulfillment](https://www.w3schools.com/php/php_ajax_php.asp)

Have an understanding of arrays in PHP. How are arrays assigned and data read from an array in PHP.


