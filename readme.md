# CPU Scheduler Simulator

A Windows Forms application that demonstrates CPU scheduling algorithms through
an interactive graphical interface. Built for CS 3502: Operating Systems at
Kennesaw State University.

**Fork maintained by Chris Regan** — Original creator: Francis (used with permission)  
**Extended by: Alexia Martinez** — Added SRTF and HRRN algorithms for Project 2

---

## Algorithms Implemented

| Algorithm | Type | Notes |
|-----------|------|-------|
| First Come First Serve (FCFS) | Non-preemptive | Executes in arrival order |
| Shortest Job First (SJF) | Non-preemptive | Selects shortest burst time first |
| Priority Scheduling | Non-preemptive | Higher number = higher priority |
| Round Robin (RR) | Preemptive | Requires a time quantum parameter |
| **Shortest Remaining Time First (SRTF)** | **Preemptive** | **Preemptive version of SJF** |
| **Highest Response Ratio Next (HRRN)** | **Non-preemptive** | **Selects by (Wait+Burst)/Burst** |

---

## Requirements

- **OS:** Windows 10 or Windows 11
- **Runtime:** .NET 8.0 SDK or newer
- **IDE:** Visual Studio 2022 or VS Code with C# Dev Kit extension

---

## How to Run

### Using VS Code Terminal (Recommended)

1. Clone the repository:
   ```bash
   git clone https://github.com/alexia-nmm/CS-3502-CPU-Scheduler.git
   ```

2. Navigate to the project folder:
   ```bash
   cd CS-3502-CPU-Scheduler
   ```

3. Run the application:
   ```bash
   dotnet run --project CpuScheduler/CpuScheduler.csproj
   ```

### Using Visual Studio 2022

1. Open `CpuScheduler.sln` in Visual Studio 2022
2. Press **F5** to build and run

---

## How to Use

1. The app opens with 5 default processes loaded
2. Edit process data directly in the grid (Process ID, Burst Time, Priority, Arrival Time)
3. Click **Set Process Count** to change the number of processes
4. Use **Generate Random** to populate with random values
5. Click any algorithm button to run the simulation
6. View results in the **Results** tab — includes all performance metrics
7. Use **Save Data / Load Data** to export and import CSV process data

---

## Performance Metrics Displayed

For every algorithm run, the Results tab shows:
- Average Waiting Time (AWT)
- Average Turnaround Time (ATT)
- CPU Utilization (%)
- Throughput (processes/unit)
- Average Response Time

---

## Project Structure

```
CpuScheduler/
├── CpuSchedulerForm.cs           # Main form + all algorithm implementations
├── CpuSchedulerForm.Designer.cs  # UI component definitions
├── Algorithms.cs                 # Legacy algorithm implementations
├── Helper.cs                     # Helper utilities
├── ModifyProgressBarColor.cs     # Custom progress bar color helper
├── Program.cs                    # Application entry point
└── Properties/                   # Assembly and resource files
```

---

## Platform Tested

- **OS:** Windows 11
- **IDE:** Visual Studio Code
- **.NET:** 8.0 SDK

---

## License

This project is licensed under the terms of the [MIT license](LICENSE.txt).
