# Project Overview

The objective of this project is to provide an alternative web application to Dublin Bikes' default service. While the default application offers basic information on bike availability, our application aims to enhance the user experience by incorporating additional features such as weather information, a journey planner, and bike availability predictions.

## Key Components

### Backend
Developed using Python with Flask as the framework, the backend manages client-side fetch requests, data manipulation, model file reading, and general server-side logic. It renders the default HTML page displayed to users on their browsers.

### Frontend
Built with HTML, CSS, and JavaScript, the frontend utilizes external libraries like Chart.js for data visualization and Google APIs for map integration and geolocation services.

### Data Scraping
Automated data collection is facilitated by Crontab scheduling the execution of a web scraper on an EC2 instance. This ensures seamless and reliable data gathering 24/7.

### Data Analytics
Machine learning models predict bike availability and occupancy based on weather patterns and historical bike usage. These models, implemented using scikit-learn and pandas in Python, are trained on data collected by the web scraper.

### External Data Sources
The application relies on data from two external service providers: JCDecaux for bike station information and WeatherAPI for weather data.

### Hosting and Deployment
The web application is hosted on an Amazon EC2 instance, with scraped data stored in an Amazon RDS database. Gunicorn and Nginx are employed for efficient load balancing, reverse proxying, and improved performance.

## Architecture

The single-page application features:

- A left-hand search bar and journey planner for easy navigation.
- A responsive map displaying bike stations with markers and allowing users to zoom for detailed views.
- A header with the application logo and a weather widget for current weather information.
- Graphs displaying historical and predictive bike occupancy data below the map.

## Key Features

- **Real-time Accurate Information:** Users receive up-to-date occupancy, bike availability, and weather data for timely decision-making.

- **Journey Planning:** A user-friendly journey planner computes the best route based on the starting point, destination, and current conditions.

- **Machine Learning-Powered Predictions:** Machine learning models predict bike occupancy, empowering users to make informed decisions and promoting efficient bike-sharing practices.

- **User-Based Geolocation:** Displays the nearest bike station to the user's location on the map, enhancing accessibility and user experience.
