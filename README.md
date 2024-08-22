# Optimizing Global Logistics for Airplane Spare Parts

## Project Overview

This project focuses on designing and optimizing a global logistics network for distributing airplane spare parts. The objective is to ensure that parts are delivered to grounded airplanes as quickly as possible, minimizing downtime and associated costs. By utilizing mixed integer programming, we modeled and solved the logistics problem to determine the optimal locations for depots worldwide. The project also includes an analysis of cost implications based on varying service level commitments, which are critical for maintaining the efficiency and effectiveness of the distribution network.

## Project Setting

### Introduction

The project is set within the context of an airplane manufacturer that supplies spare parts to airlines and private operators worldwide. Given the unpredictable nature of demand for airplane spare parts, the manufacturer needs a robust logistics network to minimize the time required to deliver parts to grounded airplanes. The high costs associated with grounded airplanes make it imperative to ensure that parts are delivered within a strict service level target.

### Data and Assumptions

- **Suppliers**: The airplane manufacturer sources parts from multiple suppliers located in various countries. Each supplier, except those in the U.S., has a supply limit of 200,000 kg per year.
- **Parts**: There are 127 part classes, each with a specific weight, that need to be distributed.
- **Customer Locations**: The demand for parts originates from major airports in 119 countries.
- **Depots**: Potential depot locations are identified, each with a specified capacity to handle orders. Chicago depot (D1) has double the capacity of other depots.
- **Service Levels**: The manufacturer aims to have 95% of grounded planes returned to service within 24 hours, requiring each country to be within 9 hours of a depot.

## Problem Statement

### Part 1: Modeling

We modeled the spare parts logistics problem as a mixed integer program. The model includes decision variables for depot locations, constraints for supplier capacity, depot capacity, and service level requirements. The service level was modeled based on the transportation costs, which served as a proxy for flight times.

### Part 2: Solution

Using Gurobi and Python (gurobipy), we solved the optimization problem to determine:
- **Optimal Depot Locations**: Which depots should be open to minimize costs while meeting service levels.
- **Objective Function Value**: The total cost, including fixed depot costs and variable transportation costs.
- **Cost Breakdown**: A detailed analysis of fixed and variable costs associated with the optimal solution.

### Part 3: Metrics

To provide actionable insights to the company, we calculated:
- **Depot Utilization**: The number of parts and total weight handled by each depot, along with the percentage of capacity used.
- **Customer Allocation**: Which depots each customer (country) is allocated to for part deliveries.
- **Model Complexity**: The number of variables and constraints in the model.

### Part 4: Service Level Sensitivity Analysis

We analyzed the impact of different service level commitments on costs by adjusting the maximum allowable flight time (and corresponding transportation costs). The scenarios considered were 6-hour, 9-hour, 12-hour, and 15-hour flight times, with transportation costs adjusted accordingly. We explored how these changes affect the number of required depots and the overall cost, providing insights into the trade-offs between service speed and cost.

## Presentation

The final part of the project involved preparing a presentation for the operations management team at the airplane manufacturer. The presentation focused on the analysis and recommendations derived from the optimization and sensitivity analysis, highlighting the financial implications of different service level commitments and providing clear, actionable insights.

## Technologies Used

- **Python (gurobipy)**: For modeling and solving the mixed integer programming problem.
- **Gurobi**: Optimization solver used to find the optimal solution.
- **Excel/CSV**: For data handling and preprocessing.

## Conclusion

This project successfully optimized the global logistics network for distributing airplane spare parts, balancing the trade-offs between cost and service level commitments. The detailed analysis provides the airplane manufacturer with a strategic plan for depot placement, ensuring that grounded airplanes receive parts quickly, thereby minimizing downtime and associated costs.

![image](https://github.com/user-attachments/assets/6c122eb3-4ba1-4165-9f87-89b15a391ff1)

