# DuckDB_Extension

# High Level Overview
This is my Independent Study project for the Spring 2026 Semester. I will be extending the capabilities of DuckDB to include sketches under the direction of Dr. Haibo Wang. The Sketches are implemented using the Single Update Sketch with Variable Counter Structure (SSVS) which is the sketch design described in "Single Update Sketch with Variable Counter Structure" by Dimitrios Melissourgos, Haibo Wang, Shigang Chen, Chaoyi Ma, and Shiping Chen [Link](http://haibo.pro/paper/ssvs23.pdf)

DuckDB is downloaded over 20 million times per month<sup>1</sup> and the goal of this project is to give those users the ability to improve their efficiency in OLAP workloads. Sketches work by giving estimates to queries on datasets (such as the frequency of a certain item) rather than the exact count, saving time and memory usage. This is to be used when a level of error is acceptable in a query (such as "Is this item rare or common?") and the dataset is large. 

Single Update Sketch with Variable Counter Structure (SSVS) was selected as the design for the sketches because it combines the accuracy of multi-update sketches with the speed and memory efficiency of single-update sketches. It accomplishes this by using three conecpts:
* Self-adjusting counters and active counters in a variable counter structure.
* Positive and Negative noise cancellation.
* Noise intervals that block out large noise components.

These concepts add to make a sketch framework that is comparable to accuracy from CU-SC (the most accurate sketch) at 1/10th the overhead which is comparable to RCS (the most efficient sketch). <sup>2</sup>


# Capabilities Added: 
* Count Min Sketch (CMS): CMS is a probabilistic data structure that estimates the frequency of an item in a data stream quickly and using little memory.


# Dependencies Used
* Ninja Python (for DuckDB) 
* llvm (for DuckDB)


# References
<sup>1</sup> DuckDB 🦆 - Python 🐍 downloads. (n.d.). https://duckdbstats.com/

<sup>2</sup> Melissourgos, D., Wang, H., Chen, S., Ma, C., & Chen, S. (2023). Single Update Sketch with Variable Counter Structure. Proceedings of the VLDB Endowment, 16(13), 4296–4309. https://doi.org/10.14778/3625054.3625065
