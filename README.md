# DuckDB_Extension

# High Level Overview
This is my Independent Study project for the Spring 2026 Semester. I will be extending the capabilities of DuckDB to include sketches under the direction of Dr. Haibo Wang. The Sketches are implemented using the Single Update Sketch with Variable Counter Structure (SSVS) which is the sketch design described in "Single Update Sketch with Variable Counter Structure" by Dimitrios Melissourgos, Haibo Wang, Shigang Chen, Chaoyi Ma, and Shiping Chen. 

DuckDB is downloaded millions of times per month and the goal of this project is to give those users the ability to improve their efficiency in OLAP workloads. Sketches work by giving estimates to queries on datasets (such as the frequency of a certain item) rather than the exact count, saving time and memory usage. This is to be used when a level of error is acceptable in a query (such as "Is this item rare or common?") and the dataset is large. 

Single Update Sketch with Variable Counter Structure (SSVS) was selected as the design for the sketches because it combines the accuracy of multi-update sketches with the speed and memory efficiency of single-update sketches. It accomplishes this by using three conecpts:
* Self-adjusting counters and active counters in a variable counter structure.
* Positive and Negative noise cancellation.
* Noise intervals that block out large noise components. 


# Capabilities Added: 
* Count Min Sketch (CMS): CMS is a probabilistic data structure that estimates the frequency of an item in a data stream quickly and using little memory.


# Dependencies Used
* Ninja Python (for DuckDB) 
* llvm (for DuckDB)
