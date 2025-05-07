# 📊 Hist-Tree Demonstration

This project provides an **interactive, visual demonstration** of the **Hist-Tree** data structure — a hierarchical, histogram-based index designed for efficient range queries over **sorted data**.

The demo runs entirely in the browser and is implemented using **vanilla HTML, CSS, and JavaScript** in a single HTML file.

---

## 🚀 Features

- **Generate Data**  
  Create a dataset of random integers following a normal distribution.- **Tree Construction**  
  Build a Hist-Tree using customizable parameters like bin count and terminal threshold.

- **Visualize Structure**  
  Get a graphical representation of the tree hierarchy and bin contents.

- **Interactive Lookup**  
  Perform key lookups and watch the traversal steps with visual feedback and final binary search within terminal bins.

- **Error Handling**  
  Gracefully handles edge cases such as duplicate values, invalid configurations, and unusual data ranges.

---

## 📁 File

- `hist-tree-demo.html`: The complete interactive demonstration.

---

## 📦 Usage

1. Open `hist-tree-demo.html` in any modern web browser (e.g., Chrome, Firefox, Edge).
2. Adjust parameters:
   - **Number of data points**
   - **Data range (min and max)**
   - **Number of bins per node**
   - **Termin bin threshold**
3. Click **Generate Random Data**.
4. Click **Build Hist-Tree** to construct and display the tree.
5. Enter a key and click **Lookup** to trace how the key is located (or approximated) in the structure.

---

## ⚙️ Parameters Explained

- **Bins per node**  
  The number of histogram bins in each node (typically between 2 and 8). Higher values result in broader trees with fewer levels.

- **Terminal bin threshold**  
  The maximum number of data points a bin can hold before it stops splitting further and becomes a terminal (leaf) bin.

---

## 🧠 How It Works

1. The data is **sorted**.
2. It is **recursively divided into equal-width bins**, forming a tree.
3. If a bin has more than the threshold number of data points and the range allows, it becomes a **non-terminal node** with children.
4. A **lookup** starts at the root and navigates down the tree by selecting the correct bin at each level.
5. The search ends in a **terminal bin**, where a **binary search** is used to find the position or nearest match.

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).
