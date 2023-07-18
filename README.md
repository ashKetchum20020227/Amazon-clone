# Fakemazon (Full Stack Amazon-clone)

## Overview

The project was individually developed by myself (Chevva Ashish Reddy) using the MERN stack and vanilla CSS. It does not include code from any other repositories or users.

The main aim of the project was to demonstrate my MERN stack and CSS skills by recreating a design of a popular e-commerce website, showcasing my ability to develop a 
website based on a given design. The website is **responsive** and compatible with various devices.

The website's main functionalities are listed below and later discussed along with accompanying pictures:
1) User Registration and Login.
2) OTP-based authentication using the user's email.
3) Ability to change email, name, mobile and password. Email, mobile and password changes require OTP verification sent to the user's email.
4) Add and remove a product to cart.
5) Process cart checkout using Razorpay integration.
6) Order History.
7) Filter previous orders based on timeline (14 days, 1 month, 3 months, etc.)
8) Add, remove, edit multiple addresses.
9) Customer Care Chat Functionality. Executives are distinguished from customers in the database.
10) Video Chat integration for the hearing-disabled. This requires connecting customers with only executives who are free.


## Home page

<img width="1728" alt="Screenshot 2023-07-16 at 6 20 53 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/fe9b4271-5245-41e0-af41-b8cdb86c83d6">


# Functionalities

Discussed in the same order as mentioned above along with respective pictures in atleast 2 device formats.

## 1)  User Registration and Login, 2) OPT-based authentication

  
<img width="1728" alt="Screenshot 2023-07-14 at 7 22 07 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/3259a908-2638-4adc-ac74-a7c73c6fafe9">
<img width="544" alt="Screenshot 2023-07-14 at 7 22 53 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/c1f7d20f-c54e-4978-8b0a-e9d3660ff6d7">

During registration, an OTP is sent to the user's email. This was achieved using nodemailer. The OTP, along with the user's email, is stored in the database for verification 
purposes.

<img width="1728" alt="Screenshot 2023-07-14 at 8 28 18 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/4d018803-18f9-4e28-aef8-ca1cbd9ae008">

During login, the user's email and password are validated against the stored credentials in the database.

## 3) Change email, password and name

  The user has the power to change his name, email and password. To change his email or password, an OTP will be sent to his current email and the OTP is stored and verified
  as shown in the first functionality.
  
<img width="1728" alt="Screenshot 2023-07-14 at 7 44 10 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/ebe16b98-d77d-4103-81ff-065843a58122">
<img width="1728" alt="Screenshot 2023-07-14 at 8 27 32 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/93f5aa2e-a934-4dcc-890d-39630a30e5c2">

## 4) Add, remove products to/from cart

   The user has the ability to add items into cart by clicking on the add to cart button and also remove items from the cart page.
   
<img width="1728" alt="Screenshot 2023-07-14 at 7 24 41 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/82f33be1-c320-4f26-b094-321f51440f50">
<img width="1728" alt="Screenshot 2023-07-14 at 7 24 53 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/e66f3d79-6f04-49ff-9a90-33542a92a271">

## 5) Process cart checkout using Razorpay integration

   The user can checkout products currently in the cart by paying through UPI, card, etc. using Razorpay's checkout integration as shown:
   
<img width="1728" alt="Screenshot 2023-07-14 at 7 42 53 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/75e797dd-55e7-4c94-89f3-f6c5e66702d4">
<img width="1728" alt="Screenshot 2023-07-14 at 7 43 21 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/d0335092-ca03-4ec6-87fe-a1165205f83e">
<img width="1728" alt="Screenshot 2023-07-14 at 7 43 21 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/bf5a302b-891e-4b5e-a5e9-440f5830ee46">

  As seen in the image below, the checked-out order has been added to the database and is now visible in the Order History.

<img width="1728" alt="Screenshot 2023-07-14 at 7 43 38 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/416846c7-c4ac-46e0-a4d0-6969d44587a7">

  I am also attaching a screenshot of the database that the order has been stored. The orders are stored as an embedded document inside a user document.
  
