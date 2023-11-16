# Module 3 Assignment: Design Study
#### Authors: Sadie Amato, Bailey DeSouza, Ajay Gandecha, Meghan Sun

**Slides**: https://docs.google.com/presentation/d/14IkNABHwWxRch61UaD2hVYvQNx5_0HM-ze1e-8X8vXU/edit?usp=sharing

**Video Presentation**:

## Precondition
### 1. Learn
The US Department of Energy has recently hired us to design a visualization tool to influence future data-driven policy recommendations. More specifically, we are constructing our tool to help reveal how energy consumption of various sources has changed over time and what direction it is trending. Energy consumption and policies differ vastly among sectors, so we were asked to focus on two of the largest populated sectors: residential and commercial. 

The commercial energy sector comprises service facilities and business equipment at all federal, state, and local levels. Energy consumption can commonly be heating, air conditioning, lighting, and powering generators, to name a few examples.  Space heating is the largest energy end-use, accounting for about 32% of energy consumption in 2018. Natural gas and electricity are the two main energy sources used, with about 60% electricity and 34% natural gas usage in 2018. [1]

On the other hand, the residential sector is made up of private households. Typical energy consumption includes heating, air conditioning, cooking, and running appliances. 
The residential sector largely relies on natural gas, petroleum, renewables, and electricity for energy consumption. In the mid to late 1900s, natural gas and petroleum were the most used resources. With time, the sector has grown to rely more on electricity and natural gas [2].
 
It’s important to influence effective energy policy because current US energy use could lead to an unsustainable future. The US makes up less than 5% of the world’s population, yet consumes about 16% of the world’s energy. If current trends continue, the US is estimated to have 66% of energy come from fossil fuels by 2050, which fails to meet the IPCC carbon reduction goals. The emissions of fossil fuels continue to add more greenhouse gasses to our environment [3]. 

Our goal is to make the monitoring of energy trends more accessible. Energy policies are critical in influencing the US's energy habits, and understanding current trends will make such policies more effective. A push towards more energy efficiency has benefits on multiple levels. On an environmental level, it will help lower greenhouse gas emissions, water use, and pollutants. From an economic perspective, more efficient energy use reduces costs for consumers.[4] 
  
This is all to say that it’s becoming more integral to instill policies to use resources better; we aim to influence more energy decisions by the US Department of Energy to be data-driven.

### 2. Winnow
To explore our problem, we need data to provide information about energy consumption trends for both the commercial and residential sectors. Within each sector, we want to know the breakdown of the types of energy resources used and how they change with time. With these factors in mind, we found the USA State energy data provided by the U.S Energy Information Administration (EIA) to be the best fit data for our goals. The US EIA publishes consumption, expenditures, and prices by state, sector, and year; we will use a CSV dataset that combines such variables provided by the CORGIS Dataset project. [5]

The dataset we are using contains US energy data by state spanning from 1960 to 2019. Data about energy consumption, expenditure, and price by state and sector is provided. One factor to be aware of in the dataset is that there may be incomplete information on newer energy resources, such as solar or wind, especially in the residential sector. Additionally, it would be more ideal if we had data on energy consumption through 2022, since that even-more-recent energy usage would also be relevant to our target problem.

Our goal is to show how energy consumption has changed over time, along with the current trends, so that it can help our client make better future energy policies. The two sectors we are focusing on are residential and commercial. The EIA dataset is useful to our question as it provides all these factors. 

To allow us to communicate trends for the US over time properly, we will use the following columns:
- Year 
- State

To gather insight about residential sector energy consumption, we will be looking at the following columns: 
- Consumption.Residential.Coal
- Consumption.Residential.Distillate Fuel Oil
- Consumption.Residential.Geothermal
- Consumption.Residential.Kerosene
- Consumption.Residential.Petroleum
- Consumption.Residential.Natural Gas
- Consumption.Residential.Wood

For the commercial side, we will be looking at: 
- Consumption.Commercial.Coal
- Consumption.Commercial.Distillate Fuel Oil
- Consumption.Commercial.Geothermal
- Consumption.Commercial.Hydropower
- Consumption.Commercial.Kerosene
- Consumption.Commercial.Petroleum
- Consumption.Commercial.Natural Gas
- Consumption.Commercial.Wood
- Consumption.Commercial.Solar
- Consumption.Commercial.Wind

Looking at these columns will be sufficient to support our approach as it provides information about energy consumption in our target sector and breaks the consumption down by energy resource.


## Core
### 1. Discover
In narrowing down the given energy dataset, we decided to focus on energy usage separately in two sectors: residential and commercial. We believe it would be important for the Dept. of Energy to examine past trends in energy sources in these sectors to give their recommendations on future policies. Therefore, we generated our two tasks to enable the department to do just that.
##### Task 1: How does the usage of the different energy sources by the residential sector change over time?
- _Why_ is a task pursued?
  - To support Dept of Energy’s recommendations for residential energy policies 
- _How_ is a task conducted?
  - Look at the makeup of residential energy sources over time and compare this with the ideal source makeup
- _What_ does a task seek to learn about the data?
  - Which energy sources are being used the most (and the least) in the residential sector currently, and how these sources have changed from the past
- _Where_ does the task operate?
  - Residential consumption of coal, distillate fuel oil, geothermal, kerosene, petroleum, natural gas, and wood (across all states and years)
- _When_ is the task performed?
  - During presentation to DoE, when DoE finalizes recommendations, and when DoE presents to policymakers
- _Who_ is executing the task? 
  - DoE and policymakers who form residential energy policies

##### Task 2: How does the usage of the different energy sources by the commercial sector change over time?
- _Why_ is a task pursued?
  - To support Dept of Energy’s recommendations for commercial energy policies 
- _How_ is a task conducted?
  - Look at the makeup of commercial energy sources over time and compare this with the ideal source makeup
- _What_ does a task seek to learn about the data?
  - Which energy sources are being used the most (and the least) in the commercial sector currently, and how these sources have changed from the past
- _Where_ does the task operate?
  - Commercial consumption of coal, distillate fuel oil, geothermal, kerosene, petroleum, natural gas, and wood (across all states and years)
- _When_ is the task performed?
  - During presentation to DoE, when DoE finalizes recommendations, and when DoE presents to policymakers
- _Who_ is executing the task? 
  - DoE and policymakers who form commercial energy policies

### 2. Design
![prototype](prototype.png)
##### Possible Interactive Features We're Considering at this Stage: 
toggle between the Residential visualization view and Commercial visualization view, hover over each point in the line graph to view the specific value, toggle between different years
##### Design Trade-offs:
- Pros:
  - Easy to understand (for most viewers)
  - Good for noticing overall trends and patterns
  - Encourages self-exploration
  - Intuitive 
  - Not overwhelming to the viewer
- Cons:
  - May not be accessible for viewers with color-blindness
  - Prone to “losing” some data and specificity
  - Viewer needs to interact in order to see energy consumption values
  - Not broken down by state; this visualization is for the U.S. as a whole
##### Design Justification: 
With this style of visualization and the color-coding, it’s very clear to the viewer which form of energy consumption is the highest. It’s also easy to see trends within each form of energy and make comparisons. Thus, this visualization could serve useful in trying to find energy consumption trends and create new policies based on the trends.

### 3. Implement
### 4. Deploy
### 5. Iterate

## Analysis
### 1. Reflect pt. 1
### 2. Reflect pt 2
