# Greentree Tracker

Coder Academy T3A1 Full Stack App (Part B) assessment

Created by Tyler Hall and Katrina Marquez 

### Purpose 

Greentree Tracker is an inventory and order management solution designed for small to medium wholesale nursery businesses. 

The key issues small to medium sized wholesale nurseries currently face is finding software that is simple to use and includes product classification fields specific for inventory found in nurseries.

Greentree Tracker worked in collaboration with a wholesale nursery in Queensland to develop a solution that is simple and easy to use with a twist. The solution provides additional functionality for customers to view and select items and request a final quotation from the nursery. 

Greentree Tracker's focus is to reduce the amount of software small to medium wholesale nurseries are required to set up and manage by combining inventory and sales function in one solution. 

### Functionality/Features 

**User Authentication**

Users are able to register for an account with Greentree Tracker, which will enable them to make a quote request to the wholesaler. Users are able to sign in using their registered email address and password. Once signed in, they will be able to edit their information on their account page, changing their password and client information.

**Authorisation**

Authorisation will be implemented to restrict the CRUD functionality to the Admin. Users accounts will have a different role to the Business, which will have the only Admin role. The Admin will be able to add, update and delete plant listings, and every user role will be able to read all components and content of the application. Authorisation will also restrict regular browsers from placing a quote request to the business, and will be prompted to sign in first. This will ensure that the business will only be dealing with accredited users.

**Admin CRUD Functionality**

Admin will have the ability to create new plant listings, update existing plants, and delete any or all plant listings. As mentioned previously, these functions will be limited only to users with the Admin role.

**Image Upload**

Image upload will be implemented to allow the Admin to post photos with plant listings. These will be stored with Amazon S3 cloud storage services, which will allow for multiple images to be hosted online for easy accessibility. If no image is uploaded, a stock image will be assigned to the plants.

**Quote Request**

The main functionality of Greentree Tracker is to allow users to make a quote request for a variety of plants from the wholesaler. Inventory can be a tricky component of Nurseries, as although the plants may be in location, they may not always be available for sale due to a number of reasons (bugs, plant quality etc). The quote request feature is provided for users to select multiple plants they wish to purchase, which can be sent to the business as well as a comment and also their contact information. The business will be able to access these quote requests through their admin dashboard, and subsequently can respond to each individual request with an informed response of their stock.

**Inventory Management**

As mentioned in the feature for Quote Request, inventory available for sale might not actually be ready for purchase due to plant conditions. The concept of remaining stock is to indicate if the nursery still has the plant available for purchase pending nursery confirmation from the stock. Admin accounts will have the functionality to add in *'remaining stock'* of a particular plant.
### Target Audience 

The target audience for Greetree Tracker is small to medium wholesale nurseries. Wholesale nuseries operate with a B2B (Business to Business) model rather than B2C (Business to Customer).

### Tech Stack

- MongoDB
- Express.js
- React.js
- Node.js
- Git

React Dependencies:

- Material UI
- Axios
- React-dom
- React-router-dom
- Cypress
- React Testing Library
- AWS S3
- Dotenv
- React-alice-carosel


Express Dependencies:

- Body-parser
- Connect-mongo
- Cors
- Dotenv
- Express
- Express-session
- Mongoose
- Mongoose-bcrypt
- Nodemon
- Passport
- Passport-local
- Passport-local-mongoose
- Jest
- Supertest.js

Third Party Services:

- GitHub
- Netlify
- Heroku
- AWS S3

### Dataflow Diagram
![Dataflow Diagram](Resources/greentree-tracker-dfd.png)
### Application Architecture Diagram

![Greentree Tracker Application Architecture Diagram](Resources/application-architecture-diagram.png)

### User Stories 

**Users**

The table below identifies the types of users in small to medium wholesale nursery businesses. Each users experience with Greentree Tracker is grouped according to their 'access type' in the application.  

![Greentree Tracker Users](Resources/users-summary.png)

**User Story - Business**

Business users is Greentree Tracker's name for administrators. In a small to medium sized nursery business, this will cover business owners, managers and all other staff working in the business. 

