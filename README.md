# **What You Need** :seedling:

![Mockup](documentation/mockup/mockup.png)

**What You Need** is an e-commerce web application that propose a range of indoor and outdoor plants to make your home or office healthier and a bit more special.  
This project is build with growth in mind and offer opportunities to add and improve features as the business develops.

For this project the use of Stripe's test functionality is implemented, rather than actual live payments.
You can make test payment with the following details:

| NUMBER                | BRAND            | CVC          | DATE            |
| --------------------- |----------------- | ------------ | --------------- |
| 4242424242424242      | Visa             | Any 3 digits | Any future date |
| 5555555555554444      | Mastercard       | Any 3 digits | Any future date |
| 378282246310005       | American Express | Any 4 digits | Any future date |

Visit the live Website : **[WEBSITE NAME :arrow_right:](https://WEBSITE-NAME.herokuapp.com/)**

## Table of Content

* [Project](#Project)
  * [Project Goals](#Project-Goals)
  * [Developer and Business Goals](#Developer-and-Business-Goals)
  * [User Goals](#User-Goals)
* [UX](#UX)
  * [Audience Definition](#Audience-Definition)
  * [User Stories](#User-Stories)
  * [Design Choices](#Design-Choices)
  * [Wireframes](#Wireframes)
  * [Different Design](#Different-Design)
* [Features](#Features)
* [Future features to implement](#Future-features-to-implement)
* [Flowchart](#Flowchart)
* [Database](#Database)
  * [Database Design](#Database-Design)
* [Code Structure/Organisation](#Code-Structure/Organisation)
* [Technologies Used](#Technologies-Used)
* [Testing](#Testing) [:fast_forward: TESTING.md](TESTING.md)
* [Deployment](#Deployment) [:fast_forward: DEPLOYMENT.md](DEPLOYMENT.md)
  * [Get Started](DEPLOYMENT.md#Get-Started)
    * [Cloning](DEPLOYMENT.md#Cloning)
    * [Forking](DEPLOYMENT.md#Forking)
    * [Installations and dependencies](DEPLOYMENT.md#Installations-and-dependencies)
  * [Live Deployment](DEPLOYMENT.md#Live-Deployment)
    * [Create the Heroku app](DEPLOYMENT.md#Create-the-Heroku-app)
    * [Set up AWS s3 to host our static files and images](DEPLOYMENT.md#Set-up-AWS-s3-to-host-our-static-files-and-images)
    * [Connect Django to s3](DEPLOYMENT.md#Connect-Django-to-s3)
    * [Add Media folder to our bucket](DEPLOYMENT.md#Add-Media-folder-to-our-bucket)
    * [Final Steps](DEPLOYMENT.md#Final-Steps)
* [Bugs](#Bugs)
* [Credits](#Credits)
  * [Content](#Content)
  * [Acknowledgements](#Aknowledgements)

## Project

### Project Goals

What You Need is an MVP build for educational purposes that promotes green and healthy homes and offices.

In this year 2022 we can observe a shift in lifestyles needs and organisation. People that use to spend most of their time at work, now work part or full-time from home. And in general people are more aware of their direct environment.

One of today's challenges is mental health. People are more conscious about it, and they are looking for ways to improve their mental health. They want to feel good or better about themselves and about what they do.

Research prove that plants and natural elements provide a positive impact on people increasing well-being and productivity.  
This creates a market opportunity for helping customers improving their workspace and home. At the same time, the e-commerce market is expanding with more people using the web to get what they need every day.

In response to this demand, **What You Need** online shop offers a wide variety of plants. From the most delicate plants to the most indestructible. Customer can browse the website catalog by sorting or searching for specific categories, deals and plants.  
Registered and logged in customer will benefit of the full functionalities of the website including save items into a wishlist, ratings products and leaving reviews as well as reviewing their past order and making request about an order with ease and confidence. Registered customer will have exclusive access to specially selected plants. So get what you need today!

As a site owner you can manage your products. You can add, delete and update products. You have the option to make a product on sale, and it will be populated added to the relevant category. As well the availability of stock is automated and products will be available to buy only if in stock. The product management page will display the products out of stock as well as the products within that reach a critical stock in order for you to keep track of your inventory and place an order if necessary.

### Developer and Business Goals

* Develop a viable e-commerce web application.
* Provide a user-friendly interface.
* Provide an amazing user-experience across multiple device sizes.
* Improve Wellness and health.

### User Goals

* Easy to use application.
* Getting clear information.
* Quick access to products.
* Buy plants for their homes or offices.

[**:back:** *Table of Content*](#Table-of-Content)

## UX

### Audience definition

1. The primary targeted audience is very broad and address all **online customers**.
2. The secondary targeted audience is **Corporates or Businesses**.

Both targeted audience are looking for plants to buy for their home, office(s) or business. They can be considered as one. The difference will reside in the quantity needed. This is managed with specials deals category for larger orders.

### User stories

#### Customer stories

##### Website navigation and browsing

1. As a user, I want a user-friendly, simple and interactive website.
2. As a user, I want to be able to access the website on different devices with the same experience.
3. As a user, I want to find out what is the website purposes.
4. As a user, I want to search products by category.
5. As a user, I want to search for specific products.
6. As a user, I want to see more details about a product.

##### Shopping experience

1. As a customer, I want to easily identify what is the price of the product.
2. As a customer, I want to easily identify if the product is available.
3. As a customer, I want to add/remove/edit product(s) in my shopping bag.
4. As a customer, I want to easily access my shopping bag.
5. As a customer, I want to make a purchase.
6. As a customer, I want the purchase process to be easy and secure.
7. As a customer, I want to be notified of the purchase I have made and be provided with a receipt.
8. As a customer, I want to contact the website owner about a past order.

##### Sign-in and registration

1. As a user, I want to create an account.
2. As registered user, I want to sign-in and sign-out easily.
3. As registered user, I want to change my password if forgotten or not safe anymore.
4. As signed-in user, I want to save/update information to my profile for a better and easier experience.
5. As signed-in user, I want to save products I like for a future purchase.
6. As signed-in user, I want to see/edit my wishlist.
7. As signed-in user, I want to access my previous orders.
8. As signed-in user, I want to leave a review on a product.

#### Site owner/Admin stories

1. As an Admin, I want to add/edit/delete products.
2. As an Admin, I want to see orders.
3. As an Admin, I want to manage customer queries.

[**:back:** *Table of Content*](#Table-of-Content)

### Design Choices

The approach concerning design choices is that the UX (User experience) should be the same across all platform and devices. Consistency being a key factor for UX.  
For this reason the UI (User Interface) is kept the same across different device sizes. This does not exclude the consideration for any extra or different features, should it improve the user experience.

#### Fonts

Considering the targeted audience, the sans serif type of font is the more appropriate because it is most often associated with simplicity and straightforwardness.  

The website will use well known and popular font that are used online in order to bring to the user a "feeling of knowing".

* *Poppins* for headings.

* *Lato* for main content.

*Sans serif* will be use as a fall back if the fonts do not load. It is common as the main typographies are sans serif type.

#### Icons

* Some Font Awesome icons will be part of the website for better UX.
* The [logo](documentation/logo/logo.jpg) and [favicon](documentation/favicon/favicon.ico) are the same image and use the color scheme of the website.

![logo](documentation/logo/logo.jpg)

#### Colors

![Color palette](documentation/colour-scheme/colours-theme.png)

The colours chosen for the website are simple and joyful. They are based on the psychology behind colours ([colour affects](http://www.colour-affects.co.uk/psychological-properties-of-colours), [London Image Institute](https://londonimageinstitute.com/how-to-empower-yourself-with-color-psychology/)).

[Adobe Color](https://color.adobe.com) was used to build the colour scheme, compatibility and accessibility. The color scheme and swatches are said color-blind safe.

![Color accessibility](documentation/colour-scheme/colours-accessibility.png)

#### Images

The images will be the one uploaded by website owner and/or Admin for products descriptions and website illustrations.  

#### Styling/Feeling

The feel of the website is welcoming and simple to provide a quick access and learning process.  
It makes users comfortable.

#### Audio/Video

No audio or video will be integrated at the moment.

[**:back:** *Table of Content*](#Table-of-Content)

### Wireframes

![Site map](documentation/wireframes/site-map.png)

* [Home page](documentation/wireframes/home.pdf)
* [About page](documentation/wireframes/about.pdf)
* [Contact page](documentation/wireframes/contact.pdf)
* [Terms and Conditions of use page](documentation/wireframes/t-c.pdf)
* [Sign-in page](documentation/wireframes/signin.pdf)
* [create an account page](documentation/wireframes/create-account.pdf)
* [Products page](documentation/wireframes/products.pdf)
* [Product details page](documentation/wireframes/product-details.pdf)
* [Search page](documentation/wireframes/search.pdf)
* [Orders history page](documentation/wireframes/orders-history.pdf)
* [Order details page](documentation/wireframes/order-details.pdf)
* [Order issue page](documentation/wireframes/order-issue.pdf)
* [Account details page](documentation/wireframes/account-details.pdf)
* [Wishlist page](documentation/wireframes/wishlist.pdf)
* [Bag page](documentation/wireframes/bag.pdf)
* [Checkout page](documentation/wireframes/checkout.pdf)
* [Add product page](documentation/wireframes/add-product.pdf)
* [Add category page](documentation/wireframes/add-category.pdf)
* [Error page](documentation/wireframes/error-page.pdf)

For the full version:

* [website name](documentation/wireframes/.pdf)

[**:back:** *Table of Content*](#Table-of-Content)

### Different design


[**:back:** *Table of Content*](#Table-of-Content)

## Features

To build this project, I use Django framework with the Django templating language. For consistency across the website some features will be repeated and functionality will be kept as simple and direct as possible.

* Navigation is always present and fix at the bottom of the page on small screen and fix at the top of the page on large screen.
  * Home
  * Account/profile
  * Bag
  * Search

[**:back:** *Table of Content*](#Table-of-Content)

## Future features to implement


## Flowchart

![Website flowchart](documentation/data-design/flowchart.png)

[**:back:** *Table of Content*](#Table-of-Content)

## Database

### Database design

The database design used is a relational database.

* During **development**, sqlite3 was used. It is the database provided by Django and only use for development.
* For **Production**, Postgres is used. It is the database provided by Heroku when deploying the website live.

Below is a representation of the database used for this project.
![Database Design](documentation/data-design/updated-db-design.png)

### Database Structure

Django, the framework used for the production of this project, is an MVP: Model View Product. This means that the project build with Django is divided in multiple apps. Its structure allows separation of concern and provide many built-in features.  
The models define the data-structure.

* In this project, the following models have been developed:
  * User (being a "default" model provided by Django and allauth)

#### Models relationship

## Technologies Used

### Programming Languages

This project was developed using:

* HTML
* CSS
* JavaScript
* Python
* Jinja templating language.

### Frameworks, Libraries and Programs

* [Django](https://www.djangoproject.com/)  
Framework used to develop the website.

* [Balsamiq](https://balsamiq.com/wireframes/)  
For creating wireframes.

* [Lucichart](https://www.lucidchart.com/)  
For producing the flowchart and database design.

* [Google Fonts](https://fonts.google.com/)  
For importing fonts.

* [favicon.io](https://favicon.io/favicon-converter/)  
For generating the favicon.

* [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/)  
For resizing all the images.

* [BeFunky](https://www.befunky.com/create/)
For cropping some images.

* [Adobe Color](https://color.adobe.com/create/image)  
For extracting the color scheme used on the website.

* [Am I Responsive?](http://ami.responsivedesign.is/?url=http://ami.responsivedesign.is/#)  
For providing screenshots of the responsiveness of the website across several devices.

* [Autoprefixer CSS online](https://autoprefixer.github.io/)  
For adding prefixer in style.css for cross browser compatibility.

* [cdnjs](https://cdnjs.com/libraries/jquery-cookie)  
For jQuery cookie

* [Git](https://git-scm.com/)  
For Version control.

* [GitPod](https://www.gitpod.io/)  
For Integrated Development Environment.

* [GitHub](https://github.com/)  
For hosting the repository.

* [Heroku](https://www.heroku.com/home)  
For deploying the website live.

[**:back:** *Table of Content*](#Table-of-Content)

## Testing

Testing information are published in a separate file for better readability.
Please see [TESTING.md](TESTING.md).

## Deployment

Deployment information are published in a separate file for better readability.  
Please see [DEPLOYMENT.md](DEPLOYMENT.md)

This project is developed on [Gitpod Workspaces IDE](https://www.gitpod.io/) (Integrated Development Environment) committed and pushed to [GitHub](https://github.com), to [my Repository](https://github.com/Tom-Nagy/what-you-need) using Gitpod Command Line Interface (CLI) with [Git version control](https://git-scm.com/).

The project is deployed on Heroku using Postgres database and linked to s3 bucket cloud service on AWS (Amazon Wed Services) for hosting the media and image files.

### Deployment content

* [DEPLOYMENT.md](DEPLOYMENT.md)
  * [Get Started](DEPLOYMENT.md#Get-Started)
    * [Cloning](DEPLOYMENT.md#Cloning)
    * [Forking](DEPLOYMENT.md#Forking)
    * [Installations and dependencies](DEPLOYMENT.md#Installations-and-dependencies)
  * [Live Deployment](DEPLOYMENT.md#Live-Deployment)
    * [Create the Heroku app](DEPLOYMENT.md#Create-the-Heroku-app)
    * [Set up AWS s3 to host our static files and images](DEPLOYMENT.md#Set-up-AWS-s3-to-host-our-static-files-and-images)
    * [Connect Django to s3](DEPLOYMENT.md#Connect-Django-to-s3)
    * [Add Media folder to our bucket](DEPLOYMENT.md#Add-Media-folder-to-our-bucket)
    * [Final Steps](DEPLOYMENT.md#Final-Steps)

## Bugs

## Credits

### Code

### Content

[W3schools](https://www.w3schools.com/)  

[W3docs](https://www.w3docs.com/)

[stack overflow](https://stackoverflow.com/)

[GeeksforGeeks](https://www.geeksforgeeks.org/)

[Net Lawman](https://www.netlawman.co.uk/d/website-privacy-policy)  
For privacy policy template.

### Acknowledgements



[**:back:** *Table of Content*](#Table-of-Content)
