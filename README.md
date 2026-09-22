# fastbox-delivery-simulator
Python-based logistics simulation that assigns packages to the nearest delivery agent, calculates delivery distances and efficiency, and generates a JSON report.


# FastBox Delivery Simulator

A Python-based logistics simulation that models package delivery across multiple warehouses and delivery agents.

## Project Overview

The FastBox Delivery Simulator assigns each package to the nearest delivery agent using Euclidean distance and simulates the delivery route from the agent's current location to the warehouse and then to the package destination.

The program calculates:

* Packages delivered by each agent
* Total distance travelled
* Delivery efficiency
* Most efficient agent
* Final delivery report in JSON format

## Technologies Used

* Python
* JSON
* Mathematical calculations
* File handling

## Key Python Concepts

* JSON parsing
* Dictionaries and lists
* Functions
* Loops
* Conditional statements
* Euclidean distance calculation
* File handling
* Data validation

## Project Structure

```text
fastbox-delivery-simulator/
│
├── fastbox_simulator.py
├── base_case.json
├── test_case_1.json
├── test_case_2.json
├── ...
├── test_case_10.json
├── report.json
└── README.md
```

## How It Works

1. Reads the input JSON file.
2. Extracts warehouse, agent, and package information.
3. Calculates the Euclidean distance between agents and warehouses.
4. Assigns each package to the nearest agent.
5. Simulates the delivery route.
6. Calculates total distance and efficiency for each agent.
7. Identifies the most efficient agent.
8. Saves the final results to `report.json`.

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

The simulator was tested using multiple JSON input files with different warehouse, agent, and package configurations.

## Learning Outcome

This project helped me practice Python programming, JSON data handling, distance calculations, file operations, and implementing a real-world logistics simulation.

