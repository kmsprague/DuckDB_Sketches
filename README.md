# DuckDB_Extension

# High Level Overview
This is my Independent Study project for the Spring 2026 Semester in the University of Kentucky's Masters of Computer Science Program. I will be extending the capabilities of DuckDB to include sketches under the direction of Dr. Haibo Wang. The Sketches are implemented using Single Update Sketch with Variable Counter Structure (SSVS) which is the sketch design described in "Single Update Sketch with Variable Counter Structure" by Dimitrios Melissourgos, Haibo Wang, Shigang Chen, Chaoyi Ma, and Shiping Chen. 

# Capabilities Added: 
* Count Min Sketch (CMS): CMS is a probabilistic data structure that estimates the frequency of an item in a data stream quickly and using little memory. Rather than return an exact count of an item, which can be slow or memory intensive on large amounts of data, an estimate is returned which requires less time and memory. This feature works best when only a relative answer is needed for frequency of items. "Is this a rare item or common?"

# Dependencies Used
* Ninja Python (for DuckDB) 
* llvm (for DuckDB)
