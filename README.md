# Quantitative-Biol

## Paragraph of my data

I'm a first-year student Masters' student at the department of Fish and Wildlife Conservations and my research focuses on the egg development of Bluehead chub fish. Currently I don't have any research data but I'll be working to build a dataset during the upcoming summer. The dataset will specifically explore the egg development of bluehead chub under different temperature and oxygen conditions. To collect this data, we will obtain eggs from a stream, examine them under a microscope, capture images, and then place them in water tanks at high (24 degrees Celsius), medium (21 degrees Celsius), and low (18 degrees Celsius) temperatures. My aim is to observe the duration it takes for the eggs to progress from one stage to another, with the larvae's oxygen consumption rate influenced by temperature. Microscopic images will be a key tool in our data analysis. We'll regularly assess the eggs, checking their stage, condition, color change, pigmentation, gender, and if they've been affected by fungus. This research helps us understand the complex process of Bluehead chub fish egg development in specific environmental conditions. We'll also explore how temperature changes affect pH and oxygen concentration, aiming to identify the impact of temperature and oxygen on the fish's entire lifespan, from egg to adult. 

Since I currently lack original data, I've found an online data that aligns well with my research focus and thesis project. I would like to work with this data for my regular assignment. This data explores the predicted lifespan of Comet goldfish, investigating how various factors such as the environment and habitat influence their lifespan. It is specifically about how average length, weight, color changes, and the lifespan of Comet goldfish  influenced by factors such as water quality, including pH levels, habitat conditions, and specific genetic characteristics. Both projects involve studying the impact of environmental conditions, including temperature and oxygen levels, on the development and lifespan of the respective fish species. Working with the online data for my regular assignment is appealing because it complements and enhances the insights gained from my research on Bluehead chub fish. It provides a broader perspective on factors influencing fish lifespan, offering valuable comparative data that contributes to a more comprehensive understanding of the subject. The combination of these datasets allows for a more robust analysis and strengthens the overall findings of my research.

### List of goals
1. Environmental Impact Analysis
2. Correlations of different environmental factors 
3. Regression analysis of fish life span
4. Principal component analysis
5. Cluster analysis 





# Week 1

#### Worked on fish_data.csv
#### read and View data in R
#### Explored the structure of different columns and what are they
#### Explored dimensions of your dataframe and What does this mean.
#### Selected a column using square brackets and logical statements
#### made summary of data and What does this give
#### Calculated of data with adding a column
#### Use base R to aggregate data  

## Code used in Week 1
data file used- fish_data.csv
fish_data = read_csv("fish_data.csv")
View(fish_data)

fish_data[ , 'ph_of_water' ]

fish_data[ fish_data$ph_of_water > 7 , 'ph_of_water']

summary(fish_data)

fish_data$double_ph_of_water = fish_data$ph_of_water * 2
head(fish_data)

aggregate(ph_of_water ~ habitat, data = fish_data, FUN = mean)

aggregate( average_length ~ habitat, data = fish_data, FUN = mean)

aggregate( average_length ~ habitat, data = fish_data, FUN = sum)

aggregate( average_length ~ habitat, data = fish_data, FUN = max)

aggregate( average_length ~ habitat, data = fish_data, FUN = min)


## Column description

1st colum: id: An identifier or unique code assigned to each fish in the dataset.

2nd colum: average_length: The average length of the fish. unit in inches.

3rd colum: average_weight: The average weight of the fish. unit in ounces

4th colum: habitat: Describes the natural environment or type of habitat where the fish is typically found.

5th colum: ph_of_water: Represents the pH level of the water where the fish is commonly found.

6th colum: color: Indicates the color or colors associated with the fish.

7th colum: Gender: Specifies the gender or sex of the fish, True for "Male," False for "Female,".

8th colum: life_span: Represents the targeted lifespan of the fish.







