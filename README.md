
# Seaborn Lesson Plan

**Course**: DS   <br/>
**Mod**: Module 1                    <br/>
**Topic**: Good visualization & Seaborn                  <br/>
**Amount of time**: 1.5 hours <br/>
**Author**: Alison Peebles Madigan.  
Ported from the ds-lesson-starters-repo [here](https://github.com/learn-co-curriculum/ds-lessons-starter/tree/master/lesson-plans-by-mod/Module-1/vizualizations-seaborn). 

**Learning goals:**
- Create a list of best practices for data visualization
- Identify the differences between matplotlib and seaborn
- Create a visualization with seaborn, applying best practices

Timing: Each section should take half an hour. Please remind them to be mindful of time it takes them to present.

***
Activation:
[image](https://pbs.twimg.com/media/DNTFhGaXcAEbrMO.jpg)
What's wrong with this visualization?


**Learning goals:**
- Create a list of best practices for data visualization
- Identify the differences between matplotlib and seaborn
- Create a visualization with seaborn, applying best practices


Intro:
We see data visualizations every day. Good, Bad, misleading... 
I'm sure we've all picked up some ideas of what makes a good visualization vs not. 
There is going to be an opportunity to share those, but first let's review what OTHER people view as best practices. 

_Instructions_
(have them count off by six)

Each group will review an article and write the key points on what to DO, vs what to AVOID, and at the bottom there is a section for "Student wisdom" where you can put your own recommendations. 


**MAKE YOUR OWN COPY OF THIS SOURCE DOC FOR THE LESSON**
The link to the google doc is here:  [original doc](https://docs.google.com/document/d/1KdwfZpwZWhTJr2agcyuzPhV-GqZD9ZI5_uBU0_92eIc/edit?usp=sharing


## Learning Goal 1: Create a list of best practices for data visualization

Documenting best practices:

In groups: [article 1](https://www.jackhagley.com/What-s-the-difference-between-an-Infographic-and-a-Data-Visualisation), [article 2](https://thoughtbot.com/blog/analyzing-minards-visualization-of-napoleons-1812-march), [article 3](http://dataremixed.com/2016/04/the-design-of-everyday-visualizations/), [article 4](https://visme.co/blog/data-storytelling-tips/),  article 5: Visualizations That Really Work.pdf (in folder), [article 6](https://www.tableau.com/learn/articles/best-beautiful-data-visualization-examples)

To fill in: [Best practices doc](https://docs.google.com/document/d/1yf3OfuM3C-hOaQKxz49ARDdXbujBTHXPMeIglUQSAEc/edit?usp=sharing) 


## Learning Goal 2:  Identify differences between seaborn & matplotlib


- [Resource](https://python-graph-gallery.com/seaborn/)
- [seaborn](https://seaborn.pydata.org/)


### Two different plots

- COLD CALL someone in the room to ask them to explain what this matplotlib code is doing

#### Matplotlib
```
import matplotlib.pyplot as plt
import pandas as pd

# Initialize Figure and Axes object
fig, ax = plt.subplots()

# Load in data
tips = pd.read_csv("https://raw.githubusercontent.com/mwaskom/seaborn-data/master/tips.csv")

# Create violinplot
ax.violinplot(tips["total_bill"], vert=False)

# Show the plot
plt.show()
```

VS

#### Seaborn

- COLD CALL SOMEONE ELSE to take a stab at reading what this code is doing, even though they have never seen seaborn before

```
import matplotlib.pyplot as plt
import seaborn as sns

# Load the data
tips = sns.load_dataset("tips")

# Create violinplot
sns.violinplot(x = "total_bill", data=tips)

# Show the plot
plt.show()
```
[reference shown here](https://www.datacamp.com/community/tutorials/seaborn-python-tutorial#sm)

#### Point out the differences
Ask what *they* see as the differences first, then confirm:
- there is no plot initialization
- you load the dataset into the sns environment
- then you reference the specific dataset and variables within the plot creation command

#### Ask:
- do you find one more readible than the other?

### In depth comparison:

#### Groups 1:3

For each plot:
- How is the code to create it different from the maplotlib code?
- What are the customization options? 
- What are the top 3 most important customization options to know(with code) ?

Group 1 - [histograms](https://python-graph-gallery.com/histogram/)<br>
Group 2 - [scatter plot](https://python-graph-gallery.com/scatter-plot/)<br>
Group 3 - [boxplot](http://python-graph-gallery.com/boxplot/)<br>

#### Groups 4:5
- What new vocabulary was introduced in these posts?
- What is the benefit of these new options?
- What code/options do you need to know? 

Group 4 - [diverging, sequential, discrete color palattes](https://python-graph-gallery.com/101-make-a-color-palette-with-seaborn/)<br>
Group 5 - [seaborn themes](https://python-graph-gallery.com/104-seaborn-themes/) <br>

#### Group 6:
[seaborn themes w matplotlib](https://python-graph-gallery.com/106-seaborn-style-on-matplotlib-plot/)
How does this work?



## Learning Goal 3: Create a visualization with seaborn, applying best practices
Time to work: 20 min<br>
Time to present: 10 minutes

[exercise from data world](https://data.world/makeovermonday/2018w37-paying-the-president)

## Reflection:
(message Data Science Coaches)
- What worked from this training? 
- What can you apply moving forward?
- What's one concept you would like to practice more?

#### For extra fun:
[visualization challenges](http://www.storytellingwithdata.com/blog/2019/3/1/swdchallenge-visualize-this-data)

[seaborn cheatsheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf)

http://www.storytellingwithdata.com/blog/2019/3/1/swdchallenge-visualize-this-data