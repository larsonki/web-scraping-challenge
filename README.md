# Mission to Mars

In this activity, the following tools were used to scrape, store and visualize data relating to the fourth planet from the sun **Mars**:
- Jupyter Notebook
- Python
- Pandas
- Splinter
- Beautiful Soup
- HTML
- Matplotlib
- MongoDB

### In the first part of the activity, titles and summaries for articles relating to Mars were scraped from [Mars News](https://redplanetscience.com/).
 - Once the initial connection was set-up with the news link (using Splinter), the HTML elements relating to the particular pieces of information needed were identified.
 - Using the HTML elememts, a loop was created to extract the title and summary of each article which was then stored in a dictionary. Each dictionary was then simultaneously appended to a list as well as a Mongo Database. Each title and summary was also printed as the loop was running.
### In the second part of the activity, an HTML table was scraped to be reformated into a DataFrame and then analyzed and visualized. The information was scraped from [Mars Temperature Data](https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html).
 - Similarly to the section above, a connection was created to connect the Jupyter Notebook to the temperature data using Splinter. HTML elements were identified and then used to scrape the table on the website and store it in lists. As the lists were created, each piece of data was converted to its respective data type.
 - From there, a DataFrame was created using the lists and column headings matching the original table. Any data that was not transformed during the scrape, were updated at this point.
 - The DataFrame was then used to visualize the data using Matplotlib answer the following questions:
 1. How many months exist on Mars?
    - 12 months
    - ![Bar Chart displaying # of Transmissions for each Martian month](/output/martian_month.png)
 2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    - 1,867 individual days
 3. What are the coldest and the warmest months on Mars (at the location of the Curiosity)?
    - Coldest Month - 3rd month
    - Warmest Month - 8th month
    - ![Bar Chart displaying Average Temp in Degrees Celsius by Martian Month](/output/min-temp.png)
 4. Which months have the lowest and the highest atmospheric pressure on Mars?
    - Lowest Atmospheric Pressure: 6th month
    - Highest Atmospheric Pressure: 9th month
    - ![Bar Chart displaying Average Atmospheric Pressure by Martian Month](/output/pressure.png)
 5. About how many terrestrial (Earth) days exist in a Martian year? That is, in the time that Mars circles the Sun once, how many days elapse on Earth?
    - Approx. 675 Earth days are in one Martian year
    - ![Line Graph displaying the daily min temp over time](/output/martian_year.png)