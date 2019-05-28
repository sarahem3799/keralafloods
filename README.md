# keralafloods

Objective:
The objective is to attempt to help the residents of cities affected by the floods in Kerala. 
This is done by visualising the road map of Kerala as a graph with the nodes being the prominent cities in Kerala, 
and the edges being the roads connecting the cities. Using centrality measures (such as degree, closeness, and betweenness) 
the closest unaffected cities are identified and the people who have experienced loss (such as the destruction of their houses, 
having severe injuries, and/or deaths) can be aided. These unaffected cities can act as relief areas for the people of 
affected cities and as distribution centres for goods and funds to these people.

Methodology:
Firstly, a dataset is made by using the road map of Kerala to create the graph. This will consist of the distance between cities. 
Thus, the edges that are used will be valued. Using the distances between each city, the most prominent city (which will be found using 
the prestige of cities), etc., a data set is created that will consist of all this relevant information.
The dataset will consist of the distances between cities with a direct path between them. 
For cities that have only indirect paths between them, the shortest path will be calculating by adding the distances of the roads
in this path. The dataset will also consist of information regarding whether or not a particular city is affected or not. 
The programmer will feed this information to the dataset. The names of affected and unaffected cities are derived from the internet
After this analysis of each city’s centrality is performed based degree, betweeness and closeness.
The most important cities are analysed for distribution by taking into consideration the betweenness of cities, 
the closest relief areas to the affected cities on the basis of degree values, and which cities are in need of most help by 
examining which cities have the smallest closeness values. The closest cities are identified using the degree and geodesic values 
between cities. Once the cities with largest betweenness values are obtained, this helps in identifying the cities that are most important 
for transport of goods through indirect paths. For unaffected cities, closeness values is identified as well, as they can provide 
insight into which cities need more help (those with low values of closeness) in comparison to other cities (those with larger values 
of closeness).

Algorithm:
1. Start
2. Import networkx library of Python.
3. Create a graph G with nodes labelled from 1 to 35.
4. Add the weighted edges from the dataset.
5. Compute the degree centrality, closeness centrality and betweenness centrality for each node using the inbuilt functions of networkx 
library of the unweighted graph.
6. Find the maximum for all three centrality measures.
7. Print the maximum values.
8. Compute the degree centrality for each node while considering weights using the formula:
q = q+s;
print("Sum of weights: ")
print(q)
for (r,s) in G.degree(weight='weight'):
p = s/q;
W_D.append(p);
p=0;
9. Compute the maximum weighted degree centrality and print it.
10. Compute the closeness centrality for each node using inbuilt functions from networkx library while considering weights this time.
11. Compute the maximum weighted closeness centrality and print it.
12. Compute the betweenness centrality for each node using inbuilt functions from networkx library while considering weights this time.
13. Compute the maximum weighted betweenness centrality and print it.
14. On the basis of the maximum values of degree, closeness, and betweenness, find the most important city and print it.
15. If the most important city amongst all cities is affected by floods, create two separate subgraphs consisting of the affected and 
unaffected cities respectively.
16. Apply steps from 8 to 14 for the graph of unaffected cities.
17. Using the inbuilt function to calculate the shortest path between two nodes using the Dijkstra algorithm, calculate the shortest 
paths to each unaffected city for an affected city.
18. Calculate and print the minimum of the shortest paths for each affected city, along with the node number of the unaffected city 
to which this shortest path exists.
19. Print the list of all the cities and prompt the user to input a specific city’s number.
20. Check if the city is affected or not, if not, print that it is an unaffected city
21. If affected, print that it has been affected, and then refer to the list created in 19 and print the distance to the nearest 
unaffected city along with the index number of that unaffected city.