<img width="1728" alt="Screenshot 2023-07-16 at 6 00 00 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/f931221d-9333-482d-a009-4c10290a3248">


## 6) Order History and 7) Filtering order history based on time

  All of the user's orders are stored in an embedded document as an array as shown in the image above. The products in a single order are coupled together. The orders can
  be filtered based on time just like in the original website.
  In the image below, I have selected the option 14 days, which only shows orders that were placed in the last 14 days. For the sake of continuity, the only order that     was placed in this account was the one placed above while showing a functionality. Other orders shown in the above image disappear when you select this option.
  
<img width="1728" alt="Screenshot 2023-07-14 at 7 43 57 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/16cd9ab4-4104-4e54-b5c8-1578fadfa461">

## 8) Add, remove, edit multiple addresses

   As in the original website, the user can add multiple addresses, make one of it the default address. He can also edit or remove his addresses.

<img width="1728" alt="Screenshot 2023-07-14 at 7 44 18 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/629e50f4-7158-4b59-a4ea-3983fe6b9a3f">
<img width="1728" alt="Screenshot 2023-07-14 at 7 44 24 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/c826490a-2537-404d-bbeb-bd249fdc9359">

## 9) Customer Care Chat Functionality

   A user can chat with a customer care executive. When he enters the chat page, he is directly connected to an executive that is online. The user, if disconnected can
   continue his chat from the previous session with the same executive. A feature can be added to delete the conversation after 24 hours.

<img width="1728" alt="Screenshot 2023-07-14 at 7 44 35 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/7f9ff8f4-3ed2-4e26-8022-646544d1180b">

The below image is from the user's account.
<img width="1728" alt="Screenshot 2023-07-14 at 7 45 14 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/c33b4749-c4a1-49d3-b595-ad1c734bcc28">

The below image is from the executive's account.
<img width="1728" alt="Screenshot 2023-07-14 at 7 45 41 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/e95c5344-9e15-45b0-8e97-36849cba0fb6">

## 10) Video Chat integration for the hearing-disabled. This requires connecting customers with only executives who are free

    As we all know, not all discrepancies are resolved via chat. We often find ourselves waiting on long holds with the customer care to solve our problem via a call.
    I was inspired from a movie which had video chat option where the executive was well-versed in sign language which helped many hearing-diabled people to solve their
    problmes.
    So I integrated video chat option that connects users to employees who are online and not already engaged in another call. I used a "free" variable that is updated
    whenever an executive enters and ends a call. CSS was not imparted to this page.

    As shown in the image below, the user is shown a list of all free executives and a button to call them
    
    <img width="1728" alt="Screenshot 2023-07-14 at 7 51 43 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/afb8d4b7-ee45-4115-be78-ba10691fc93d">
    <img width="1728" alt="Screenshot 2023-07-14 at 7 51 16 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/5c35ce95-f3e0-4232-97b9-3f7546661d23">


## Responsive Images

The below images showcase the responsiveness of the website in various devices.

<img width="1728" alt="Screenshot 2023-07-16 at 6 21 34 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/3193e7ea-88d6-4f9e-9fa0-c36f761eabbb">

<img width="1728" alt="Screenshot 2023-07-16 at 6 21 43 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/38e72a02-401b-407c-b842-68e3d9de93cc">

<img width="1728" alt="Screenshot 2023-07-16 at 6 21 53 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/f7cd3b7a-3cc1-4c74-be5d-bee2113280e5">

<img width="1728" alt="Screenshot 2023-07-16 at 6 22 02 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/e515a21f-415c-4289-aa33-15a7f1b093db">

<img width="1728" alt="Screenshot 2023-07-16 at 6 22 12 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/c7016b61-6b10-4437-9e82-cd90953fbd5f">

<img width="1728" alt="Screenshot 2023-07-16 at 6 23 32 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/bdce9a83-c17c-4600-98dd-6a52937c0731">

<img width="1728" alt="Screenshot 2023-07-16 at 6 23 37 PM" src="https://github.com/ashKetchum20020227/Amazon-clone/assets/135194797/a60abcd0-3476-47e4-8522-7917bbfd471a">



  


   

   
  
