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

## 🗺️ Project Plan

The project is delivered over four structured milestones, each designed to scaffold a reproducible analytics workflow and map directly to the repo structure.

### 🔹 Milestone 1 — Project Setup · Kick‑off (Day 0)
**Objective**  
Establish a working, collaborative delivery environment so the team can start shipping immediately and predictably.

**Key Actions**
- Create GitHub repository and **Projects (Kanban) board** with status columns, labels, and issue/PR templates.
- Define folder structure: `Data/raw`, `Data/clean`, `jupyter_notebooks`, **`Media/`**, `Dashboard/`.
- Stage the Kaggle dataset into `Data/raw/` (`cars.csv`, `Data Dictionary - carprices.xlsx`).
- Seed ETL/EDA backlog and link issues/PRs to milestones; assign owners/reviewers.

**Success Criteria**  
Any teammate can clone, install deps, and run the first notebook without friction. The board provides real‑time visibility into planned, active, and completed work.

---

### 🔹 Milestone 2 — Initial ETL Build & First Visuals (Day 1)
**Objective**  
Turn the raw dataset into a clean, analysis‑ready table and verify the pipeline end‑to‑end.

**Key Actions**
- Implement **notebook‑driven ETL** (`jupyter_notebooks/ETL.ipynb`): parsing brand/model, standardizing categorical labels, converting units/types, engineering features, and exporting `Data/clean/cars_processed.csv` (**index=False**).
- Handle missing values safely (e.g., Subaru model → `dl`), keep outliers by design, and document assumptions.
- Produce first EDA visuals in `jupyter_notebooks/Visualisation.ipynb` and **save artifacts to `Media/`**.

---

### 🔹 Milestone 3 — ETL Refinement, Dashboards & Testing (Day 2)
**Objective**  
Harden and extend the pipeline to support decision‑grade insights and prep the first dashboard build.

**Key Actions**
- Add and validate **comparability scores** (City/Family, Outdoor/Off‑Road, Sport): per‑feature normalization (invert where higher is worse), sum, and re‑normalize to 0–1.
- **Quantify drivers of price**: compute absolute correlations and visualize strongest relationships (heatmap + scatter); export to `Media/`.
- Make paths robust (prefer `pathlib`), ensure **idempotent**/deterministic writes.
- Draft **Power BI** page layout (overview + persona pages) and field naming conventions aligned with ETL (e.g., *Engine Size (L)*).

---

### 🔹 Milestone 4 — Final Refinements, Presentation, Documentation & Publish (Day 3)
**Objective**  
Polish deliverables for readability and accessibility, and package the work for sharing and demo.

**Key Actions**
- Freeze `Data/clean/cars_processed.csv` and commit all `Media/` visuals (PNGs/HTML).
- Populate the presentation deck with an EDA narrative and figure references.
- (Optional) Publish a GitHub **Release** bundling CSV, figures, and PBIX when ready.

---

## 📁 Repository Structure (scaffold)

```
car-price-analysis-hackathon-team4/
├─ Dashboard/                     # PBIX + exported screenshots/GIFs when ready
├─ Data/
│  ├─ raw/                        # Kaggle CSV + data dictionary
│  └─ clean/
│     └─ cars_processed.csv       # ETL output (written by ETL.ipynb)
├─ jupyter_notebooks/
│  ├─ ETL.ipynb                   # cleaning, feature engineering, scoring, export
│  ├─ Visualisation.ipynb         # EDA (dists, correlations, outliers, scores)
│  └─ Notebook_Template copy.ipynb
├─ Media/                         # EDA figures/HTML + deck assets (images, GIFs)
├─ .gitignore
├─ .python-version
├─ .slugignore
├─ Procfile
├─ README.md
├─ requirements.txt               # include `scipy` (zscore) + core libs
└─ setup.sh
```

---

## 1️⃣ High‑Level Steps Taken for the Analysis

| Phase | Description |
|------:|-------------|
| **Setup** | Repo creation, Kanban board setup, folder scaffolding, dataset staging |
| **ETL Build** | Raw‑to‑clean transformation, notebook‑driven pipeline, first visuals |
| **EDA & Scores** | Distributions, correlations, **comparability scores**, outlier rationale |
| **Finalization** | Presentation narrative, documentation, (optional) GitHub Release |

---

## 2️⃣ Data Management Across All Phases

- **Collection** — Kaggle dataset staged in `Data/raw/`, tracked via GitHub issues.  
- **Processing** — ETL notebooks version‑controlled; outputs stored in `Data/clean/`.  
- **Analysis** — EDA steps logged in notebooks; visuals exported to **`Media/`**.  
- **Interpretation** — Insights narrated in the presentation; dashboard framework prepared.  
- **Collaboration** — Issues/PRs tied to milestones; reviewers ensure reproducibility and clarity.

---

## 3️⃣ Justification of Research Methodologies

| Methodology | Rationale |
|-------------|-----------|
| **Notebook‑Driven ETL** | Transparent, auditable, easy onboarding |
| **Power BI (planned)** | Stakeholder‑friendly, interactive exploration |
| **Milestone‑Based Delivery** | Agile iteration, clear accountability |
| **GitHub Project Management** | Labels, issues, reviewers → traceability |

---

## 👥 Collaboration & Teamwork

