
# Project outline

My simulation aims to analyze the spread of the fire over the grid of 100 x 100 cells under different environmental conditions, like variability in tree densities in the cells and dynamic wind incorporation. By building this model, I want to measure several key outputs like the rate of fire spread across the grid, the total burnt area, and the identification of the high-risk cells prone to catching fire in the area of Arnstein, east of Frankfurt, Germany. The region was chosen due to its variability in tree densities ranging from 0 to 100. 


# The rules of the simulation
1. Each cell in a grid can incorporate one of the three states: “no_fire,” “burning,” and “charcoal.”
2. **“No_fire”** state represents the not yet affected cell by the fire
3. **“Burning”** represents the cell being on fire due to factors like proximity to other burning cells, the cell’s tree density, wind direction, and strength.
4. **“Charcoal”** means that the cell has already been on fire and has been completely burned out which does not allow the cell to contribute to the spread of the fire. 
5. The simulation starts a fire randomly in one cell to simulate the initial ignition. 
6. The wind direction and strength dynamically change the probability of the fire spreading from the burning cell to the immediate neighbors. The probability is impacted by:
7. Probability of percolation: Corresponds to the probability of percolation calculated based on the tree density.
8. Wind Adjustment: Corresponds to the alignment of the wind direction with the vector pointing from the burning cell to the neighbor. 
9. The wind direction and the strength can randomly change throughout the simulation, where the wind direction can take one of the eight wind directions: North, South, East, West, Northeast, Northwest, Southeast, and Southwest. 
10. The simulation is built on the Moore neighborhood and accounts for the eight wind directions, allowing each cell to interact with all eight immediate neighbors. 
11. The simulation does not wrap around the grid, allowing it to mimic the real world more closely
