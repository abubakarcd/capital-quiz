#  World Capital Quiz
Welcome to the World Capital Quiz! This website allows users to test their knowledge of world capitals by guessing the capital city of various countries. The quiz pulls data from a PostgreSQL database containing country names and their respective capitals.

# Features
- Quiz Mode: Users are presented with the name of a country and asked to guess its capital.

-Database Integration: The capitals and countries are stored in a PostgreSQL database.

-Score Tracking: Users can track their score based on correct answers.

-Interactive UI: User-friendly interface to make learning fun and engaging.
 # Getting Started
 # Prerequisites
Before starting, ensure you have the following installed:

-PostgreSQL: Make sure PostgreSQL is installed and running on your machine.
-Node.js (if using a JavaScript backend)
-npm (if using Node.js)
Installation
Follow these steps to set up the project locally:

# Clone the Repository
Clone the repository to your local machine using the following command:

git clone https://github.com/your-username/world-capital-quiz.git
cd capital-quiz

# Set Up Database
Create a PostgreSQL database named country for the app:
CREATE DATABASE country;

# Create the Country Table
Inside the country database, create a table to store the countries and capitals:

CREATE TABLE country (
  id SERIAL PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  capital VARCHAR(255) NOT NULL
);
# Import Data
Populate the country table with countries and their capitals. You can either manually insert data or use an SQL file like countries_and_capitals.sql. Example:


INSERT INTO country (name, capital)
VALUES
  ('France', 'Paris'),
  ('United Kingdom', 'London'),
  ('United States of America', 'Washington, D.C.');
# Configure Environment Variables
Create a .env file in the root directory and add the following environment variables:


PG_USER=your-username
PG_HOST=localhost
PG_DATABASE=country
PG_PASSWORD=your-password
PG_PORT=5432
# Install Dependencies
If using Node.js, install the necessary packages:


npm install
 # Start the App
Run the app on your local machine:

npm start
# Access the App
Open your browser and go to http://localhost:3000 (or the specified port) to play the quiz.

# Usage
-Start the Quiz: Click the "Start Quiz" button to begin. You will be shown a country name and need to enter the capital city.

-Answer: Type your answer and submit. The app will tell you whether you're correct and move on to the next question.

-Score: Your score will be tracked throughout the quiz. Try to get as many correct answers as possible!

