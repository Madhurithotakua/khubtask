        August Practice task by IIIT Hyderabad
        =======================================

Title:  K-Hub Practice React App
====================================

Car Data Analysis Web Application
Project Overview:
=================
Description: This web application is designed to analyze and visualize data related to various car models. It offers statistical insights and an overview of key attributes that can assist both car buyers and enthusiasts in making informed decisions.
This project aims to develop a data ingestion, analytics, and visualization system. The system allows users to input data through a form or an Excel sheet frontend built with React. The entered data is stored in a database for further processing and analysis. A Python script is utilized to perform analytics on the data, and the results are stored back in the database. Finally, the frontend visualizes both the raw data and the output of the Python script
Table of Contents
•	Procedure
•	Frontend
o	React Js
•	Backend
o	Database
o	Dataset
•	 Technologies used
•	Conclusion
Procedure
First thing is to create 2 folders named Frontend and Backend The folder structure is as follows:

├── docs
│   ├── images
│   ├── help documents...                               
├── frontend 
│   ├── src
│   │   ├── assests
│   │   ├── components
│   │   │   ├── component_name
│   │   │   │   ├── **/*.css
│   │   │   │   ├── **/*.js
│   │   ├── pages
│   │   │   ├── page_name
│   │   │   │   ├── **/*.css
│   │   │   │   ├── **/*.js
├── backend
├── README.md
└──.gitignore
The folder structure is as follows:


 

FRONTEND:
1.	Importing React and CSS: The code starts by importing React, which is a JavaScript library for building user interfaces. Additionally, it imports CSS files for styling.
2.	Footer Component (Footer.js):
•	This section defines a functional component named Footer. Components in React are reusable building blocks for user interface.
•	Within the footer:
o	An image of a Git logo is displayed, adding visual appeal.
•	The styles for this component are defined in an associated CSS file called 'Footer.css'.
3.	Navbar Component (Navbar.js):
•	In this part of the code, another functional component named Navbar is created.
•	The purpose of the Navbar component is to render the header or navigation bar.
•	Inside the Navbar:
o	The application name or logo, which is "K-Hub React Practice App" in this case, is displayed prominently.
•	Slides Component (slides.js):
o	The slides component is the main content area of our application. It handles the display of various statistics and visualizations.
4.	Key functionalities of this component:
•	Fetching Data:
o	Data for metrics like mean, maximum, variance, standard deviation, median, and minimum is fetched from a Flask backend using the fetch function and API endpoints.
•	Histograms:
o	For each metric, a histogram (bar chart) is created using the rechart library. These visualizations are then displayed within separate elements.
•	The styles for this component are not explicitly mentioned but can be defined in a corresponding CSS file.
It is organized into components, each with a specific role. The Footer and Navbar components handle the layout and branding of our site. The Body component, on the other hand, is responsible for data fetching, visualization, and presenting dataset information. Together with the Flask backend, this code allows users to explore and analyze dataset statistics in a user-friendly manner.
We run the frontend part using the command npm start
This will be the output that has to be displayed on running the command with connection of backend.
 
 

BACKEND:
1.	Import requried   Modules:
o	Flask: A micro web framework for creating web applications.
o	CORS: A Flask extension for handling Cross-Origin Resource Sharing (CORS) headers.
o	MongoClient: A class from the pymongo library for connecting to MongoDB.
o	numpy as np: A library for numerical computations.
o	pandas as pd: A library for dataFrames.
o	json : A library for doing operation on json files
2.	Create Flask App and Enable CORS:
•	An instance of the Flask app is created and named app.
•	CORS is enabled using CORS(app) to allow Cross-Origin requests.
3.	Connect to MongoDB:
•	A connection to the local MongoDB server is established using MongoClient.
4.	Fetch Data from MongoDB:
•	Data from the 'carsdata’ collection in the 'carsdata' database is fetched.
•	Feautures of each model of cars are extracted from the data and stored in separate lists.
5.	Route for Mean:
•	A route '/mean' is defined for calculating and returning the mean of a particular subject.
•	The np.mean() function is used to compute the mean.
6.	Route for Maximum:
•	A route '/maximum' is defined for calculating and returning the maximum of a particular subject.
7.	Route for Variance:
•	A route '/variance' is defined for calculating and returning the variance of a particular model.
•	The np.var() function is used to compute the variance.
8.	Route for Standard Deviation:
•	A route '/std_deviation' is defined for calculating and returning the standard deviation of a particular model.
9.	Route for Median:
•	A route '/median' is defined for calculating and returning the median of a particular model.
•	The np.median() function is used to compute the median.
10.	Route for Minimum:
•	A route '/Minimum' is defined for calculating and returning the Minimum of a particular subject.
11.Running the Flask App:
•	The app is run with the debug mode set to True, allowing for real-time debugging.
•	Once we run the backend part using command python app.py
•	The data in my backend is as shown:

 
The provided code sets up a Flask backend to compute various statistics (mean, maximum, variance, standard deviation, median, minimum) for cars data stored in a MongoDB database. The React frontend fetches this data from the backend and displays it along with barcharts using recharts. This setup allows users to visualize and analyze the characteristics of the dataset.
DATA SET: Car data
1.The dataset comprises various attributes related to car models, encompassing details such as the manufacturer, type, seating capacity, engine displacement, dimensions (length, width, height, wheelbase), cylinder count, fuel type, engine specifications, transmission type, brake systems, drive type, turning radius, fuel tank capacity, boot space, fuel efficiency, emission classification, tire size, available variants, and NCAP safety rating. This comprehensive collection of attributes offers insights into the specifications, performance, and safety features of different car models. Analyzing this data can help in understanding the diversity and characteristics of vehicles, aiding in decision-making for buyers, manufacturers, and automotive enthusiasts.
2.This is a dataset has the data about various cars of different models and also has some key components that tell if a car is good to buy, affordable for a certain range or not. The dataset comprises various attributes related to car models, encompassing details such as the manufacturer, type, seating capacity, engine displacement, dimensions (length, width, height, wheelbase), cylinder count, fuel type, engine specifications, transmission type, brake systems, drive type, turning radius, fuel tank capacity, boot space, fuel efficiency, emission classification, tire size, available variants, and NCAP safety rating. All these features help to define the performance and durability of a car. This comprehensive collection of attributes offers insights into the specifications, performance, and safety features of different car models. Analyzing this data can help in understanding the diversity and characteristics of vehicles, aiding in decision-making for buyers, manufacturers, and automotive enthusiasts.

 

Technologies Used:
Frontend: React.js, Axios, Recharts, FontAwesome, CSS
Backend: Flask, MongoDB, Python (programming language for the backend logic)
Data Analysis: Python libraries (NumPy, pandas, statistics)
Version Control: Git

CONCLUSION:

The implemented data ingestion, analytics, and visualization system provide users with a convenient way to input data, perform analytics, and visualize the results. The frontend allows for data input
through a form or Excel sheet uploads, while the backend manages the storage of data in the database. The Python script handles the analytics tasks, and the results are stored back in the database. Finally, the frontend presents the data and analytics output in a visually appealing manner, enabling users to gain insights from the processed information









  






