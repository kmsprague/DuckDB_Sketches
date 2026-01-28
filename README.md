# DuckDB_Extension

# High Level Overview
This is my Independent Study project for the Spring 2026 Semester. I will be extending the capabilities of DuckDB to include sketches under the direction of Dr. Haibo Wang. 

DuckDB is downloaded over 20 million times per month<sup>1</sup> and the goal of this project is to give those users the ability to improve their efficiency in OLAP workloads. Sketches work by giving estimates to queries on datasets (such as the frequency of a certain item) rather than the exact count, saving time and memory usage. This is to be used when a level of error is acceptable in a query (such as "Is this item rare or common?") and the dataset is large. 


# Capabilities Added: 
* **Count Min Sketch (CMS):** CMS is a probabilistic data structure that estimates the frequency of an item in a data stream quickly and using little memory. The files added to implement CMS are duckdb/src/common/count_min_sketch.hpp and duckdb/src/common/count_min_sketch.cpp. 


# Dependencies Used
* Ninja Python (for DuckDB) 
* llvm (for DuckDB)


# References
<sup>1</sup> DuckDB 🦆 - Python 🐍 downloads. (n.d.). https://duckdbstats.com/
