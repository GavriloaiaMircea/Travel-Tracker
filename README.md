# Travel Tracker

Travel Tracker is a web application that allows users to keep track of countries they have visited. It features an interactive world map where visited countries are highlighted, and users can add new countries to their list.

## Features

- Interactive world map visualization
- Add visited countries to your list
- Total count of visited countries
- Error handling for invalid or duplicate entries

## Technologies Used

- Node.js
- Express.js
- EJS (Embedded JavaScript templating)
- PostgreSQL
- HTML/CSS
- JavaScript

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js
- npm (Node Package Manager)
- PostgreSQL

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/GavriloaiaMircea/Travel-Tracker.git
   cd Travel-Tracker
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Set up the PostgreSQL database:
   - Create a database named "World"
   - Update the database connection details in `index.js` if necessary

4. Create the required tables in your database:
   ```sql
   CREATE TABLE countries (
     country_code VARCHAR(2) PRIMARY KEY,
     country VARCHAR(100) NOT NULL
   );

   CREATE TABLE visited_countries (
     country_code VARCHAR(2) PRIMARY KEY
   );
   ```

5. Populate the `countries` table with country data (country codes and names)

## Running the Application

1. Start the server:
   ```
   node index.js
   ```

2. Open a web browser and navigate to `http://localhost:3000`

## Usage

- The world map will be displayed on the main page
- To add a visited country, type the country name in the input field and click "Add"
- Successfully added countries will be highlighted on the map
- The total count of visited countries is displayed at the bottom of the page
- If you enter an invalid country or try to add a duplicate, an error message will be displayed

## File Structure

- `index.js`: Main server file with Express.js setup and route handlers
- `public/styles/main.css`: CSS styles for the application
- `views/index.ejs`: EJS template for the main page
