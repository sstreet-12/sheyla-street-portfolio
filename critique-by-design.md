| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique and Redesign: Tomato Production Visualization

## Step one: Choose the visualization
<img width="293" height="296" alt="image" src="https://github.com/user-attachments/assets/c38c65ab-d55c-48ba-833e-c7d52d06ef6f" />

Link to original visualization: https://www.linkedin.com/feed/update/urn:li:activity:7038221922265915394/

I chose this visualization because it presents a simple question, which countries produce the most tomatoes, in a way that makes the answer hard to see. The animated bar chart race is eye catching, but it moves too quickly to compare countries or follow trends. Since FAOSTAT dataset is clean and spans six decades, the weaknesses come from design choices rather than the data itself, which made it a good candidate for a redesign.

## Step two: the critique
This visualization does a great job of showing how leadership in tomato production has shifted among countries, but it could do more to describe overall tomato production. The main missing element is how total production changes over time. 
The colors stood out to me and are what first drew me to the visualization, but they also create a lot of noise. It can be hard to tell what the authors want the audience to focus on, because each bar is a different color that carries no meaning. This works for aesthetics but hurts perceptibility: when color encodes nothing, readers search for a meaning that isn’t there. The pie chart also adds little meaning. It is overkill, since the bar chart already provides a comparison, and the gray section adds a mystery element. Based on where it was posted (LinkedIn), the audience is a general social media audience. For this audience it is effective on Few’s emotive criteria. The moving bars, bright colors, flags, and tomato background are built to catch attention while people scroll (engagement and aesthetics). In my redesign, I will focus on aesthetics by choosing a more consistent, less noisy color scheme and design. I plan to use one neutral color for most countries and a single highlight color for the story I want to emphasize, such as China’s rise to the top. I’ll also replace the flags and tomato background so the data stands out.


## Step three: Sketch a solution
<img width="310" height="345" alt="image" src="https://github.com/user-attachments/assets/5a10bfb4-d56c-494b-aae1-0048bc4cbe4b" />

## Step four: Test the solution
Interviewer Information: Interviewer 1: 1st year MISM student from China and 2nd year MISM student from Taiwan with AI Engineer work experience. Interview 2: 2nd year Architecture student, studying Building Performance Diagnostics, from India with 2-year work experience as an architect. 

Interview Results:

| Question | Interview 1 | Interview 2 |
|----------|-------------|-------------|
|    What worked?      |       The reduction of the number of countries allowed this person to understand the takeaway: top producing countries.      |     The red palette goes nice with the narrative of tomato production.        |
|      What did not work?    |      They suggested that if I sort by the number of tomatoes in ascending order then the countries that produced more tomatoes would have a darker colored bar on the chart.       |        They suggested that I make sure you can see the full name of the countries or use abbreviations. They also caught a misspelling.     |
|     What questions came up?     |       They said my graph made them curious about the correlation between countries and then they said they realized that the countries toward the end of the graph were the largest countries. Recommended that I add a comment about how the population plays a role in the tomato production. |      They were confused about the time frame and how that impacts the production since my original visualization represented tomato production aggregated across 30 years.|
|       What should I add?   |     Their feedback inspired me to include a title/annotation such as the “top 10 countries by tomato production: China leads”.        |       Add another visual component since this is international:  geocode the data to create a map.      |

Synthesis: 
Most of the feedback came back to clarity: my peers wanted to understand the chart faster. The parts that worked, like cutting down the number of countries, made the chart easier to read. The parts that didn’t work were small things that that slowed interpretation: country names that were cut off, a misspelling, and colors that didn’t clearly match the amount of production.
I learned that small details affect how much a viewer trusts a visualization. A typo or a cutoff label distracts from the main point. I also learned that color must be tied to the data: if darker means more, people expect the order and the shading to agree. Finally, the questions about population showed me that showing raw totals answers “who produces the most” and a good visualization has more than aggregation but breaks up the data. 
Based on this feedback, I made three main changes. First, I made color carry meaning: the map uses a red scale where darker means more tonnes produced. I grouped production into fixed steps so that China’s huge output doesn’t wash out every other country. Second, I fixed the labeling problems by using full, consistent country names and added exact values on hover. Third, I added a title and annotation that state the finding directly.

## Step five: build the solution
Based on my interviews, I realized I needed to put a lot more time and effort into my visualization. I decided to add animated map piece and filtered the bar chart to only include the top country's (China) tomato production over time. This required geocoding the original csv file which was hard because the locations were simply the midpoint of each country to get the map filling on Tableau. To clarify the purpose of the visualization, I also added subtitles with key takeaways (in gray for design purposes) and made my titles more descriptive (black for design purposes). 

While completing my final visualization, looking closer at the data I noticed quirks in the data with regard to China. FAOSTAT lists “China” as a single total that combines China (mainland), Taiwan and Hong Kong. It also lists each of those three separately, so keeping every row would have counted China’s production twice. Since my map shows individual regions, I removed the combined “China” row and kept the mainland, Taiwan and Hong Kong. 

When choosing colors for the map, I grouped production into fixed steps instead of a smooth scale. China produces so much more than any other country that a smooth scale made nearly every other country the same shade of red, which hid differences among middle producers. The tradeoff is that countries within the same step look identical, so I added hover values.

<div class='tableauPlaceholder' id='viz1794539961513' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ma&#47;MakeoverMonday_Final&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='MakeoverMonday_Final&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ma&#47;MakeoverMonday_Final&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
var divElement = document.getElementById('viz1794539961513');                    
var vizElement = divElement.getElementsByTagName('object')[0];                   
if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else { vizElement.style.width='100%';vizElement.style.height='877px';}                    
var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

## References
_https://makeovermonday.vercel.app/dataset/2023w17_


## AI acknowledgements
_I used Claude to help me with Tableau steps for creating my final visualization._

