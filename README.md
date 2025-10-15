# Operating Systems Lab - Codetantra

A comprehensive collection of Operating System concepts and algorithm implementations, covering CPU scheduling, memory management, process synchronization, and various OS algorithms commonly taught in OS lab courses.

## 📋 Table of Contents

- [Overview](#overview)
- [Topics Covered](#topics-covered)
- [CPU Scheduling Algorithms](#cpu-scheduling-algorithms)
- [Memory Management](#memory-management)
- [Process Synchronization](#process-synchronization)
- [Disk Scheduling](#disk-scheduling)
- [File Allocation Methods](#file-allocation-methods)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This repository contains implementations of fundamental Operating System algorithms and concepts. Each program is designed to help understand core OS principles through practical implementation. The implementations are suitable for academic purposes and OS lab coursework.

## 📚 Topics Covered

### CPU Scheduling Algorithms

CPU scheduling is the basis of multiprogrammed operating systems. By switching the CPU among processes, the operating system can make the computer more productive.

- **First Come First Serve (FCFS)**: Simplest scheduling algorithm that schedules according to arrival times of processes
- **Shortest Job First (SJF)**: Schedules processes based on shortest execution time (both preemptive and non-preemptive)
- **Priority Scheduling**: Each process is assigned a priority, and CPU is allocated to the process with highest priority
- **Round Robin (RR)**: Each process gets a small unit of CPU time (time quantum), after which it is preempted
- **Multilevel Queue Scheduling**: Processes are divided into different queues based on priority
- **Multilevel Feedback Queue**: Similar to multilevel queue but allows processes to move between queues

**Key Metrics Calculated:**
- Average Waiting Time
- Average Turnaround Time
- Average Response Time
- CPU Utilization
- Throughput

### Memory Management

Memory management is the functionality of an OS which handles or manages primary memory and moves processes back and forth between main memory and disk during execution.

#### Contiguous Memory Allocation

Allocation techniques for contiguous memory:

- **First Fit**: Allocate the first hole that is big enough
- **Best Fit**: Allocate the smallest hole that is big enough
- **Worst Fit**: Allocate the largest available hole
- **Next Fit**: Similar to first fit, but starts searching from where it left off

#### Paging

- **Page Replacement Algorithms**:
  - FIFO (First In First Out)
  - LRU (Least Recently Used)
  - Optimal Page Replacement
  - LFU (Least Frequently Used)
- **Page Fault Calculation**
- **Effective Access Time**

#### Segmentation

- Segmentation with paging
- Segment table implementation

#### Banker's Algorithm

Banker's Algorithm is a deadlock avoidance algorithm that tests for safety by simulating the allocation of predetermined maximum possible amounts of all resources.

**Features:**
- **Safety Algorithm**: Determines if the system is in a safe state
- **Resource Request Algorithm**: Checks if a resource request can be granted safely
- **Deadlock Detection**: Identifies if the system is in a deadlock state
- **Available, Allocation, Need matrices**: Core data structures used

**Concepts Covered:**
- Safe State vs Unsafe State
- Resource Allocation Graph
- Deadlock Prevention
- Deadlock Avoidance

### Process Synchronization

Solutions to critical section problem and synchronization:

- **Producer-Consumer Problem** (Bounded Buffer Problem)
- **Readers-Writers Problem**
- **Dining Philosophers Problem**
- **Sleeping Barber Problem**
- **Semaphores Implementation**
- **Mutex and Locks**
- **Monitor Implementation**

### Disk Scheduling

Algorithms to determine the order in which disk I/O requests are serviced:

- **FCFS (First Come First Serve)**: Services requests in the order they arrive
- **SSTF (Shortest Seek Time First)**: Services the request with minimum seek time from current position
- **SCAN (Elevator Algorithm)**: Head moves in one direction servicing requests until it reaches the end
- **C-SCAN (Circular SCAN)**: Similar to SCAN but only services in one direction
- **LOOK**: Similar to SCAN but reverses direction when no more requests ahead
- **C-LOOK**: Circular version of LOOK

**Metrics:**
- Total Head Movement
- Average Seek Time

### File Allocation Methods

Methods for allocating disk space to files:

- **Contiguous Allocation**: Each file occupies a set of contiguous blocks
- **Linked Allocation**: Each file is a linked list of disk blocks
- **Indexed Allocation**: Brings all pointers together into an index block

## 🚀 Getting Started

### Prerequisites

Depending on the implementation language used:

```bash
# For C programs
gcc --version

# For C++ programs
g++ --version

# For Python programs
python3 --version

# For Java programs
java --version
javac --version
```

### Compilation

```bash
# For C programs
gcc program_name.c -o program_name

# For C++ programs
g++ program_name.cpp -o program_name

# For Java programs
javac ProgramName.java
```

### Running Programs

```bash
# C/C++ compiled programs
./program_name

# Java programs
java ProgramName

# Python programs
python3 program_name.py
```

## 💻 How to Use

1. **Clone the repository**:
   ```bash
   git clone https://github.com/SleepyStack/OS_Lab1_Codetantra.git
   cd OS_Lab1_Codetantra
   ```

2. **Navigate to the specific algorithm/program** you want to run

3. **Compile** (if necessary) and **run** the program

4. **Provide input** as prompted by the program

5. **Analyze the output** which typically includes:
   - Step-by-step execution
   - Final results
   - Performance metrics
   - Gantt charts (for scheduling algorithms)

## 📁 Repository Structure

```
OS_Lab1_Codetantra/
├── CPU_Scheduling/
│   ├── FCFS/
│   ├── SJF/
│   ├── Priority/
│   ├── RoundRobin/
│   └── MultilevelQueue/
├── Memory_Management/
│   ├── Contiguous_Allocation/
│   ├── Paging/
│   ├── Segmentation/
│   └── Bankers_Algorithm/
├── Process_Synchronization/
│   ├── Producer_Consumer/
│   ├── Readers_Writers/
│   └── Dining_Philosophers/
├── Disk_Scheduling/
│   ├── FCFS/
│   ├── SSTF/
│   ├── SCAN/
│   └── LOOK/
└── File_Allocation/
    ├── Contiguous/
    ├── Linked/
    └── Indexed/
```

## 🤝 Contributing

Contributions are welcome! If you'd like to add new algorithms, improve existing implementations, or fix bugs:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines

- Ensure your code is well-commented
- Include sample input/output in comments
- Follow consistent coding style
- Test your implementation thoroughly
- Update documentation if needed

## 📖 Additional Resources

### Recommended Reading

- **Operating System Concepts** by Abraham Silberschatz, Peter B. Galvin, Greg Gagne
- **Modern Operating Systems** by Andrew S. Tanenbaum
- **Operating Systems: Three Easy Pieces** by Remzi H. Arpaci-Dusseau and Andrea C. Arpaci-Dusseau

### Online Resources

- [OS Dev Wiki](https://wiki.osdev.org/)
- [GeeksforGeeks OS Section](https://www.geeksforgeeks.org/operating-systems/)
- [Tutorialspoint OS Tutorial](https://www.tutorialspoint.com/operating_system/index.htm)

## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Chirag** - [SleepyStack](https://github.com/SleepyStack)

## 🙏 Acknowledgments

- Thanks to all contributors who help improve this repository
- Inspired by various OS textbooks and course materials
- Created for educational purposes and OS lab coursework

---

**Note**: This repository is intended for educational purposes. The implementations focus on demonstrating core concepts and may be simplified compared to real-world OS implementations.

## 📬 Contact

For questions, suggestions, or issues, please open an issue in the GitHub repository.

**Happy Learning! 🎓**
