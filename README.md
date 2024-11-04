# Smart Agriculture Harvest Optimization Using Autonomous Ground and Air Vehicles

This repository contains the code and research paper for the project "Smart Agriculture with Autonomous Ground and Air Vehicles: An Application on Harvest Optimization." The study applies autonomous aerial and ground vehicles to optimize apple harvest times in an agricultural setting, focusing on time minimization through clustering and optimization techniques.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [Citation](#citation)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Introduction

The agricultural industry is increasingly adopting high-tech solutions to meet the growing demand for efficiency and sustainability. This project explores a novel approach by using autonomous ground and aerial vehicles to optimize the apple harvest process in a time-effective manner. The main goal is to use clustering techniques to determine the optimal stops for ground vehicles and to optimize aerial vehicle routes to minimize harvest times.

This study was published in the *Ankara Hacı Bayram Veli University Journal of Economics and Administrative Sciences* and is supported by the project funded by TÜBİTAK (Project No. 217E138).

## Project Structure

The repository contains the following files:

```bash
Smart_Agriculture_Harvest_Optimization/
├── docs/
│   └── EYI-2020.pdf                # Published research paper
├── src/
│   └── Disaster Mission Planning.jl # Julia code for harvest optimization
├── README.md                       # This README file
└── LICENSE                         # License information


##Installation

To set up and run the project code, you need to install Julia and several packages. Follow the steps below:

Install Julia:
Download and install Julia from the official website: https://julialang.org/downloads/.
Install required Julia packages:
Open the Julia REPL (Read-Eval-Print Loop).
Install the following packages by running these commands:

using Pkg
Pkg.add("JuMP")
Pkg.add("Clustering")
Pkg.add("Distances")
Pkg.add("Gurobi") # Requires Gurobi license; see instructions below.

Note: Gurobi requires a separate license to run. To install the Gurobi Optimizer:
Download Gurobi from https://www.gurobi.com/.
Obtain a free academic license or purchase a commercial license.
Follow the installation instructions provided by Gurobi to activate the license.

##Usage

Clone the Repository:
Open a terminal and run:
git clone https://github.com/yourusername/Smart_Agriculture_Harvest_Optimization.git
cd Smart_Agriculture_Harvest_Optimization/src

Run the Julia Code:
Open Julia in the src directory.
Run the Smart_Agriculture_Harvest_Optimization.jl script:
include("Disaster Mission Planning.jl")
The script will output the optimized stop locations and harvest times for the autonomous vehicles based on the parameters set in the model.

##Methodology

The optimization model in this study divides the complex harvest optimization problem into two sub-problems:

Stop Location Optimization: Using the K-means clustering algorithm to determine the optimal number and locations of stops for the ground vehicle.
Harvest Time Optimization: Minimizing the time taken by aerial vehicles to collect apples at each stop. The model leverages integer programming, solved using the Gurobi optimizer, to minimize the waiting time at each stop.
Parameters and Variables

Parameters:
Coordinates of apples and stops.
Maximum range and flight duration for drones.
Decision Variables:
Optimal stop locations for ground vehicles.
Harvest times and drone wait times.
Results

The model was tested with a scenario involving 500 apples, which yielded the following optimal values:

Number of Stops: 3
Average Waiting Time per Stop: Approximately 439 seconds
These findings demonstrate the feasibility of using autonomous vehicles for large-scale, optimized harvest operations in agricultural fields.

##Citation

If you use this research or code in your work, please cite it as follows:
Güzey, A., Akinci, M.M., & Altan, Ş. (2020). Smart Agriculture with Autonomous Ground and Air Vehicles: An Application on Harvest Optimization. *Ankara Hacı Bayram Veli University Journal of Economics and Administrative Sciences*, Special Issue, 207-220.

##License

This project is licensed under the MIT License - see the LICENSE file for details.

##Acknowledgments

Special thanks to TÜBİTAK for funding this research under Project No. 217E138 and to all contributors involved in the study. This work was presented at the 20th International Econometrics, Operations Research, and Statistics Symposium and is a testament to the collaborative effort towards innovative agricultural solutions.