*a. Create an account with Greentree Tracker*
- The client requires only one administration accounts to be set up for the business. 

*b. First view of website*

Options showing to users on this page:
- Create a plant listing
- View list all plants listed in alphabetical order
- Contact us page

*d. Creating a plant*

Information that may be entered includes:
- botanical name;
- common name; 
- description; 
- price;
- pot size; 
- special; and
- category name. 

*e. Editing or deleting a plant and adding number of inventory in stock*

Editing a plant:
- All fields mentioned in (d) can be edited
- A field called inventory is attached to the specific plant where the business user can add the quantity in stock

Business users have the option to delete the plant listing. 

*f. View list of orders* 
- List of orders from all customers

*g. View list of all plants*
- Buisness is able to see full list of plant listings with a section to sort listings according to types of plant (i.e. shrub, tree, ground cover and grass)

**User Story - Customer**

*a. Customer creates an account on Greentree Tracker*
- Greentree Tracker requires users who want to purchase plants to create an account.

*b. First view of website*

Options showing to users on this page:
- View list all plants listed in alphabetical order
- Contact us page

*c. View list of all plants for sale*
- Customer can view all plant listings

*d. View details of a specific plant*

Customers are able to click on a specific plant they are interested in and view more details about the plant.The following details will be avaliable on the page:
- botanical name;
- common name; 
- description; 
- price;
- pot size; 
- special; and
- category name. 

*e. Customer wants to add plant to cart for order request*
- Customer is able to add the plant to the quote
- Cart on the page is updated to include item

*f. Customer is able to see requested quote to the nursery and complete the order*
- Customer is able to see a summary of quality, types of plants ordered
- Customer can enter thier name
- Customer can enter their business name
- Customer can enter thier billing address
- Customer is able to add any additional comments 

*g. Customer is able to edit their account information*
- Customer is able to change their user name, password, business, ABN and email

**User Story - Guest**

*a. First view of website*

Options showing to users on this page:
- View list all plants listed in alphabetical order
- Contact us page

*b. View list of all plants for sale*
- Guest can view all plant listings

*c. View details of a specific plant*

Guests are able to click on a specific plant they are interested in and view more details about the plant.The following details will be avaliable on the page:
- botanical name;
- common name; 
- description; 
- price;
- pot size; 
- special; and
- category name. 

*d. Guest is prompted to create a customer account*
- Greentree Tracker requires users who want to purchase plants to create an account.
### Wireframes 

#### **Home**

![Home Page Wireframe](Resources/home-page.png)

#### **Login**

![Login Page Wireframe](Resources/login-page.png)

#### **Register**

![Register Page Wireframe](Resources/register-page.png)

#### **User Account**

![User Account Page Wireframe](Resources/user-account-page.png)

#### **Plants**

![Plants Page Wireframe](Resources/plants-page.png)

#### **Plants Show**

![Plants Show Page Wireframe](Resources/plants-show-page.png)

#### **Plants Edit**

![Plants Edit Page Wireframe](Resources/plants-edit-page.png)

#### **Quote Request**

![Quote Request Page Wireframe](Resources/quote-request-page.png)

#### **Contact**

![Contact Page Wireframe](Resources/contact-page.png)

#### **Admin Dashboard**

![Admin Dashboard Page Wireframe](Resources/admin-dashboard-page.png)

### Screenshots

Trello was used as the project management for T3A2 Full Stack App (Part A). 

*Monday, 23 November 2020*
![Trello 23 Nov 2020](Resources/trello-board-23112020.png)

*Tuesday, 24 November 2020*
![Trello 24 Nov 2020](Resources/trello-board-24112020.png)

*Wednesday, 25 November 2020*
![Trello 24 Nov 2020](Resources/trello-board-25112020.png)

*Friday, 27 November 2020*
![Trello 27 Nov 2020](Resources/trello-board-27112020.png)

*Tuesday, 8 December 2020*
![Trello 8 December 2020](Resources/trello-board-8122020.png)