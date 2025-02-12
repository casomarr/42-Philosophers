<a href="https://www.linux.org/"><img src="https://img.shields.io/badge/Linux-CCAC00?style=for-the-badge&logo=Linux&logoColor=white" height="25em" alt="Linux"/></a>
<a href="https://www.cprogramming.com"><img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" height="25em" alt="C"/></a>

# Philosophers

## Goal
Simulate the classic "Dining Philosophers" problem using threads and mutexes to explore concurrency, synchronization, and resource sharing in a multi-threaded environment.

## Key Features
- **Philosophers:** Represented as threads, each thinking and eating in a cyclic manner.
- **Forks:** Shared resources (mutexes) that philosophers need to pick up to eat.
- **Deadlock Prevention:** Ensures that no philosopher starves by implementing strategies to prevent circular waiting.

## Implementation Details
- Threads: Each philosopher is a separate thread that alternates between thinking, eating, and sleeping.
- Mutexes: Forks are represented as mutexes to ensure exclusive access when picked up.
- Timing: Philosophers sleep and eat for specified durations, with timestamps to track their states.
- Deadlock Avoidance: Implemented a strategy such as picking up forks in a specific order (e.g., always left fork first).

## Challenges
- Deadlock: Avoiding circular waiting where all philosophers hold one fork and wait for another.
- Starvation: Ensuring all philosophers get a chance to eat without indefinitely postponing others.
- Race Conditions: Managing shared resource access to prevent inconsistent states.

## Skills Developed
- Thread Management: Creating and managing multiple threads for concurrent execution.
- Synchronization: Using mutexes to control access to shared resources.
- Debugging: Identifying and resolving deadlocks and race conditions.

## Installation

1. **Clone the repository to your local machine:**
	```sh
	git clone git@github.com:casomarr/42-Philosophers.git
	```

2. **Navigate to the project directory:**
	```sh
	cd 42-Philosophers
	```

3. **Compile the project:**
	```sh
   make
	```

4. **Run the program with the required arguments:**
	```sh
 ./philo <number_of_philosophers> <time_to_die> <time_to_eat> <time_to_sleep> [number_of_meals]
 	```
Example:
```sh
./philo 5 800 200 200 7
```
