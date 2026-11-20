# Week 2

Having changed my degree after my first semester, I have seen first-hand the differences in classrooms and lecture halls between faculties and departments. Of course, this applies not only to majors but also to any electives taken outside of one's major. I think it would satiate my curiousity to use these data tools to compile information about Carleton classrooms and lecture halls, classifying them by size, use, what features they do or do not have, when their were made, and, importantly, their building. What does each building offer in terms of pros and cons for their rooms? How does the student experience differ based on these qualities?

# Week 3

Following Dr. Graham's email, I read the opening to Embedded Pedagogies by Brandon Walsh, discussing spatial rhetoric specifically in terms of university classrooms. His discussions on how a room's construction may, prescriptively or descriptively, point to a guided vision for the relationship between the educators and students. How a bolted desk might symbolize a sort of totalitarian prison system, as a hyperbolic example. What this made me think about was: In tracking the age of classrooms, might it be a valuable indicator of progression (or regression) based on subjective reports from students and educators alike? I worry not to veer away from digital archaeology in attaining what resembles a survey that may be found in a psychology or sociology class, but I think it could be an interesting way to gauge quality. (Though is archaeology really interested in "quality?" Or would that be more of an Art History student's interpretation of the work?) I will try to find resources/readings about the exact parameters of archaeological projects.

Aside from that, I thought about using KoboToolbox for inputting basic information about the rooms: What building were they in, their type, their size, their features, their dimensions, their desks and chairs, their colours, their boards, their doors, whether there was writing/graffiti on the walls, and potentially some more.

# Week 4

Following last week, I created a KoboToolbox data set to input some rooms in. I will start adding entries to this next week. Additionally, I might try my hand at replicating a Python code that handles data like the one from this week's burial sites.

Here is the set I have right now: https://ee.kobotoolbox.org/x/LFsjmE72

# Week 7

This week I began making a script in R modelled off this week's sample script used for the family gravestone exercises. So far, it can take the exported .csv from KoboToolbox and define its values into "rooms", then extract individual rooms by a specific identifier into a variable "nodes." Though much of this was from the exercise, I had to learn a lot about R from StackOverflow. This includes what the dollar sign does, how the brackets work, what the parameters are for read.csv, what c means, et cetera. It is attached.

The following are some of the websites/resources I used to find out more about these things:
- https://stackoverflow.com/questions/42560090/what-is-the-meaning-of-the-dollar-sign-in-r-function
- https://www.reddit.com/r/RStudio/comments/1g6gaoq/how_do_we_know_when_to_use_brackets_in_r/
- https://www.stat.ubc.ca/~jenny/STAT545A/block03_basicObjects.html
- https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/paste
- https://stackoverflow.com/questions/17075529/subset-based-on-variable-column-name
- https://r.tiid.org/loading-data-and-subsetting.html
- https://www.rdocumentation.org/packages/COVID19/versions/2.0.3/topics/read.csv

# Week 8

This week I continued working on my graph theory script. However, upon revisiting my work, I realized that I was just trying to blindly apply the graph theory stuff to my PDAP without considering what that would actually give me. I did some surface-level research on how different networks are compared, and realized that the geographical networks of the exercises we did last week would not give me much out for my specific subject. It would just tell me where the rooms are on campus, I believe. So I wondered if I could use this graph theory to kind of track the differences between the rooms and how, for example, a room being a lecture hall might make it more likely to have a certain colour of wall, based on its similarity or not to another room with a lecture hall, etc. I stumbled (by looking at a bunch of Google Searches and forums) on Gower's distance, which is apparently a big deal in this kind of stuff. It basically tracks how similar two things are based on more than one aspect of them. This was great because there is a package called cluster in R that has the daisy() function to calculate the Gower distance. I set my sets on turning my script into that purpose. This sent me on a long-winded rabbit hole of trying to figure out how I can turn the results of a Gower distance calculation into my edge list. With the help of Google, Stack Overflow, et cetera, I managed to create an edge list that I think should work? I don't have enough entries into the KoboToolbox yet to actually confirm or check it -- and I'm still not entirely sure how everything works -- but it passes the surface check, at least. At the end of the script, I tried pasting in the graphing code for the closeness centrality calculation from the Week Seven sample code, but it didn't work. I will try next week to read these errors and debug in order to try and plot the data I have. Perhaps it's just because there aren't enough entries? I will do that also. I tried to collect all my sources hence:
- https://www.rdocumentation.org/packages/cluster/versions/1.2-2/topics/daisy
- https://www.jstor.org/stable/2528823?origin=crossref
- https://search.r-project.org/CRAN/refmans/StatMatch/html/gower.dist.html
- https://stat.ethz.ch/R-manual/R-devel/library/cluster/html/daisy.html
- https://stackoverflow.com/questions/43424761/what-are-the-practical-differences-between-factor-and-string-data-types-in-r
- https://stats.stackexchange.com/questions/22212/gowers-dissimilarity-index
- https://www.w3schools.com/r/r_matrices.asp
- https://www.rdocumentation.org/packages/data.table/versions/1.18.6.1/topics/as.matrix
- https://en.wikipedia.org/wiki/Edge_list
- https://stackoverflow.com/questions/13204046/how-to-create-an-edge-list-from-a-matrix-in-r
- https://stackoverflow.com/questions/33046636/difference-between-as-data-framex-and-asx-data-frame
- https://www.datanovia.com/learn/programming/data-wrangling/rename-columns-in-r
- https://r.igraph.org/reference/graph_from_data_frame.html
