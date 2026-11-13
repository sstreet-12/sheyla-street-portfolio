| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Title
Text here...

_For each step below, you should document your progress as you move forward.  In terms of tone, think of the writeup as though you're keeping journal of your step-by-step process.   You should include a any insights you gained from the critique method, and what it led you to think about when considering the redesign.  You should talk about how you moved next to the sketches, and any insights you gleaned from your user feedback.  Document what you changed based on the user feedback in your redesign.  Finally, talk about what your redesigned data visualization shows, why you selected the data visualization you did, and what you attempted to show or do differently._

_You can include screenshots, sketches or other artifacts with your narrative to help tell the story of how you moved through the process.  Again, make sure to avoid including any personally identifying information about your interviewees (don't list full names, etc.).  While this template serves as a guide, make sure to reference the assignment writeup on Canvas for the official guidance.  This template does not include all guidance mentioned on the assignment page._

## Step one: the visualization

_Include link to the original data visualization (or screenshot - make sure to correctly cite your sources, etc.).  Include paragraph or two on why you selected this particular data visualization.  For obvious reasons, the data visualization you select should come from a publicly accessible source._

## Step two: the critique
_Don't forget to complete the Google Form found on the assignment page.  You can summarize your thoughts here._

## Step three: Sketch a solution
![Alt text](./images/screenshot.png)

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

_What patterns in the feedback emerge?  What did you learn from the feedback?  Based on this feedback, come up with what design changes you think might make the most sense in your final redesign._

## Step five: build the solution

_Include and describe your final solution here. It's also a good idea to summarize your thoughts on the process overall. When you're done with the assignment, this page should all the items mentioned in the assignment page on Canvas(a link or screenshot of the original data visualization, documentation explaining your process, a summary of your wireframes and user feedback, your final, redesigned data visualization, etc.)._

_Based on my interviews, I realized I needed to put a lot more time and effort into my visualization. I decided to add animated map piece and filtered the bar chart to only include the top country's (China) tomato production over time. This required geocoding the original csv file which was hard because the locations were simply the midpoint of each country to get the map filling on Tableau. To clarify the purpose of the visualization, I also added subtitles with key takeaways (in gray for design purposes) and made my titles more descriptive (black for design purposes). 

While completing my final visualization, looking closer at the data I noticed quirks in the data with regard to China. FAOSTAT lists “China” as a single total that combines China (mainland), Taiwan and Hong Kong. It also lists each of those three separately, so keeping every row would have counted China’s production twice. Since my map shows individual regions, I removed the combined “China” row and kept the mainland, Taiwan and Hong Kong. 

When choosing colors for the map, I grouped production into fixed steps instead of a smooth scale. China produces so much more than any other country that a smooth scale made nearly every other country the same shade of red, which hid differences among middle producers. The tradeoff is that countries within the same step look identical, so I added hover values._

<div class='tableauPlaceholder' id='viz1794539961513' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ma&#47;MakeoverMonday_Final&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='MakeoverMonday_Final&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ma&#47;MakeoverMonday_Final&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1794539961513');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='1000px';vizElement.style.height='827px';} else { vizElement.style.width='100%';vizElement.style.height='877px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>

## References
_List any references you used here._

## AI acknowledgements
_If you used AI to help you complete this assignment (within the parameters of the instruction and course guidelines), detail your use of AI for this assignment here._

