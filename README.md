# Data_Science_PhonePay
## Phonepe Pulse Data Visualization and Exploration: A User-Friendly Tool Using Streamlit and Plotly

# 1. Introduction and Technologies Used: 
# 2. Streamlit Part: outlined the layout and components by using Streamlit app. It's good to split the layout into different columns (col1, col2, col3) to organize different sections.
# 3. Data Extraction and Database Connection:
# 4. Data Visualization: Plotly for data visualization
# 5. Geo Visualization: Plotly Express for geospatial visualization
# 6. Data Visualization Insights: 

## Technologies: Github Cloning, Python, Pandas, MySQL, mysql-connector-python, Streamlit, and Plotly.

# libraries used:
import pandas as pd
import os
import json
import pymysql
import numpy as np
import streamlit as st
import plotly.graph_objects as go
import plotly.express as px

# streamlit Part:
---- st.set_page_config(page_title="Phonepe Pulse Data Visualization and Exploration",page_icon=":bar_chart:",layout="wide")
----- st.title(":chart_with_upwards_trend: Phonepe Pulse Data Visualization and Exploration")
spliting the layot into 3,

# with col1:
   - ("Data Evaluation")
   - creating the button:
       - button("Top 10 states by transaction volume."):
       - button("Top transaction count and type"):
       - button("Top brands by usage in each year"):
       - button("Top 10 districts by transaction volume"):
       - button("Bottom 10 states by transaction volume"):
       - button("Bottom brands by usage in each year"):
       - button("Bottom 10 districts by transaction volume")
                
# with col2:
   - ("Geo Visualization")
   - Again splited into Tab:
          - tabs(["Transaction Visualization", "User Visualization"])
                   # with tab1:
                         - button("Geo Visualization - Transaction_Data")
                   # with tab2:
                         - button("Geo Visualization - User_Data "):

# with col3:
     - ("Data Visualiation")
             - checkbox(":open_book: Insights"):
             - selectbox("("Total Transaction Amount by Quarter (Animated by Year)",
                                                "Trend of Transaction Counts by Year and Transaction Type",
                                                "Usage of Mobile Brands",
                                                "Amount by Year for each State and District",
                                                "Statistical Representation - State vs Year vs Amount",
                                                "Statistical Representation - State vs year vs count"))

## Extract data from the Phonepe pulse Github repository through scripting and clone it..
# Extraction of Aggregate User Data:
path = "C:\\Users\\LENOVO\\OneDrive\\Desktop\\Phonepay Project\\data\\data\\aggregated\\user\\country\\india\\state"
Aggregate_state_user=os.listdir(path)
Extract the Data from the respective path, store the data in the list.
OS - In Python, the os module provides a way of using operating system-dependent functionality. It allows you to interact with the operating system, such as working with files and directories, managing processes, and obtaining information about the system.
Exclude the value to exclude from the list of values to remove:

## Extraction of Aggregate Transaction Data:
## Extraction of Map Transaction Data:
## Extraction of Map User Data:
## Extraction of Top Trans Data:
## Extraction of Top User Data:

## Connecting to data base:
Creating the "PhonePay" database in mysql.

# creating the data(Aggregate Transaction Data) table in sql:
# creating the data(Aggregate User Data) table in sql:
# creating the data(Map Transaction Data) table in sql:
# creating the data(Map User Data) table in sql:
# creating the data(Top Transaction Dis and Pin Data) table in sql:
# creating the data(Top User Dis and Pin Data) table in sql:

# Data Visualization:
    - Plotly is a Python library used for creating interactive and publication-quality plots. It offers various types of plots such as scatter plots, line plots, bar             charts, heatmaps, and more.
    - Data Evaluation:
          1. def Data_Analysis_1():"Top 10 states by transaction volume."
                - Bar Chart
          2. def Data_Analysis_2():"Top transaction count and type"
                - Pie Chart
          3. def Data_Analysis_3():"Top brands by usage in each year"
                - Pie Chart
          4. def Data_Analysis_4():"Top 10 districts by transaction volume"
                - Bar Chart
          5. def Data_Analysis_5():"Bottom 10 states by transaction volume"
                - Bar Chart
          6. def Data_Analysis_6():"Bottom brands by usage in each year"
                - Bar Chart
          7. def Data_Analysis_7():"Bottom 10 districts by transaction volume"
                - Bar Chart

    - Geo_Visualization:
    For geospatial visualization, Plotly offers a powerful module called Plotly Express, which provides an easy-to-use interface for creating various types of geographic 
    plots.

        - Geo Visualization - Transaction_Data
        - Geo Visualization - User_Data

    - Data Visualiation:
          - Insights
          - Select box: 5 Data Visulaization: ("Total Transaction Amount by Quarter (Animated by Year)",
                                                "Trend of Transaction Counts by Year and Transaction Type",
                                                "Usage of Mobile Brands",
                                                "Amount by Year for each State and District",
                                                "Statistical Representation - State vs Year vs Amount",
                                                "Statistical Representation - State vs year vs count")
