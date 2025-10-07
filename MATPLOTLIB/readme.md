# Matplotlib: From Basics to Advanced Data Visualization

This repository contains **comprehensive Matplotlib tutorials and examples** covering both fundamental and advanced plotting techniques for data visualization. Progress from basic plots to complex 3D visualizations, subplots, and pandas integration using real cricket and other datasets.

## 📹 Learning Resources

**YouTube Tutorials:**
- [Matplotlib Basics Live Tutorial](https://www.youtube.com/live/XaKn_cKFlSY?si=jUoRmebX1QmMFKd_) - Fundamentals
- [Advanced Matplotlib Live Tutorial](https://www.youtube.com/live/7YDc5xU9CQQ?si=xMqxN3cRsvkdD_xs) - Advanced concepts

**Matplotlib Documentation:** [Official Matplotlib Docs](https://matplotlib.org/)
- [User Guide](https://matplotlib.org/stable/users/index.html)
- [API Reference](https://matplotlib.org/stable/api/index.html)
- [Gallery](https://matplotlib.org/stable/gallery/index.html) - Examples and code snippets
- [Tutorials](https://matplotlib.org/stable/tutorials/index.html)

---

## 📊 Topics Covered

### **Part 1: Basic Plotting**

#### **1. Line Plots**
- Basic plotting with `plt.plot()`
- Plotting from Pandas DataFrames
- Multiple lines on same plot
- Adding labels, titles, and legends
- Customizing colors, line styles, and markers
- Setting axis limits with `plt.xlim()` and `plt.ylim()`
- Adding grids for better readability

#### **2. Scatter Plots**
- Creating scatter plots with `plt.scatter()`
- Customizing markers and colors
- Variable sizing based on data
- Alternative technique using `plt.plot()` with 'o' marker

#### **3. Bar Charts**
- Vertical bar charts with `plt.bar()`
- Horizontal bar charts with `plt.barh()`
- Grouped bar charts (side-by-side)
- Stacked bar charts
- Rotating x-axis labels for better readability

#### **4. Histograms**
- Basic histograms with custom bins
- Logarithmic scale histograms
- Analyzing data distributions

#### **5. Pie Charts**
- Basic pie charts with labels and percentages
- Exploding slices for emphasis
- Adding shadows and styling

#### **6. Basic Styling and Customization**
- Using different plot styles (`plt.style.use()`)
- Available style options (dark_background, ggplot, seaborn, etc.)
- Saving plots to files with `plt.savefig()`

### **Part 2: Advanced Matplotlib**

#### **7. Advanced Scatter Plots**
- Color mapping with `cmap` and species classification
- Alpha transparency for overlapping points
- Figure sizing with `plt.figure(figsize=())`
- Color bars for continuous data

#### **8. Annotations and Reference Lines**
- Text annotations with `plt.text()`
- Horizontal and vertical reference lines (`axhline`, `axvline`)
- Custom font styling and positioning

#### **9. Subplots and Multiple Plots**
- Object-oriented approach with `fig, ax = plt.subplots()`
- Multiple subplots with `nrows` and `ncols`
- Shared axes between subplots
- Grid layouts (2x2, custom arrangements)
- Alternative subplot creation with `add_subplot()`

#### **10. 3D Visualizations**
- 3D scatter plots with `projection='3d'`
- 3D line plots with `plot3D()`
- 3D surface plots with `plot_surface()`
- Mesh grids with `np.meshgrid()`
- Mathematical functions in 3D space
- Color mapping and color bars for 3D plots

#### **11. Contour Plots and Heatmaps**
- 2D contour plots with `contourf()`
- Heatmaps using `plt.imshow()`
- IPL ball-by-ball data heatmap analysis
- Custom tick labels and color mapping

#### **12. Pandas Integration**
- Direct plotting from pandas Series and DataFrames
- `DataFrame.plot()` method with different kinds
- Scatter plots with categorical color mapping
- Line plots from time series data
- Bar charts from grouped data
- Stacked and grouped bar charts
- Histograms from DataFrame columns
- Pie charts with subplots
- Multi-index DataFrame visualizations

---

## 📁 Datasets Used

All datasets are stored in the `dataset/` folder:

### **Cricket Datasets:**
- **`sharma-kohli.csv`** - Career comparison data between Rohit Sharma and Virat Kohli
- **`batter.csv`** - Comprehensive batting statistics for cricket analysis
- **`batsman_season_record.csv`** - Season-wise performance records
- **`vk.csv`** - Virat Kohli's detailed batting data
- **`gayle-175.csv`** - Chris Gayle's historic 175-run match data
- **`IPL_Ball_by_Ball_2008_2022.csv`** - Detailed ball-by-ball IPL data for heatmap analysis

### **Other Datasets:**
- **`iris.csv`** - Classic iris flower dataset for classification visualization
- **`big-array.npy`** - Large numerical array for histogram demonstrations
- **External:** Seaborn's tips dataset and online stock data for pandas integration

---

## 🚀 Key Features Demonstrated

### **Basic Features:**
- **Data Loading:** Reading CSV files with Pandas and NumPy arrays
- **Plot Customization:** Colors, markers, line styles, and sizes
- **Multiple Plots:** Comparing datasets on single visualization
- **Statistical Visualization:** Distributions, comparisons, and trends
- **Export Functionality:** Saving plots as image files
- **Interactive Elements:** Legends, grids, and basic annotations

### **Advanced Features:**
- **3D Visualizations:** Surface plots, 3D scatter plots, and mathematical modeling
- **Complex Layouts:** Multi-subplot arrangements and shared axes
- **Advanced Annotations:** Text positioning, reference lines, and styling
- **Color Mapping:** Continuous and categorical color schemes
- **Pandas Integration:** Direct plotting from DataFrames with multiple plot types
- **Heatmaps and Contours:** 2D data representation and pattern analysis
- **Object-Oriented Plotting:** Professional subplot management and customization

---

## 💻 Getting Started

### Prerequisites
```bash
pip install matplotlib pandas numpy seaborn
```

### Running the Notebook
1. Open `matplotlib_basics_to_adavance.ipynb` in Jupyter Notebook or VS Code
2. Run cells sequentially to progress from basic to advanced concepts
3. Experiment with different datasets and customizations
4. Follow along with both YouTube tutorials for comprehensive understanding

---

## 🎯 Learning Objectives

After completing this comprehensive tutorial, you'll be able to:

### **Basic Level:**
- Create fundamental plot types (line, scatter, bar, histogram, pie)
- Apply plot customization and styling
- Handle real-world datasets for visualization
- Export plots for reports and presentations

### **Advanced Level:**
- Create complex 3D visualizations and surface plots
- Design multi-subplot layouts with shared axes
- Implement advanced annotations and reference lines
- Use pandas for direct DataFrame plotting
- Create heatmaps and contour plots for pattern analysis
- Apply color mapping for categorical and continuous data
- Use object-oriented plotting for professional visualizations

---

## 🔗 Related Topics

- **NumPy:** For numerical array operations and mathematical functions
- **Pandas:** For data manipulation, analysis, and direct plotting
- **Seaborn:** For statistical visualizations (built on Matplotlib)
- **3D Mathematics:** Surface equations, mesh grids, and mathematical modeling
- **Data Science:** Exploratory data analysis and pattern recognition

---

## 📈 Sample Visualizations

The notebook includes practical examples such as:

### **Basic Visualizations:**
- Cricket player performance comparisons
- Batting average vs strike rate analysis
- Season-wise performance tracking
- Data distribution analysis
- Custom styling and themes

### **Advanced Visualizations:**
- 3D surface plots of mathematical functions
- Multi-subplot cricket data analysis
- IPL ball-by-ball heatmaps
- Iris species classification with color mapping
- Stock market time series analysis
- Interactive annotations and reference lines

## 🎥 Video Learning Path

1. **Start with [Basics Tutorial](https://www.youtube.com/live/XaKn_cKFlSY?si=jUoRmebX1QmMFKd_)** - Foundation concepts
2. **Progress to [Advanced Tutorial](https://www.youtube.com/live/7YDc5xU9CQQ?si=xMqxN3cRsvkdD_xs)** - Complex visualizations
3. **Reference [Official Documentation](https://matplotlib.org/)** - Detailed function guides


This comprehensive approach ensures you master both fundamental and advanced matplotlib techniques!