- **GitHub Projects** — Kanban board, labels, milestones, and linked issues/PRs.  
- **Google Drive** — Shared workspace for presentation and shared docs.  
- **Discord** — Daily check‑ins, async updates, links to issues and previews.

---

## 📦 Final Deliverables (current state)

- ✅ Cleaned dataset: `Data/clean/cars_processed.csv`  
- ✅ EDA artifacts saved in **`Media/`** (distributions, correlations, outliers, score‑vs‑price)  
- ✅ Jupyter notebooks: `jupyter_notebooks/ETL.ipynb`, `jupyter_notebooks/Visualisation.ipynb`  
- 🧭 Power BI dashboard: **framework defined**, PBIX to be built in `Dashboard/`

---
 

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

* In order to map the business requirements to meaningful data visualizations, the dataset includes both raw and processed features. Some features, such as power_to_weight, car_volume, and the various *_score metrics, were created during the ETL phase to provide more actionable insights. These features, along with the original data, serve as the input for the visualization phase, enabling analysis of market segmentation, performance, fuel efficiency, and suitability for different driving needs.

Car Dataset Features:

| Column                     | Description                              | Significance                          |
|----------------------------|------------------------------------------|---------------------------------------|
| `car_ID`                   | Unique car identifier                    | Distinguishes records                 |
| `brand`                    | Car manufacturer                         | Trend & market analysis               |
| `model`                    | Specific car model                       | Comparison between models             |
| `symbolling`               | Insurance risk rating                    | Indicates safety risk                 |
| `fueltype`                 | Fuel type (gas/diesel)                   | Impacts cost, emissions, performance  |
| `aspiration`               | Engine aspiration (standard/turbo)       | Affects engine power & efficiency     |
| `doornumber`               | Number of doors                          | Family/city suitability               |
| `carbody`                  | Car body style                           | Market segmentation & price           |
| `drivewheel`               | Drivetrain type                          | Handling & offroad capability         |
| `enginelocation`           | Engine placement                         | Affects balance & design              |
| `wheelbase`                | Distance between axles (inches)          | Stability & interior space            |
| `carlength`                | Car length (inches)                      | Interior space & parking              |
| `carwidth`                 | Car width (inches)                       | Maneuverability & comfort             |
| `carheight`                | Car height (inches)                      | Headroom & ground clearance           |
| `curbweight`               | Car weight (lbs)                         | Fuel efficiency & handling            |
| `enginetype`               | Engine type/configuration                | Technical analysis                    |
| `cylinernumber`            | Number of cylinders                      | Engine power & smoothness             |
| `enginesize`               | Engine size (cubic inches)               | Predictor of power & price            |
| `fuelsystem`               | Fuel delivery system                     | Efficiency & performance              |
| `boreratio`                | Bore-Stroke ratio                        | Engine design metric                  |
| `stroke`                   | Piston stroke length                     | Engine design metric                  |
| `compressionratio`         | Compression ratio                        | Efficiency & power                    |
| `horsepower`               | Engine power output                      | Performance & price                   |
| `peakrpm`                  | Max engine RPM                           | Performance characteristics           |
| `citympg`                  | City fuel efficiency                     | Cost & environmental analysis         |
| `Price`                    | Market price ($)                         | Target variable                       |
| `power_to_weight`          | Horsepower / curbweight                  | Real-world performance                |
| `car_volume`               | Estimated car volume                     | Interior space & comfort              |
| `mpg_ratio`                | City MPG / highway MPG                   | Compare fuel efficiency               |
| `is_luxury`                | Luxury car flag                          | Market segmentation                   |
| `city_score`               | Family/city suitability                  | Composite score                       |
| `outdoor_score`            | Offroad suitability                      | Composite score                       |
| `sport_score`              | Sportscar suitability                    | Composite score                       |
| `city_score_normalized`    | Normalized city score (0-1)              | Comparison across cars                |
| `outdoor_score_normalized` | Normalized outdoor score (0-1)           | Comparison across cars                |
| `sport_score_normalized`   | Normalized sport score (0-1)             | Comparison across cars                |

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Accessibility for Color Blind Users
All visualizations in this project have been tested for accessibility using COBLIS (Color Blindness Simulator). The accompanying image demonstrates how the charts appear under a wide range of color vision conditions, including:
• 	Red-Weak (Protanomaly)
• 	Green-Weak (Deuteranomaly)
• 	Blue-Weak (Tritanomaly)
• 	Red-Blind (Protanopia)
• 	Green-Blind (Deuteranopia)
• 	Blue-Blind (Tritanopia)
• 	Monochromacy (Achromatopsia)
• 	Blue Cone Monochromacy
Each chart was evaluated across these conditions to ensure that key visual distinctions—such as data clusters, trends, and histogram distributions—remain perceptible and interpretable regardless of color vision type.
Based on the analysis of the simulation grid, no further adjustments were necessary. The charts maintain sufficient contrast, shape differentiation, and layout clarity, making them accessible to users with all forms of color vision deficiency. This ensures that the visual integrity of the data is preserved without relying solely on color cues.
By proactively testing and validating our visualizations, we aim to support inclusive design and make data insights available to a broader audience.

Example:
![COBLIS Test Result](https://github.com/AL-MASNAI/car-price-analysis-hackathon-team4/raw/main/Media/Coblis_test.png "Color Blindness Simulation")

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
