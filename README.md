# DuckDB_Extension

# High Level Overview
This is my Independent Study project for the Spring 2026 Semester. I will be extending the capabilities of DuckDB to include sketches under the direction of Dr. Haibo Wang. 

DuckDB is downloaded over 20 million times per month<sup>1</sup> and the goal of this project is to give those users the ability to improve their efficiency in OLAP workloads. Sketches work by giving estimates to queries on datasets (such as the frequency of a certain item) rather than the exact count, saving time and memory usage. This is to be used when a level of error is acceptable in a query (such as "Is this item rare or common?") and the dataset is large. 


# Capabilities Added: 
* **Approximate_Min:** Approximate min is Count Min Sketch. It has two parts, approximate_min_build builds the sketch and the sketch is queried using approximate_min. Once a sketch is built for a column, it does not need to be built again, it can be queried many times. 


# Dependencies Used
* Ninja Python (for DuckDB) 
* llvm (for DuckDB)


# References
<sup>1</sup> DuckDB 🦆 - Python 🐍 downloads. (n.d.). https://duckdbstats.com/
