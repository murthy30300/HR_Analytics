# HR Analytics Dashboard

## Project Overview
An end-to-end HR analytics solution that transforms raw HR data into actionable insights through an interactive dashboard, providing HR professionals with evidence-based information for strategic decision-making.

![HR Analytics Dashboard](https://res.cloudinary.com/dovvc3hvb/image/upload/v1745673528/hr.jpg)

## Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [System Architecture](#system-architecture)
- [Technologies Used](#technologies-used)
- [Implementation](#implementation)
- [Dataset](#dataset)
- [Data Flow](#data-flow)
- [Results and Insights](#results-and-insights)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Installation and Setup](#installation-and-setup)
- [Contributing](#contributing)
- [License](#license)

## Abstract
The HR Analytics Dashboard project delivers a data-driven solution for workforce management by leveraging a publicly available HR dataset. The dataset was meticulously preprocessed to ensure data integrity, addressing missing values, inconsistencies, and outliers. Using Microsoft Power BI, an interactive dashboard was developed to visualize critical HR metrics, including employee turnover, performance trends, and demographic insights. The dashboard was embedded into a user-friendly front-end webpage, enhancing accessibility for stakeholders. The entire solution was deployed on Microsoft Azure, ensuring scalability and seamless access. This project integrates data preprocessing, business intelligence, and cloud hosting to provide HR professionals with actionable insights, demonstrating a scalable approach to HR analytics for strategic decision-making.

## Introduction
Human Resource (HR) analytics has become a cornerstone for organizations seeking to optimize workforce performance and align talent strategies with business goals. The HR Analytics Dashboard project was initiated to create an intuitive, data-driven tool that transforms raw HR data into actionable insights.

Utilizing a publicly sourced HR dataset, the project involved a systematic pipeline of:
- Data preprocessing
- Analysis
- Visualization
- Deployment

The dataset was cleaned and structured to ensure quality, followed by the development of an interactive dashboard using Power BI to showcase key performance indicators (KPIs) such as attrition rates, employee satisfaction, and departmental demographics. To enhance user accessibility, the dashboard was embedded into a custom front-end webpage and hosted on Microsoft Azure for scalability and reliability.

## Problem Statement
Organizations often struggle to derive meaningful insights from raw HR data due to challenges such as:
- Inconsistent data formats
- Missing values
- Lack of intuitive visualization tools

Traditional HR reporting methods are time-consuming and fail to provide real-time, actionable insights into workforce dynamics. Additionally, the absence of scalable, accessible platforms limits stakeholders' ability to interact with HR analytics effectively.

This project addresses these challenges by developing an HR Analytics Dashboard that processes and visualizes HR data efficiently, offering a user-friendly interface and cloud-based deployment to support strategic HR decisions.

## Objectives
The primary objectives of the HR Analytics Dashboard project are:

1. **Data Preprocessing**: Clean and preprocess a publicly available HR dataset, ensuring data quality by handling missing values, outliers, and inconsistencies.

2. **Data Visualization**: Develop an interactive dashboard using Power BI that visualizes key HR metrics, such as employee turnover, performance, and demographic distributions.

3. **Front-End Integration**: Embed the Power BI dashboard into a front-end webpage, providing an intuitive interface for stakeholders to access analytics.

4. **Cloud Deployment**: Host the front-end application on Microsoft Azure, ensuring scalability, security, and seamless access for users.

5. **Actionable Insights**: Enable HR professionals to make data-driven decisions by providing clear, visual insights into workforce trends and patterns.

## System Architecture
The system architecture of the HR Analytics Dashboard is designed as a modular pipeline:

```
┌───────────┐     ┌───────────────┐     ┌────────────────┐     ┌───────────────┐     ┌───────────────┐
│           │     │               │     │                │     │               │     │               │
│ Data Layer│────>│Preprocessing  │────>│ Analytics Layer│────>│ Front-End     │────>│ Deployment    │
│           │     │ Layer         │     │                │     │ Layer         │     │ Layer         │
└───────────┘     └───────────────┘     └────────────────┘     └───────────────┘     └───────────────┘
```

- **Data Layer**: The HR dataset, sourced online, is ingested and stored in a structured format (CSV/Excel).
- **Preprocessing Layer**: Data cleaning and transformation using Python or Power BI's built-in tools.
- **Analytics Layer**: Power BI interactive dashboard creation, visualizing KPIs through charts, graphs, and tables.
- **Front-End Layer**: Power BI dashboard embedded into a front-end webpage built with HTML/CSS/JavaScript.
- **Deployment Layer**: Front-end application hosted on Microsoft Azure for scalability and accessibility.

## Technologies Used
The project leverages a suite of modern technologies:

- **Python**: Data preprocessing tasks (cleaning, normalization, outlier detection using Pandas and NumPy)
- **Microsoft Power BI**: Data visualization and dashboard creation
- **HTML/CSS/JavaScript**: Front-end webpage development for embedding the Power BI dashboard
- **Microsoft Azure**: Cloud hosting of the front-end application
- **Excel/CSV**: Formats for storing and importing the HR dataset

## Implementation
The implementation followed a structured workflow:

1. **Data Acquisition**: A publicly available HR dataset was downloaded from an online repository.

2. **Preprocessing**:
   - Python scripts for data cleaning
   - Handling missing values (imputation with mean/median)
   - Encoding categorical variables (one-hot encoding)
   - Removing outliers

3. **Dashboard Development**:
   - Imported preprocessed data into Power BI
   - Created visualizations (bar charts, pie charts, line graphs)
   - Added interactive filters and slicers for dynamic exploration

4. **Front-End Integration**:
   - Embedded Power BI dashboard into a front-end webpage
   - Used Power BI's "Publish to Web" feature
   - Implemented responsive design with HTML/CSS/JavaScript

5. **Cloud Deployment**:
   - Deployed front-end application on Microsoft Azure using Azure App Service
   - Configured for scalability and secure access

## Dataset
The project utilized a publicly available HR dataset containing information such as:

- Employee ID, age, gender
- Department, job role
- Years of experience
- Performance ratings
- Attrition status
- Salary

The dataset was preprocessed to ensure data quality, addressing issues like missing values and inconsistent formats.

## Data Flow
The flow of data through the system is illustrated below:

### Level 0 (Context) Diagram
```
┌───────────┐     ┌───────────────────┐     ┌─────────────────┐
│           │     │                   │     │                 │
│ HR Dataset│────>│ HR Analytics System│────>│Users/Stakeholders│
│           │     │                   │     │                 │
└───────────┘     └───────────────────┘     └─────────────────┘
```

### Level 1 Data Flow Diagram
```
                                 ┌───────────┐
                                 │           │
                        ┌───────>│Cleaned Data│───────┐
                        │        │           │       │
                        │        └───────────┘       │
                        │                            ▼
┌───────────┐     ┌────────────┐     ┌────────────┐     ┌──────────────┐
│           │     │            │     │            │     │              │
│ HR Dataset│────>│1.0 Data    │────>│2.0 Data    │────>│3.0 Data      │
│           │     │   Ingestion│     │Preprocessing│     │  Visualization│
└───────────┘     └────────────┘     └────────────┘     └──────────────┘
                                                               │
                                                               ▼
                                                        ┌────────────────┐
                                                        │                │
                                                        │Power BI Dashboard│
                                                        │                │
                                                        └────────────────┘
                                                               │
                        ┌───────────────────────────────────────┘
                        │
                        ▼
                 ┌────────────┐     ┌────────────┐     ┌───────┐
                 │            │     │            │     │       │
                 │4.0 Dashboard│────>│5.0 Cloud   │────>│ Users │
                 │   Embedding │     │  Deployment│     │       │
                 └────────────┘     └────────────┘     └───────┘
```

## Results and Insights
The HR Analytics Dashboard successfully achieved its objectives:

- **Data Quality**: Preprocessing ensured a clean, reliable dataset with missing values reduced to 0% and outliers handled effectively.

- **Visualization**: The Power BI dashboard provided clear insights, identifying high-turnover departments and performance trends, enabling targeted HR interventions.

- **Accessibility**: The front-end webpage offered an intuitive interface, with the embedded dashboard accessible to non-technical users.

- **Scalability**: Azure hosting ensured reliable access with minimal latency, supporting multiple users simultaneously.

Key insights derived from the dashboard include:
- Employee attrition patterns by department
- Performance trends across demographics
- Factors influencing employee satisfaction

## Conclusion
The HR Analytics Dashboard project successfully delivered a scalable, user-friendly solution for workforce analytics. By combining data preprocessing, Power BI visualization, front-end integration, and Azure hosting, the project empowered HR professionals with actionable insights into employee trends. The solution demonstrated the feasibility of building end-to-end analytics pipelines using modern tools and cloud infrastructure.

## Future Work
Potential enhancements for future iterations include:

- Integration of real-time data sources (e.g., HRIS APIs) for dynamic updates
- Incorporation of machine learning models to predict employee attrition or performance
- Enhancement of the front-end with advanced features like user authentication or personalized dashboards
- Expansion of the dataset to include additional metrics, such as employee engagement or training outcomes

## Installation and Setup
To set up this project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/murthy30300/HR_Analytics.git
   cd hr-analytics-dashboard
   ```

2. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run data preprocessing:
   ```bash
   python preprocess.py
   ```

4. Open the `index.html` file in your browser or deploy to a web server.

5. For Power BI visualizations, open the `.pbix` file in Power BI Desktop.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.
