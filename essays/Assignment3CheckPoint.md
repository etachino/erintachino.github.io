---
layout: essay
type: essay
title: "Check Point for Assignment 3"
# All dates must be YYYY-MM-DD format!
date: 2022-11-30
published: true
labels:
  - Check Point for Assignment 3
---

<p> Show what each page will look like. The pages do not have to be “functional” but the design should clear. </p>
  [Click here to view screencast of diagram](https://youtu.be/a72-sQLSQEg)
 
<p> Describe your design for your site’s shopping cart. That is, will it be a separate page that the user can view and edit, or will it be integrated into the product pages? If so, describe in detail how this will work on your site. Provide several examples of using the cart. </p>
  For my site's shopping cart I was thinking of doing a pop out of the cart so that a user can see what is in their cart. Then I have two buttons, one that says “check out” and the other saying “view cart”. The checkout button will take the user to the login page if the user has not logged in. After logging in the user will be taken back to the previous product page they were at. If the user is logged in then they will be taken to the invoice once hitting check out. On the view cart page the user will be able to edit the cart. Once the user has edited their cart they will be redirected to the login page or invoice depending on whether or not they are logged in. 
  
<p>Explain specifically how you will use sessions to manage your shopping cart. In particular, what shopping cart data will be stored in the session, what data format will be used (NOT what data type, but the format like with the data format used for your registration data). Use code examples showing what data structures (such as arrays and their objects) you will use to manage the shopping cart data and how they will be used in a session.</p>
	The shopping cart data will be stored in the session ID of the user so that if they leave the page all items will be held. For my IR I will have it if the user is logged in but they leave the page the login will hold for (5minutes - using maxAge) and the user will be taken back to the product page/product they were last on. I will execute this using an array format to hold the products that were added from different product pages. To store the session data I would use a code that would look something like this:
 // Save data to the current session's store
sessionStorage.setItem("username", "John"); 
// Access some stored data 
alert( "username = " + sessionStorage.getItem("username"));
This example is for their user account. I would do something similar for the products that they have in their cart and create some type of array that will have the product quantity and which type of product. 
 
<p>How will you avoid access to your application when the user has not logged in or registered? What are the particular security concerns you must address?</p>
	The way that I will avoid access to my application when a user has not logged or registered is to have it redirect them to the login page, where they will have the option to register if they have no account. This will not allow them to move any further than the products display pages until they have logged in or registered. I will also use cookies to avoid access any farther than my products display page. Using cookies allows the server to validate if the user has cookies and if so they will be able to hit the checkout and get sent to the invoice. If there are no cookies of this user then they will be sent to the register page. The main security concern with cookies is that cookies can be edited or manipulated by a malicious attacker. 

<p>Upon a successful login, how do you provide personalization in your UI? Explain how you did or will do this (paste code if necessary)</p>
	The way that I will provide personalization after the user has successfully logged in is by using the user_data stored from the cookies. So the cookies will allow me to display whichever users email on the invoice page. I will also have the cookies set up to display the user's email in the cart so instead of “you” it will have the user's email saying, “user has this many items in cart”. Lastly I will have the users email displayed on the thank you for purchasing page. 
	
<p>If you are working with partners, how will you split up the work in your team so that you are working in parallel as effectively as possible? That is, who is doing what and when?</p>
	I am not working with a partner for this Assignment 3.
  
<p>How are you approaching Assignment 3 differently than Assignment 2?</p>
	The way that I am going to approach this assignment differently than assignment 2 is mapping. The diagram was really helpful for me to start the layout of Assignment 3 and how I want things to flow when the user is hitting certain buttons. I will also be making sure that my code can run using nodemon instead of node so that it will be easier to edit and test. I will also figure out the bigger issues than working on small bugs. By getting the bigger issues out of the way it will allow me to move forward within my assignment. I am also planning to map out how I want my server to look since I need to transfer most of my html pages to my server. This will allow me not to get so confused when transferring the different pages. 
