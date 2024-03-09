# SQL
Data cleaning and data organization to analyze Covid19 death and vaccinations 

In this README file, I will walk you through my SQL project.

Let's start by uploading the two database, CovidDeaths and CovidVaccines, into BigQuery. 

With the first SQL statement, I use basic skills to overlook the data, focusing on EUROPE. I can isolate the STATE I want to look at by using the WHERE command.

Going forward, I want to compare the total cases vs total deaths, still focusing only on EUROPE. We can do this with a simple division in the SELECT statement.

Next, I compared the total population and total cases to examine how many people in EUROPE were infected.

After analyzing data only from Europe, I decided to compare all the countries and found out the highest death count per population. We can do this by using the MAX statement.
To look a little depper, we can break it down by continents, using GROUP BY.

Doing so, we realize that, becasue of null values, we are getting worng numbers, to fix this problem, I added a WHERE statment that show only continent with a null value.

Now, let's take a look at global numbers. In this STATEMENT, I use SUM to calculate the total death numbers. In the WHERE statment I also mak esure to exclude worng name from the LOCATION column.

This query contains a few steps, first I created a CTE, then I use CAST to change my data type from STRING to INTEGER. As a next step, I use PARTINIO BY which allows me to devide location by sections so that whe I sum the numbre of vaccines, it will start over every time it hit a new location. As you can see, I used a JOIN so that I could gather data from both tables.

With those clean and organized data, I created a TEMP TABLE. Now I can easly look at the data I am interested in.

Next, I created a VIEW that I will use for my TABLEAU project, where I will use those data I"ve workde on to created vizualitanions.
