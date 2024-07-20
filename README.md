# Restaurant Chatbot with MongoDB Localhost Database

## Description

This repository contains the code for a restaurant chatbot that leverages a MongoDB localhost database to manage and retrieve information about the restaurant's menu, bookings, and other interactions. The chatbot is designed to provide an efficient and user-friendly interface for customers to interact with the restaurant, making reservations, browsing the menu, and getting answers to frequently asked questions.

## Features

- **Menu Management**: The chatbot can display the restaurant's menu items, including descriptions, prices, and special dietary information.
- **Booking System**: Users can make reservations through the chatbot. The system checks availability and confirms bookings in real-time.
- **Order Placement**: Customers can place orders directly through the chatbot for both dine-in and takeaway.
- **Interactive Conversations**: The chatbot can handle various customer inquiries, providing information about the restaurant's opening hours, location, special events, and more.
- **User-Friendly Interface**: Designed to be intuitive, making it easy for users to interact with the restaurant.

## Technologies Used

- **Python**: The primary programming language for the chatbot.
- **MongoDB**: Used as the database to store menu items, booking details, and other relevant information.
- **Flask**: A lightweight WSGI web application framework used to build the web interface.
- **Natural Language Processing (NLP)**: Implemented for understanding and processing user inputs.

## Setup Instructions

1. **Clone the Repository**:
   cd restaurant-chatbot

2. **Install Dependencies**:
   pip install -r requirements.txt

3. **Setup MongoDB**:
   - Ensure MongoDB is installed and running on your local machine.
   - Create a database named `restaurant_db` and collections for `menu_items`, `bookings`, and `interactions`.

4. **Configure Environment Variables**:
   Create a `.env` file in the root directory and add the following:
   MONGODB_URI=mongodb://localhost:27017/restaurant_db
   FLASK_APP=app.py
   FLASK_ENV=development

5. **Run the Application**:
   flask run

6. **Access the Chatbot**:
   Open your browser and navigate to `http://127.0.0.1:5000/` to start interacting with the chatbot.

## Database Schema

### Menu Items

{
   "item_id": "unique identifier",
   "name": "string",
   "description": "string",
   "price": "float",
   "dietary_information": ["vegan", "gluten-free", etc.]
}

### Bookings
{
   "booking_id": "unique identifier",
   "user_name": "string",
   "date": "date",
   "time": "time",
   "number_of_people": "int",
   "contact_details": "string"
}


### Interactions
{
   "interaction_id": "unique identifier",
   "user_query": "string",
   "response": "string",
   "timestamp": "date"
}


## Example Interactions

### Booking a Table

User: I would like to book a table for 4 people on July 25th at 7 PM.
Chatbot: Sure! Can I have your name and contact details to confirm the booking?
User: My name is John Doe, and my contact number is 123-456-7890.
Chatbot: Thank you, John! Your table for 4 people on July 25th at 7 PM has been confirmed.


### Browsing the Menu
User: Can you show me the menu?
Chatbot: Sure! Here are some of our menu items:
1. Spaghetti Carbonara - $12.99
   Description: Classic Italian pasta with creamy sauce and pancetta.
   Dietary Information: Contains dairy, gluten.
2. Vegan Burger - $10.99
   Description: Delicious plant-based burger with lettuce, tomato, and vegan mayo.
   Dietary Information: Vegan, gluten-free.
...

### Placing an Order
User: I would like to order a Vegan Burger for takeaway.
Chatbot: Great choice! Can I have your name and contact details for the order?
User: My name is Jane Smith, and my contact number is 987-654-3210.
Chatbot: Thank you, Jane! Your Vegan Burger will be ready for takeaway in 20 minutes.

## Contribution Guidelines

We welcome contributions to improve the chatbot! Please follow these steps to contribute:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with a clear message.
4. Push your changes to your fork.
5. Submit a pull request to the main repository.
