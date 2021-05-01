# Designing-of-Pacman-Search-Agents-using-various-AI-Search-Algorithms

• Implemented Finding a Fixed Food Dot strategy using DFS & BFS and also find lowest cost path using Uniform Cost Search    (UCS) Algorithm. Also build A* Algorithm which used heuristic to finds the optimal solution which is slightly faster than UCS.

• Finding all the corners of the maze using admissible, consistent and non-trivial Heuristic was another part of the project. Last part of the project was implementation of algorithm for eating all the Pacman food in as few steps as possible and Suboptimal food Search.

  
• Commands for Various Search Actions:

1. **Finding a Fixed Food Dot using Depth First Search (DFS)**

		python pacman.py -l tinyMaze -p SearchAgent -a fn=tinyMazeSearch
           
		python pacman.py -l tinyMaze -p SearchAgent
		
		python pacman.py -l mediumMaze -p SearchAgent
		
		python pacman.py -l bigMaze -z .5 -p SearchAgent
		
		
2. **Finding a Fixed Food Dot using Breadth First Search (BFS)**		

		python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs

		python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5
		
**eight-puzzle search problem**

		python eightpuzzle.py
		
3. **Varying the Cost Function**		

		python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs

		python pacman.py -l mediumDottedMaze -p StayEastSearchAgent

		python pacman.py -l mediumScaryMaze -p StayWestSearchAgent
		
4. **A-star search**		

		python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic 

5. **Finding All the Corners**

		python pacman.py -l tinyCorners -p SearchAgent -a fn=bfs,prob=CornersProblem

		python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem
	
6. **Corners Problem: Heuristic**

		python pacman.py -l mediumCorners -p AStarCornersAgent -z 0.5
		
	AStarCornersAgent is a shortcut for

		-p SearchAgent -a fn=aStarSearch,prob=CornersProblem,heuristic=co rnersHeuristic

7. **Eating All The Dots with Minimum Path Cost Problem**

		python pacman.py -l testSearch -p AStarFoodSearchAgent
		
	AStarFoodSearchAgent is a shortcut for
	
		-p SearchAgent -a fn=astar,prob=FoodSearchProblem,heuristic=foodHeuristic

8. **Suboptimal Search Problem (always greedily eats the closest dot)**

		python pacman.py -l bigSearch -p ClosestDotSearchAgent -z .5
