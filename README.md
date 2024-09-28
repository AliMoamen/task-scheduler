# Task Scheduler - Min Heap Implementation

This project implements a task scheduler using a **min-heap** data structure. The min-heap is used to efficiently manage tasks, where each task has a priority, and the highest-priority task is always scheduled next. The implementation includes methods to add tasks, remove tasks, and manage the priority queue.

## Table of Contents

- [Task Scheduler - Min Heap Implementation](#task-scheduler---min-heap-implementation)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
    - [Features](#features)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Heap Operations](#heap-operations)
    - [Heappush](#heappush)
    - [Heappop](#heappop)
    - [Heapify](#heapify)
    - [Get Min](#get-min)
  - [Testing](#testing)

## Project Overview

This project demonstrates the functionality of a **min-heap** data structure to implement an efficient task scheduling system. The core operations of the min-heap include:

- **Inserting a new task**: A task with a priority is added to the heap, and the heap property is maintained.
- **Removing the minimum priority task**: The task with the highest priority (i.e., the minimum value) is removed.
- **Heapifying a list**: A random list of tasks is converted into a min-heap.
- **Retrieving the minimum**: The task with the minimum priority is retrieved without removing it.

### Features

- **Efficient Scheduling**: By using a min-heap, task insertion, removal, and retrieval are optimized to run in logarithmic time.
- **Heap Methods**: Support for pushing, popping, and heapifying a list of tasks.
- **Visualizations**: Includes visualizations of heap performance under various scenarios.

## Installation

To run this project locally, you will need to have Python and Jupyter Notebook installed. Follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/task-scheduler.git
    ```

2. Install the required packages using `pip`:
    ```bash
    pip install numpy matplotlib
    ```

3. Launch Jupyter Notebook to explore the notebook:
    ```bash
    jupyter notebook
    ```

## Usage

The project can be run through the Jupyter Notebook interface. In the notebook, you'll find examples of creating a min-heap, adding tasks, removing tasks, and visualizing the heap's performance.

To create a min-heap and add tasks, use the following commands in the notebook:

```python
heap = min_heap()
heap.heappush(10)
heap.heappush(5)
heap.heappush(3)
heap.heappush(8)
```

To remove the minimum priority task:

```python
min_task = heap.heappop()
print(min_task)
```

## Heap Operations

### Heappush
The `heappush` method is used to add a new task (element) to the heap while maintaining the heap property.

Example:
```python
heap.heappush(5)
```

### Heappop
The `heappop` method removes and returns the task with the minimum priority.

Example:
```python
min_task = heap.heappop()
```

### Heapify
The `heapify` method is used to convert an arbitrary list of tasks into a valid min-heap.

Example:
```python
lst = [9, 4, 6, 2, 8, 5]
heap.heapify(lst)
```

### Get Min
The `get_min` method retrieves, but does not remove, the task with the minimum priority.

Example:
```python
min_task = heap.get_min()
```

## Testing

The project includes a test suite to verify the correctness of the heap operations. You can run the tests in the notebook by executing the following cells.

Some of the tests include:
- Insertion of elements into the heap and ensuring that the minimum is correct.
- Heapifying a list and checking that it maintains the heap property.
- Popping elements from the heap and confirming the correct order of removal.

Example test cases:

```python
# Test heappush and heappop
heap = min_heap()
heap.heappush(5)
heap.heappush(3)
heap.heappush(7)
assert heap.heappop() == 3
assert heap.heappop() == 5
```

You can explore the entire notebook to see detailed test cases.

---