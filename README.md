**Hist-Tree Demonstration**

This project provides an interactive, visual demonstration of the Hist-Tree data structure, a hierarchical histogram-based index for range queries over sorted data. The demo is entirely browser-based and implemented in a single HTML file using vanilla JavaScript, HTML, and CSS.

🚀 **Features**
-**Generate Data:** Create a dataset of random integers following a normal distribution.
-**Tree Construction:** Build a Hist-Tree with user-defined bin count and terminal threshold.
-**Visualize Structure:** Graphical representation of the tree hierarchy and bin contents.
-**Interactive Lookup:** Perform key lookups, with visual step-by-step traversal and binary search inside terminal bins.
-**Error Handling:** Handles edge cases like duplicate values or improper configurations.

📁 **File**
**hist-tree-demo.html:** The complete interactive demonstration.

📦 **Usage**
Open hist-tree-demo.html in a modern web browser (Chrome, Firefox, Edge, etc.).

**Adjust parameters:**

Number of data points

Data range (min and max)

Number of bins per node

Terminal bin threshold

Click Generate Random Data.

Click Build Hist-Tree to construct the tree.

Enter a key and click Lookup to trace how the key is located (or approximated) in the structure.

⚙️ **Parameters Explained**
**Bins per node:** Number of histogram bins in each node (between 2 and 8).

**Terminal bin threshold:** Maximum number of data points allowed in a bin before it becomes a leaf.

🧠 **How It Works**
The data is sorted and divided recursively into histogram bins.

If a bin contains more than the threshold and further partitioning is beneficial, it becomes a non-terminal node with child bins.

Lookup proceeds by following the correct bin at each level and finally performing binary search in a terminal bin.
