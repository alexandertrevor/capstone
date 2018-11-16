# Convoluted Kernel Maze Presentation
Task 35
Trevor Alexander

## While building the maze, we attempted moving 2 cells at a time.

### What would the maze look like when moving a larger number of cells?

The larger number would result in more instances of the end going outside of the maze bounds, thus there would be less pathways. Of course, with a larger number the empty lanes would be longer, so we would be looking at a maze with fewer, longer open pathways.


### What would the maze look like if this number was not constant?

With the number being random, the maze could often look a lot like the result from moving 2 cells as the random number could fall close to 2 often enough, and for any one time where the number was too long (and thus out of the maze bounds), the next time could again return the number 2 or close.


## What algorithms could you use to find a path through this maze? Compare and contrast at least 2.

Two algorithms that could find a path through the maze are A* and Dijkstra's Algorithm

A*
This algorithm would be the most optimal for finding the shortest path through the maze. We would need to input some heuristic data in order for it to work, but fortunately the Manhattan Heuristic would be applicable as the maze only moves up, down, left and right at a known rate. 

Dijkstra's Algorithm
Though this algorithm would not be as optimal for finding the fastest route in comparison to A*, where it could prove more advantagous is if in it's output we wanted to chart a course through the maze that included picking up some Swag. With an additional check within the algorithm, we could not only have it record the distance to a particular point, but also check and record if that particular point has Swag within it. With this data, not only could we find a path to the exit, but chart a course to pick up any number of Swag items (if not all), before exiting the maze.  


## How does knowing the algorithm used to generate the maze influence the best algorithm to solve it with?

Knowing that the maze does, in fact, have an exit helps in choosing A* as the potential best algorithm as we don't need to do any exploratory algorithms (such as DFS). Additionally, having insight into the limitations of how the paths are created, specifically Up, Down, Left, and Right at a constant rate, would allow us to employ the Manhattan Heuristic for the additional required data.

I say "potential" best algorithm as it would depend on the goal. If the goal was to pick up as much Swag as possible before exciting, then as explained in the previous question Dijkstra's Algorith could be more optimal.

## As a patron picking up Swag along the way, how might you best store the list of items you've collected?

For a simple storage of the Swag, a List would do well (swag_bag = []). However, if you wanted to store more information about not only the item, but where you found it, you could go with a Dictionary ( swag_bag = {"Gold": 4d, "Copper": 2b} ).

## If the farmer asked you to sort the items you collected before leaving the maze, what sorting algorithms would you consider using (assume a much larger list of possible Swag)?

With a larger list of Swag, Quick Sort and Merge Sort could both effectively be used.

## How does the quantity and variety of Swag influence your answer?

With a larger list, Bubble Sort starts to become inefficient compared to Merge Sort and Quick Sort. With a small variety of Swag, there is a higher chance that the items could be sorted already, which does not favor Quick Sort. With a greater variety of Swag, the chances of an items falling into order naturally are reduced, and thus Quick Sort could form as well or better than Merge Sort. Given how Merge Sort stores the items in memory, if the list truely becomes large there could be another argument for using Quick Sort.
