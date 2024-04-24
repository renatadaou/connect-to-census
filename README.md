# connect-to-census - bilingual schools in NYC dataset

For my master's project, I have been exploring rhe new immigration wave to the US with a particular focus on children's access to education. I want to explore How being an immigrant at a young age influence children's upbringing and their access to education. 

## outcomes

Hispanic population and median income:
   - Areas with higher median income tend to have a lower percentage of Hispanic population, and vice versa.
    
Program type vs Hispanic population vs median income:
    - Transitional Bilingual Education programs are more prevalent in areas with higher Hispanic population percentages.
    - What’s up with places with high income, a few Hispanic populations, and a lot of Spanish language programs (both types,  more specific dual language)? 
    - Generally, areas with a high Hispanic population have a great number of both programs, but in areas with a low Hispanic population, and high income have         more dual language schools.

Program Type vs General/Special Education:
    - More transitional Spanish schools have special education programs. Why?
    
Program types vs Hispanic percentage estimate:
    - There isn't enough evidence to reject the null hypothesis of no difference between the two program types in terms of Hispanic percentage estimates.
Median Incomes vs Program Types:
    - There’s a significant difference in median incomes between communities with Dual Language programs and those with Transitional Bilingual Education programs.



## methodology
### Part 1: Geocoding your data and joining it with Census data

1. In the `connect-to-census.ipynb` notebook, add code to:

    a. download your data
    b. convert addresses --> lat/long (if the data doesn't already have lat/long)
    c. convert lat/long to census geography codes (like 'GEOID', 'STATE', 'COUNTY', 'TRACT', 'BLOCK', etc...). you may want to have more than one level of geography so you can do the analysis at different levels later on.
    d. this notebook should output a file containing your data and the census geographies you're interested in.

    Example notebooks to help you with all this will live in [this repository](https://github.com/data4news/census-examples). You may use R or Python (or a combination of the two).


2. In `merge-with-census.ipynb` notebook, download some census data using `tidycensus` and merge it with your data.

### Part 2: Exploratory Data Analysis

1. In the `distributions.ipynb` notebook, do some basic exploratory data analysis on **your dataset** in one dimension. Here you will explore the **distributions** of your data (histograms, boxplots, dotplots, etc).

2. In the `scatterplots.ipynb` notebook, do some basic exploratory data analysis on your data, but this time, merge in some census variables you're interested in and make some **scatterplots** with a variable from **your dataset** as the Y and variables from the **census data** as the X. 

### Part 3: Write up your findings

1. In a new google doc, summarize what you've found so far. Think of this as a short memo of what you've done or the progress you've made towards pitching a story on this topic or using this dataset. You don't need to show all the charts, just the one you found most interesting. What questions do you have that you'd like to dig more into? Do you think you've got an idea for a story angle? Write it informally as a memo to Dhrumil and Aishi (your editors). 

### Part 4
Now add one more `linear-regression.ipynb` . In this notebook you’ll use linear regression as a tool of exploratory data analysis. Remember, regressions are a way to put a “line of best fit” through a scatter plot. So you can use the scatterplots you’ve already made as a starting point. Or you can make new scatter plots. 

### Part 5: Hypothesis Test: Journalistic —> Statistical Inquiry

In `hypothesis-test.ipynb` come up with **at least two** hypothesis tests that will assist you with answering your journalistic questions. For each test:

1. Write the null and alternative hypothesis
2. Make a chart of the distributions you’re comparing
3. Run the t-test or chi-squared test
4. Interpret the result

Write about what you can and cannot conclude based on the test in plain english. Make sure to mention any caveats.

## Usage

1. Rename `.env.example` to `.env` and put in your census API key. 
   
    _(FYI there is a file in this repo called `.gitignore` that will prevent `.env` from being tracked by git so you don't push your census key on accident._

2. Run the notebooks. If you're unfamiliar with this setup, see https://github.com/dmil/jupyter-quickstart/

