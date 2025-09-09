# Project Car Price Analysis

**Project Car Price Analysis** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.
This project is a comprehensive data analysis of a car price dataset. Our primary objective was to explore the key factors that influence car prices and use these insights to inform the development of a professional, interactive dashboard. By uncovering which specifications, features, and configurations have the strongest impact on a vehicle's price, this analysis provides valuable intelligence for automotive businesses and enthusiasts.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* The Car Price Prediction Multiple Linear Regression dataset, sourced from Kaggle https://www.kaggle.com/datasets/hellbuoy/car-price-prediction, is a comprehensive collection of information on various automobiles, designed for building a machine learning model to predict car prices.

* The dataset is composed of two primary files:

1. CarPrice_Assignment.CSV: This is the main data file, containing 205 observations and 26 features. The features include details such as the car's make and model, technical specifications (e.g., engine size, horsepower, city and highway MPG), physical dimensions (e.g., wheelbase, length, width, height), and other key attributes like fuel type, number of doors, and engine location. The target variable for prediction is the price of the car.

2. Data Dictionary - carprices.xlsx: This supplementary file provides a detailed data dictionary, offering clear descriptions for each of the features found in the CSV file. This helps in understanding the meaning and data type of each column, which is crucial for data analysis and model development.

## Business Requirements
* Describe your business requirements
Core Objective: The primary objective is to serve as a data analytics consulting team for Geely Auto, providing a clear, data-backed strategy for their entry into the competitive US automobile market. The project will address the key business questions related to car pricing and market dynamics.

Data Analysis Goals:

* Analyse car prices based on various independent variables to understand the factors affecting car pricing in the US market.

* Develop interactive dashboards to provide insights into car pricing dynamics, helping the company design cars and develop business strategies that meet market demands.

## Context:
An automobile company aims to enter the US market and compete with local and European manufacturers. To adjust its strategies and designs accordingly, it needs to understand the factors influencing car prices in the US market. The dataset includes various car attributes, such as make, model, engine size, and price.

## How the Project Addresses the Objectives:

* Pricing Factor Analysis: We will analyze the provided dataset to identify which variables (e.g., horsepower, fuel efficiency, engine size, brand) are most significant in predicting a car's price in the American market. This directly answers Geely's need to understand how pricing works outside of their home market.

* Competitive Strategy Development: Instead of a single, broad analysis, our project focuses on the four identified customer personas (Budget Buyer, Family Buyer, Luxury Buyer, and Eco-friendly Buyer). We will provide specific, tailored insights for how Geely can design cars to be competitive within each market segment.

* Actionable Insights: The final deliverable will not just be a set of visualizations but a comprehensive strategy. The presentation will guide Geely on what features to prioritize and what market segments offer the most promising opportunities for a new competitor.

## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 

## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Full path directories were used when reading the csv file containing our unprocessed dataset, this means without the user manually changing this path when trying to use the notebook they won't be able to load the dataset into a dataframe

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.
