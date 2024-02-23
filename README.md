# Sytner.InterviewApi

## Overview
This Interview API, is for you to demonstrate your abilities to build and manage a RESTful API. 

Some tips:
- You are free to use the internet for reference as you would normally
- You can assume the stakeholder is very amenable, and will go with your sensible suggestion if the acceptance criteria are not completely clear
- The design of the API is expected to follow REST principles
- We commonly use clean architecture at Sytner
- Your code is expected to be covered by appropriate unit tests
- Your code is expected to have appropriate documentation
- We recommend using Entity Framework and Microsoft SQL for any database you create
- For brevity we do not expect you to implement permissions in your API (for example consumer vs administrator)

A class library called Sytner.Utilities is included in this project, which will provide a taste of shared code at Sytner. We would encourage you to try and include this code in your project. 

## Tasks

**1) As a consumer of the API, I want to receive a weather forecast summary that accurately reflects the temperature, so that it is more meaningful.**

Given I am a consumer of the API  
When the temperature is equal or below 0  
Then I see the summary is "Freezing"  

When the temperature is above 0, but equal or below 10  
Then I see the summary is "Chilly"   

When the temperature is above 10, but equal or below 20  
Then I see the summary is "Mild"  

When the temperature is above 20, but equal or below 30  
Then I see the summary is "Warm"  

When the temperature is above 30, but equal or below 40  
Then I see the summary is "Sweltering"  

When the temperature is above 40  
Then I see the summary is "Scorching"  

**2) As an administrator of the API, I would like to be able to add my existing weather stations, so that I can associate my weather forecasts with a specific location**

Given I am an administrator of the API  
When have a weather station, which includes a code, name, latitude and longitude  
Then I can add the weather station via the API  

**3) As an administrator of the API, I would like to add future weather forecast data, so that I can keep my clients up to date**

Given I am an administrator of the API  
When have a new piece of temperature data (in centigrade), including date, temperature and weather station.  
Then I can add it to the API  

When I have an updated piece of temperature data (in centigrade), including date, temperature and weather station.  
Then I can update the API

**4) As a user of the API, I would like to search for weather forecasts over a period of time, for a particular weather station, so that I can plan my time.**

Given I am a consumer of the API  
When I call the API with a weather station and date range  
Then I receive a list of relevant weather forecasts for that range  


