# Dynamic Pricing at Lyft Bay Wheels

*Disclaimer:* Instead of executing the project by parts (Part I, II, and III), I opted by doing a single Jupyter Notebook. The initial queries were done through the CL and are included in the section [Data Exploration](./Project_1#data_exploration), whereas project questions and visualizations were done using BigQuery, and are included in the section [Project Questions](./Project_1#project_questions).

## Problem Statement

### Situation

- Lyft Bay Wheels (https://www.lyft.com/bikes/bay-wheels) is the company running Bay Area Bikeshare.
- Their objective is to increase ridership through the offering of new deals through their mobile app. 
- Currently, Lyft Bay Wheels has several deal options to customers, which include: 
  * _Single Ride_: rides start at \\$2 for the first 30 minutes, then \\$3 per additional 15 minutes; 
  * _Monthly Membership_ - unlimited number of 45-minute rides, then \\$3 per additional 15 minutes; it costs \\$15 per month;
  * _Annual Membership_ - unlimited number of 45-minute rides, then \\$3 per additional 15 minutes; it costs \\$149 per year;
  * _Access Pass_ - unlimited number of 30-minute rides on 24-hours, then \\$3 per additional 15 minutes; it costs \\$10 per day;
  * _Bike Share for All_ - subsidized offers to income-eligible customers;
  * _Corporate Membership_ - fully or partially subsidized memberships sponsored by private organizations;
  * _Riding With Others_ - special Access Pass offers for groups;
  * _Ebike Pricing_ - special pricing conditions applicable for ebikes.

### Complication

- The number of rides has been declining in the past few months compared with the same period of last year.
- It is imperative to attract new customers to the service in order to achieve a higher utilization and a better profitability.

### Objetive
- In this project, we will recommend changes to our offering portfolio in order to increase the attractiveness of our service to new customers.
- We are going to focus on a customer segment that has proved to be particularly attractive to the company: the commuter riders.
- For the scope of this project, we will focus on the deal portfolio as it were the only lever at our disposal; we will not consider other business levers at disposal of Lyft Bay Wheels management team, such as increasing the number of stations, expanding number of docks on existing stations, offering new mobility options, creating a return service, partnering with other parking spaces, etc.

### Key questions
- To accomplish with the project's objectives, these are the most critical questions we need to answer: 

    * How fast have we been able to grow the overall number of trips in the system?
    * Which hours of the day concentrate the most number of trips ('commuter hours')?
    * What is the mix of subscribers vs. regular customers during the commuter hours? How does it compare to the mix during other periods of the day?
    * What is the average trip duration during commuter hours? How does it compare with the trip duration in other periods of the day? 
    * What are the 5 most popular trips that we would call "commuter trips" in the morning?
    * What are the 5 most popular trips that we would call "commuter trips" in the evening?
    * Which stations are the most demanded ones as origin points during commuter hours?
    * Where does our most demanded origin stations are located?
    * How is the availability of bikes in the most demanded origin stations during commuter hours? Do we have spare capacity to offer to new users?
    * Which stations are the most demanded ones as destination points during commuter hours?
    * Where does our most demanded destination stations are located?
    * How is the availability of dockers in the most demanded destination stations during commuter hours? Do we have spare parking capacity to offer to new users?
    * What are our recommendations for new offers (justified based on our findings)?
    
## Dataset

- For this project, we will use a Big Query Public Dataset, offered by Google Cloud Platform (GCP).
- The dataset covers an aproximate period of 3 years of bike trips in the Bay Area.
- It has two datasets: a static one and a dynamic one. We will use the static one, called **san_francisco**.
- From the **san_francisco** dataset, we will use the following tables:
    * bikeshare_stations
    * bikeshare_status
    * bikeshare_trips

## Tools

- This project will be done entirely on Google Cloud Platform (GCP).
- This project will make use of the following tools:
    * Our virtual machine on GCP
    * Jupyter Notebook
    * Google's BigQuery
    * Linux Command Line
    * Python 3
    * Numpy
    * Pandas
    * Geopandas
    * Matplotlib
    
## Summary of findings

From our analyses, we could learn that:
- Our business has been declining in the last months, making it imperative to attract new customers;
- Commuter hours are a very popular timing window for our service: from 7 to 10am in the morning, and from 4 to 7pm in the evening;
- Trip duration during commuter hours is almost half of that during the other service hours, and mix of subscribers is higher, suggesting commuter customers are very valuable to our company;
- The most demanded origin stations during commuter hours (either in the morning or in the evening) have enough bike availability to accomodate new users, without jeopardizing the quality of service for current users;
- The same applies for our most demanded destination stations during commuter hours (either in the morning or in the evening), which also have enough dock availability to accomodate new users;
- Given that, we will propose in the following chapter some new deals intended to maximize the use of our service during commuter hours, attracting new valuable customers and bringing additional revenue for our company.

## Recommendations

Based on the findings of this study we recommend a pilot of the following offerings intended to attract new commuter customers to our service:
- A **round trip** day option costing \\$2.50 a day; it allows you to pick a bike in one station, commute to another, and then came back later in the day to the same origin station; as the single ride option, it will cover the first 30 minutes of each ride, then it will charge an extra \\$3 per additional 15 minutes.
- A **commuter-only monthly membership** option - unlimited number of 30-minute rides valid within commuter hours only, then \\$3 per additional 15 minutes; it will be more affordable than the regular option, costing \\$9.90 per month. May be restricted for only a specific zone of origin-destination stations in the city.
- A **commuter-only annual membership option** - unlimited number of 30-minute rides within commuter hours only, then \\$3 per additional 15 minutes; it will be more affordable than the regular option, costing \\$99 per year. May be restricted for only a specific zone of origin-destination stations in the city.

## Full Report - Table of Contents

- [1-Problem Statement](./Project_1.ipynb#problem_statement)
- [2-Dataset](./Project_1.ipynb#dataset)
- [3-Tools](./Project_1.ipynb#tools)
- [4-Data Exploration](./Project_1.ipynb#data_exploration)
- [5-Project Questions](./Project_1.ipynb#project_questions)
- [6-Summary of Findings](./Project_1.ipynb#summary_findings)
- [7-Recommendations](./Project_1.ipynb#recommendations)