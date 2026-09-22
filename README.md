# FastBox Delivery Simulator

A Python-based logistics simulation that models package delivery across multiple warehouses and delivery agents.

## Project Overview

The FastBox Delivery Simulator assigns each package to the nearest delivery agent using Euclidean distance and simulates the delivery route from the agent's current location to the warehouse and then to the package destination.

The program generates a report containing:

* Packages delivered by each agent
* Total distance travelled
* Delivery efficiency
* Most efficient agent

## Technologies Used

* Python
* JSON
* File Handling
* Mathematical Calculations

## Key Python Concepts

* JSON parsing
* Lists and dictionaries
* Functions
* Loops
* Conditional statements
* Euclidean distance calculation
* File handling
* Data validation

## How It Works

1. Reads and parses the input JSON file.
2. Extracts warehouse, agent, and package information.
3. Calculates Euclidean distance between agents and warehouses.
4. Assigns each package to the nearest agent.
5. Simulates the delivery route:
   `Agent → Warehouse → Destination`
6. Calculates total distance travelled by each agent.
7. Calculates delivery efficiency.
8. Identifies the most efficient agent.
9. Saves the final report as `report.json`.

## Project Structure

```text
fastbox-delivery-simulator/
│
├── fastbox_simulator.ipynb
├── base_case.json
├── test_case_1.json
├── test_case_2.json
├── ...
├── test_case_10.json
├── report.json
└── README.md
```

## Example Output

```json
{
    "A1": {
        "packages_delivered": 2,
        "total_distance": 121.21,
        "efficiency": 60.6
    },
    "A2": {
        "packages_delivered": 2,
        "total_distance": 79.21,
        "efficiency": 39.6
    },
    "A3": {
        "packages_delivered": 1,
        "total_distance": 14.14,
        "efficiency": 14.14
    },
    "best_agent": "A3"
}
```

## Testing

The simulator was tested using the base dataset and 10 additional test cases with different warehouse, agent, and package configurations.

The program successfully processed the test cases and generated delivery reports.

## Assumptions

* Each package is assigned to the nearest agent based on the agent's distance from the warehouse.
* Euclidean distance is used for distance calculations.
* If two agents are equally close, the agent with the smaller ID is selected.
* Packages are processed in the order provided in the input JSON.
* After delivering a package, the agent remains at that package's destination.
* Efficiency is calculated as:

```text
Total Distance / Packages Delivered
```

* Lower distance per package represents better efficiency.

## Learning Outcomes

This project helped me strengthen my understanding of Python programming, JSON data handling, file operations, mathematical calculations, functions, loops, and implementing a real-world logistics simulation.
