# Capacitated Vehicle Routing Problem for Waste Collection Repository with Time Windows

## Introduction

This repository provides a decision support tool for the dispatcher of A.F. Valput, a waste collection and processing company in Belgium. The company has experienced rapid growth, resulting in complex situations and conditions both legally and practically. To optimize waste collection, this project addresses the Capacitated Vehicle Routing Problem (CVRP) with time windows, considering various constraints.

The objective of this project is to develop a realistic decision support tool that can efficiently plan waste collection routes, considering factors such as vehicle capacity, time windows, waste types, and customer specifications. The simulated annealing algorithm is used to find near-optimal solutions for this combinatorial optimization problem.

## Input Data

The input data includes detailed information about the 30 customers whose waste needs to be processed in 4 waste processing facilities. Each customer has a specific volume of demand, and containers of various sizes are used to meet these demands. The trucks start their routes from the depot in Kampenhout and must return to the depot by 5 PM. Constraints related to time windows, waste type, waste processing facility, and customer-specific requirements are defined in Table 1.

Please refer to the provided sample example for the format of the input data, including client locations, types of containers, and types of companies.

The distance matrix used in the optimization process was calculated in QGIS, which takes into account the geographical coordinates of the client locations.

## Constraints

The following constraints are considered in the waste collection problem:

1. Waste from garages, laboratories, electronics (dangerous waste), and construction waste can only be dumped in Antwerp.
2. Dangerous waste can only be dumped at the facility in Antwerp.
3. Dangerous waste must be dumped between 1 PM and 4 PM.
4. Restaurants must be serviced before noon.
5. Clients 4, 14, 19, 26, and 29 must be serviced before noon.
6. Regular waste collection hours are between 7 AM and 5 PM.
7. Clients 1, 13, 19, and 24 require an additional handling time of 15 minutes due to administration.
8. Bookstore clients require the same container to be returned.
9. Client 12 is a new client, and client 24 is at the end of their contract.

These constraints play a crucial role in optimizing the waste collection routes and ensuring compliance with legal requirements and customer preferences.

## Sample Example

Here is a sample example of the input data for the waste collection problem:
| Client | Location          | Container Size | Company Type         |
| ------ | ----------------- | -------------- | -------------------- |
| 1      | Antwerpen         | 20 m3          | Bookstore            |
| 2      | Grimbergen        | 15 m3          | Bookstore            |
| 3      | Leuven            | 20 m3          | Fish Shop            |
| 4      | Mechelen          | 18 m3          | Restaurant           |
| 5      | Zaventem          | 15 m3          | Garage               |
| 6      | Gent              | 20 m3          | Construction Company |
| 7      | Waver             | 20 m3          | Bookstore            |
| 8      | Hasselt           | 18 m3          | Laboratory           |
| 9      | Luik              | 20 m3          | Vegetables           |
| 10     | Boutersem         | 20 m3          | Construction Company |
| 11     | Boom              | 18 m3          | Fish Shop            |
| 12     | Duffel            | 20 m3          | Electronics          |
| 13     | Brussel           | 20 m3          | Vegetables           |
| 14     | Leuven            | 15 m3          | Restaurant           |
| 15     | Brugge            | 20 m3          | Garage               |
| 16     | Zonhoven          | 20 m3          | Bookstore            |
| 17     | Mol               | 20 m3          | Bookstore            |
| 18     | Herentals         | 20 m3          | Fish Shop            |
| 19     | Veurne            | 18 m3          | Restaurant           |
| 20     | Brussel           | 15 m3          | Garage               |
| 21     | Zelzate           | 20 m3          | Construction Company |
| 22     | Leuven            | 20 m3          | Bookstore            |
| 23     | Aarschot          | 18 m3          | Laboratory           |
| 24     | Diest             | 20 m3          | Vegetables           |
| 25     | Tienen            | 20 m3          | Construction Company |
| 26     | Lier              | 18 m3          | Restaurant           |
| 27     | Geel              | 20 m3          | Electronics          |
| 28     | Kortrijk          | 20 m3          | Vegetables           |
| 29     | Ieper             | 20 m3          | Restaurant           |
| 30     | Louvain-la-Neuve  | 20 m3          | Garage               |


## Installation

To use this repository, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/cvrp-waste-collection.git`
2. Navigate to the project directory: `cd cvrp-waste-collection`
3. Install the necessary dependencies: `pip install -r requirements.txt`

## Usage

The repository provides a set of tools and resources to solve the CVRP for waste collection repositories with time windows using simulated annealing. Here are the key components:

1. **Data Input**: Modify the input data file to reflect your specific problem instance or client list. Refer to the provided sample example for the required input format.

2. **Simulated Annealing Implementation**: Use the implemented simulated annealing algorithm tailored for the CVRP with time windows. Adjust the algorithm's parameters, such as initial temperature, cooling schedule, and neighbor generation methods, to optimize the results for your problem instance.

3. **Visualization and Evaluation**: Utilize the provided visualization utilities to analyze the results of the simulated annealing algorithm. Plot optimized routes, visualize waste collection patterns, and evaluate the efficiency of the algorithm in terms of solution quality,

 adherence to time windows, and computational time.

4. **Examples and Tutorials**: Explore the example datasets, sample code, and tutorials included in the repository. These resources guide you through solving the CVRP for waste collection repositories with time windows using simulated annealing and help you understand the capabilities of the algorithm.

