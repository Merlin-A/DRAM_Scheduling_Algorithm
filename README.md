# DRAM Scheudling Algorithms

---



This project enhances the [Ramulator](https://github.com/CMU-SAFARI/ramulator) DRAM simulator with the implementation and evaluation of several memory scheduling algorithms.  
The goal is to improve memory access performance and fairness across multiple cores and memory controllers.

## 📋 Implemented Schedulers
- **FCFS** (First Come First Serve)
- **FRFCFS** (First Ready First Come First Serve)
- **FRFCFS_PriorHit** (Prioritize Row-Hits)
- **FRFCFS_Cap** (Limit consecutive Row-Hits)
- **BLISS** (Blacklisting Memory Scheduler)
- **ATLAS** (Adaptive per-Thread Least Attained Service)

## 🛠️ Setup and Run
```bash
make -j$(nproc)    # Build the simulator
./ramulator configs/DDR3-config.cfg --mode=dram --stats my_output.txt dram.trace
```
> Replace `DDR3-config.cfg` with `DDR4-config.cfg` for DDR4 tests.

## 📈 Results
Key performance metrics collected:
- Row buffer hits/misses/conflicts
- DRAM active/busy cycles
- Number of requests served
- Average read latency

## 📄 Report
Detailed results and analysis available in the project report.

## 📚 References
- [Ramulator by CMU SAFARI Group](https://github.com/CMU-SAFARI/ramulator)
- Scheduling techniques: FRFCFS, BLISS, ATLAS papers

---
