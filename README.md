# multihead-disk-scheduling-algorithm
Base Case - OPTIMIZED TWO HEAD DISK SCHEDULING ALGORITHM (OTHDSA)

# Multi-head Disk Scheduling Algorithms

This project demonstrates the implementation and comparison of various disk scheduling algorithms including C-SCAN, SSTF, and Random Scan. The goal of the project is to optimize seek time for disk scheduling by analyzing the efficiency of these algorithms in terms of total head movements.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
  - [Running the Algorithms](#running-the-algorithms)
- [Project Files](#project-files)
- [Explanation of Algorithms](#explanation-of-algorithms)
  - [C-SCAN Algorithm](#c-scan-algorithm)
  - [SSTF Algorithm](#sstf-algorithm)
  - [Random Scan Algorithm](#random-scan-algorithm)
- [Plots](#plots)
- [Research and Logic](#research-and-logic)
- [Requirements](#requirements)
- [References](#references)

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/darsh0o/multihead-disk-scheduling-algorithm.git
    cd disk-scheduling-algorithms
    ```

2. **Install the dependencies**:

    To install all the necessary packages using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```

3. **Ensure you have Python 3.x** installed on your machine.

## Usage

### Running the Algorithms

You can run the algorithms by executing the respective Python files. Each algorithm can be executed separately. Make sure to adjust the input parameters for the I/O requests, which can be modified directly in the respective Python files.

#### C-SCAN Algorithm
```bash
python "C-SCAN Disk Scheduling Algorithm.py"
```

#### SSTF Algorithm
```bash
python "SSTF disk scheduling algorithm.py"
```

#### Random Scan Algorithm
```bash
python "Random SCAN Disk Scheduling Algorithms.py"
```

### Plotting the Results

To compare the performance of these algorithms visually, you can run the `Plots.py` script. It will generate plots showing the total seek time for each algorithm based on the provided I/O requests.

Run the following command to generate the plots:
```bash
python Plots.py
```

This will generate visual representations of the performance of each disk scheduling algorithm. The plots compare the total seek times across C-SCAN, SSTF, and Random Scan algorithms, showing which approach yields the lowest overall head movements based on the given I/O requests.

The generated plots can help in analyzing the efficiency of different algorithms, giving insights into how they perform under various conditions. These plots can be especially useful when testing with different data sets of I/O requests.

## Project Files

- **`C-SCAN Disk Scheduling Algorithm.py`**: Implements the C-SCAN algorithm, where the disk head moves from one end of the disk to the other, servicing requests, and returns to the beginning without processing requests on the way back.
- **`SSTF disk scheduling algorithm.py`**: Implements the Shortest Seek Time First (SSTF) algorithm, which selects the closest I/O request to the current head position.
- **`Random SCAN Disk Scheduling Algorithms.py`**: Implements a randomized I/O request processing algorithm, where requests are served randomly without any specific optimization.
- **`Plots.py`**: Generates comparative visual plots that display the total seek time for each disk scheduling algorithm.

## Explanation of Algorithms

### C-SCAN Algorithm
C-SCAN is a variation of the SCAN disk scheduling algorithm. In C-SCAN, the disk head moves in one direction, servicing I/O requests as it goes. Once it reaches the far end of the disk, the head immediately returns to the start without servicing any requests on the return journey. This circular behavior ensures that all requests are treated uniformly, reducing the wait time variance compared to the SCAN algorithm.

### SSTF Algorithm
Shortest Seek Time First (SSTF) is an algorithm that selects the I/O request closest to the current head position. By servicing the nearest request, the SSTF algorithm reduces the seek time required for each operation. However, this method can lead to starvation, where distant requests are delayed indefinitely if there are always closer requests to process.

### Random Scan Algorithm
In the Random Scan algorithm, the disk head services I/O requests in random order, without considering their proximity to the current head position. This non-deterministic behavior often results in higher seek times and is primarily used for comparison against more structured algorithms like SSTF and C-SCAN.

## Plots

The `Plots.py` file provides a visual comparison of the total seek times for each algorithm. By running this script, you can observe how each algorithm performs with the same set of I/O requests and analyze which one minimizes disk head movements most effectively.

## Research and Logic

The logic behind this project is based on well-known disk scheduling algorithms that are commonly used in operating systems to optimize disk I/O performance. The primary goal of these algorithms is to reduce the seek time, which directly impacts the efficiency of data retrieval from storage devices.

The research that inspired this project includes a study on multi-head disk scheduling systems, such as the **Optimized Two-Head Disk Scheduling Algorithm (OTHDSA)** developed by Singh, K., Rastogi, D., and Singh, D. (2015). Their work focuses on improving the performance of disk systems by reducing the total number of head movements, especially in multi-head disk configurations. The algorithms implemented in this project are a part of standard disk scheduling techniques, but the logic behind them is inspired by these advanced research efforts.

### Research Paper Citation
The concepts and optimization strategies used in this project are based on:
- **Singh, K., Rastogi, D., & Singh, D.** (2015). *Optimized Two Head Disk Scheduling Algorithm (OTHDSA)*. 2015 Fifth International Conference on Advanced Computing & Communication Technologies. IEEE. DOI: 10.1109/ACCT.2015.70.

## Requirements

This project requires the following Python libraries:

- `matplotlib`: Used for generating the plots that compare the performance of different disk scheduling algorithms.
- `numpy`: Required for numerical operations and data handling.
- `random`: Used in the implementation of the Random Scan algorithm to simulate random I/O request servicing.

To install the necessary dependencies, run:
```bash
pip install -r requirements.txt
```

This will generate visual representations of the performance of each disk scheduling algorithm. The plots compare the total seek times across C-SCAN, SSTF, and Random Scan algorithms, showing which approach yields the lowest overall head movements based on the given I/O requests.

The generated plots can help in analyzing the efficiency of different algorithms, giving insights into how they perform under various conditions. These plots can be especially useful when testing with different data sets of I/O requests.

## Project Files

- **`C-SCAN Disk Scheduling Algorithm.py`**: Implements the C-SCAN algorithm, where the disk head moves from one end of the disk to the other, servicing requests, and returns to the beginning without processing requests on the way back.
- **`SSTF disk scheduling algorithm.py`**: Implements the Shortest Seek Time First (SSTF) algorithm, which selects the closest I/O request to the current head position.
- **`Random SCAN Disk Scheduling Algorithms.py`**: Implements a randomized I/O request processing algorithm, where requests are served randomly without any specific optimization.
- **`Plots.py`**: Generates comparative visual plots that display the total seek time for each disk scheduling algorithm.

## Explanation of Algorithms

### C-SCAN Algorithm
C-SCAN is a variation of the SCAN disk scheduling algorithm. In C-SCAN, the disk head moves in one direction, servicing I/O requests as it goes. Once it reaches the far end of the disk, the head immediately returns to the start without servicing any requests on the return journey. This circular behavior ensures that all requests are treated uniformly, reducing the wait time variance compared to the SCAN algorithm.

### SSTF Algorithm
Shortest Seek Time First (SSTF) is an algorithm that selects the I/O request closest to the current head position. By servicing the nearest request, the SSTF algorithm reduces the seek time required for each operation. However, this method can lead to starvation, where distant requests are delayed indefinitely if there are always closer requests to process.

### Random Scan Algorithm
In the Random Scan algorithm, the disk head services I/O requests in random order, without considering their proximity to the current head position. This non-deterministic behavior often results in higher seek times and is primarily used for comparison against more structured algorithms like SSTF and C-SCAN.

## Plots

The `Plots.py` file provides a visual comparison of the total seek times for each algorithm. By running this script, you can observe how each algorithm performs with the same set of I/O requests and analyze which one minimizes disk head movements most effectively.

## Research and Logic

The logic behind this project is based on well-known disk scheduling algorithms that are commonly used in operating systems to optimize disk I/O performance. The primary goal of these algorithms is to reduce the seek time, which directly impacts the efficiency of data retrieval from storage devices.

The research that inspired this project includes a study on multi-head disk scheduling systems, such as the **Optimized Two-Head Disk Scheduling Algorithm (OTHDSA)** developed by Singh, K., Rastogi, D., and Singh, D. (2015). Their work focuses on improving the performance of disk systems by reducing the total number of head movements, especially in multi-head disk configurations. The algorithms implemented in this project are a part of standard disk scheduling techniques, but the logic behind them is inspired by these advanced research efforts.

### Research Paper Citation
The concepts and optimization strategies used in this project are based on:
- **Singh, K., Rastogi, D., & Singh, D.** (2015). *Optimized Two Head Disk Scheduling Algorithm (OTHDSA)*. 2015 Fifth International Conference on Advanced Computing & Communication Technologies. IEEE. DOI: 10.1109/ACCT.2015.70.

## Requirements

This project requires the following Python libraries:

- `matplotlib`: Used for generating the plots that compare the performance of different disk scheduling algorithms.
- `numpy`: Required for numerical operations and data handling.
- `random`: Used in the implementation of the Random Scan algorithm to simulate random I/O request servicing.

To install the necessary dependencies, run:
```bash
pip install -r requirements.txt
```

## References
Singh, K., Rastogi, D., & Singh, D. (2015). Optimized Two Head Disk Scheduling Algorithm (OTHDSA). 2015 Fifth International Conference on Advanced Computing & Communication Technologies. IEEE. DOI: 10.1109/ACCT.2015.70.
Parekh, H. B., Saksena, A., Ringshia, A., & Chaudhari, S. (2017). Simulation of a Two Head Disk Scheduling Algorithm. 2017 Second International Conference on Electrical, Computer and Communication Technologies (ICECCT). IEEE.

## Conclusion
In this project, we have implemented three disk scheduling algorithms—C-SCAN, SSTF, and Random Scan. Each algorithm was tested for its efficiency in minimizing disk head movements, with the results plotted for easy comparison. The C-SCAN and SSTF algorithms are well-established for optimizing disk I/O performance, and this project provides a practical implementation and comparison of these methods.

## Future improvements could include:

Implementing other algorithms such as LOOK and C-LOOK for further comparisons.
Incorporating more complex datasets to simulate real-world scenarios.
Expanding the multi-head disk scheduling approach, as discussed in the research paper by Singh et al. (2015).
Feel free to contribute to this project or raise issues if you have any questions or suggestions!
