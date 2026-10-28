# Mini-Courier Planner

## Project Overview
Mini-Courier Planner is a Python-based application that helps plan parcel selection and delivery routes. It selects parcels within a van's weight capacity, calculates shortest paths between locations, and estimates a delivery route.

## Objectives
- Sort parcels by priority and deadline.
- Select parcels to maximize total value within the van's capacity.
- Calculate shortest road paths using Dijkstra's algorithm.
- Plan a delivery route using the Nearest Neighbor TSP approximation.
- Measure algorithm runtimes and visualize performance.

## Technologies Used
- Python
- Pandas
- Matplotlib
- NetworkX
- Jupyter Notebook

## Algorithms
1. **Merge Sort:** Sorts parcels by descending priority, then ascending deadline.
2. **0/1 Knapsack Dynamic Programming:** Selects parcels that maximize total value without exceeding the van capacity.
3. **Dijkstra's Algorithm:** Calculates shortest distances between road-network locations.
4. **Nearest Neighbor TSP Approximation:** Chooses the closest unvisited delivery location and returns to the depot.

## Sample Dataset
The project includes:
- `datasets/parcels.csv` — parcel weights, priorities, deadlines, values, and locations.
- `datasets/roads.csv` — road connections and distances.

The sample van capacity is 10 units.

## Sample Results
- Selected parcel weight: 10 units
- Selected parcel value: 250
- Unique delivery locations: 3
- Approximate route: Depot → B → C → D → Depot
- Total route distance: 22 km

These results correspond to the included sample dataset and current algorithm settings.

## Performance Analysis
Runtime experiments measure Merge Sort and Knapsack as the number of parcels increases. The generated charts are saved in the `images/` directory.

- `images/route.png` — road network and delivery route.
- `images/runtime_chart.png` — Merge Sort runtime chart.
- `images/knapsack_runtime.png` — Knapsack runtime chart.

Runtime values depend on the computer and execution environment.

## How to Run
1. Install Python.
2. Install the required libraries:
   ```bash
   python -m pip install pandas matplotlib networkx jupyter
   ```
3. Open the project folder in VS Code.
4. Open `mini_courier_planner.ipynb`.
5. Select a working Python kernel and run the notebook cells from top to bottom.

## Limitations
- The dataset is small and illustrative.
- The route algorithm is an approximation and may not find the globally shortest tour.
- The model uses road distances rather than live traffic or real-time delivery conditions.

## Future Improvements
- Add more locations and realistic datasets.
- Include delivery deadlines in route scheduling.
- Add a graphical user interface.
- Compare the route approximation with other algorithms.

## Project Structure
```text
Mini-Courier-Planner/
├── mini_courier_planner.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── datasets/
│   ├── parcels.csv
│   └── roads.csv
└── images/
    ├── route.png
    ├── runtime_chart.png
    ├── knapsack_runtime.png
    └── screenshots/
```
