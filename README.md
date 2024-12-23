# Survey-Project
# README for Income and Expense Survey Project

This project is a web-based survey tool built using Flask and MongoDB to collect and store user data related to income and expenses. The data collected includes details such as age, gender, total income, and categorized expenses. The project also involves analyzing and visualizing the collected data using Python, followed by hosting the application on AWS.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Setup Instructions](#setup-instructions)
4. [Usage](#usage)
5. [Data Processing and Analysis](#data-processing-and-analysis)
6. [Visualizations](#visualizations)
7. [Deployment on AWS](#deployment-on-aws)
8. [Known Issues](#known-issues)


## Project Overview

The project implements a simple survey form where users can input their income and expense data. The data is stored in a MongoDB database, and various Python scripts are used for data processing, analysis, and visualization. The results are displayed in graphical formats, which are then exported for further presentation in a PowerPoint file.

### Key Features:
- **Web Interface**: A form-based interface to collect user data, including name, age, gender, total income, and expenses across different categories.
- **Data Storage**: User data is stored in MongoDB.
- **Data Processing**: Python is used to process the data and export it to a CSV file.
- **Visualization**: Data visualizations are generated using Matplotlib in a Jupyter notebook.
- **AWS Hosting**: The Flask application is hosted on AWS.

## Technologies Used

- **Flask**: Python web framework for building the web application.
- **MongoDB**: NoSQL database for storing user data.
- **Python**: For data processing and analysis.
- **Matplotlib**: For data visualization.
- **Jupyter Notebook**: For analysis and visualization of data.
- **AWS EC2**: For hosting the web application.
- **HTML/CSS**: For front-end design of the survey form.



## Setup Instructions

### Prerequisites
1. Python 3.x installed on your system.
2. MongoDB installed and running locally 
3. Flask and required Python libraries installed. 

### Installing Dependencies
Clone the project repository or download the project files.

1. Install Python dependencies:
   ```bash
   pip install Flask pymongo pandas matplotlib
   ```

2. Set up MongoDB:
   - Install MongoDB and ensure it is running locally.
   - Create a database named `survey_tool` and a collection named `users`.

### Running the Application

1. Navigate to the project directory.
2. Run the Flask application:
   ```bash
   python app.py
   ```

####Necessary 
Flask
pymongo
pandas
matplotlib
jupyter


3. Open your browser and go to `http://127.0.0.1:5000/` to access the survey form.

## Usage

1. **Submit Survey**: 
   - On the main page, fill in the survey form with the required details (name, age, gender, income, and expenses).
   - Click the **Submit** button to store the data in the MongoDB database.

2. **View Submitted Data**:
   - The survey submissions will be stored in the MongoDB database, and all users' data can be viewed on the database at the backend.

3. **Export Data**:
   - The Python script `export_to_csv.py` will fetch data from MongoDB and export it as a CSV file for further processing.

## Data Processing and Analysis

Once the data is exported to a CSV file, you can use the `user_analysis.ipynb` Jupyter notebook to analyze and visualize it.

### Steps:
1. **Load Data**: The CSV file (`users.csv`) containing the survey data will be loaded into the Jupyter notebook.
2. **Data Processing**: The expenses column is normalized into separate columns (e.g., utilities, entertainment, etc.).
3. **Data Calculations**: Total income and expenses for each user are calculated.
4. **Visualizations**: Generate charts to analyze the data:
   - **Ages with the Highest Income**: A bar chart displaying the total income for each age group.
   - **Gender Distribution Across Spending Categories**: A stacked bar chart displaying the spending across different categories, broken down by gender.

### Running the Analysis:
To run the analysis:
1. Open `user_analysis.ipynb` in Jupyter.
2. Ensure the `users.csv` file is in the same directory.
3. Run all the cells to perform the analysis and visualize the results.

## Visualizations

The visualizations are saved as images (`income_by_age.png` and `spending_by_gender.png`) in the `data` directory. These images can be included in a PowerPoint presentation for client use.

## Deployment on AWS

The Flask application can be deployed on AWS EC2.

### Steps to Deploy:
1. Launch an EC2 instance and SSH into it.
2. Install required software (Python, Flask, etc.) on the instance.
3. Upload the project files to the EC2 instance.
4. Run the Flask application on the EC2 instance:
   ```bash
   python app.py
   ```
5. Access the application using the EC2 public IP address:
   ```bash
   http://<your-ec2-public-ip>:5000/
   ```

   http://34.201.65.134:5000

## Known Issues

- **TemplateNotFound Error**: There is a known issue where the template `index.html` cannot be found on the deployed AWS instance due to missing files. This issue is being worked on, and a workaround will be provided soon. Network Connectivity Issues such as  firewalls or VPNs were blocking SSH connections causing inability to  ping the server.

## Conclusion: Data Analysis and Visualizations
### Conclusion

This project provides valuable insights into income and spending patterns across different age and gender groups. The **Ages with the Highest Income** visualization highlights the key age demographics contributing the most to total income, allowing businesses to identify and target high-value customers, particularly those in their 30s and 40s, for products such as financial services or high-value goods. 

The **Gender Distribution Across Spending Categories** chart reveals distinct spending behaviors between men and women, offering businesses the opportunity to tailor their offerings to specific gender preferences. For example, women may spend more on healthcare or shopping, while men may focus on transportation or entertainment. 

By combining these insights, businesses can refine their marketing strategies, create personalized campaigns, and better understand their customer demographics. This data-driven approach will enable companies to optimize their products and services, ensuring they meet the needs and preferences of their target audiences.

