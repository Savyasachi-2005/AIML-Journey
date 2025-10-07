# Matplotlib Basics for Data Visualization

This repository contains **basic Matplotlib tutorials and examples** focusing on fundamental plotting techniques for data visualization. This covers the essential building blocks before moving to advanced matplotlib concepts. Learn to create various types of basic plots using real cricket datasets and practice essential visualization skills.

## 📹 Learning Resources

**YouTube Tutorial:** [Matplotlib Basics Live Tutorial](https://www.youtube.com/live/XaKn_cKFlSY?si=jUoRmebX1QmMFKd_)

**Matplotlib Documentation:** [Official Matplotlib Docs](https://matplotlib.org/)
- [User Guide](https://matplotlib.org/stable/users/index.html)
- [API Reference](https://matplotlib.org/stable/api/index.html)
- [Gallery](https://matplotlib.org/stable/gallery/index.html) - Examples and code snippets
- [Tutorials](https://matplotlib.org/stable/tutorials/index.html)

---

## 📊 Topics Covered

### **1. Line Plots**
- Basic plotting with `plt.plot()`
- Plotting from Pandas DataFrames
- Multiple lines on same plot
- Adding labels, titles, and legends
- Customizing colors, line styles, and markers
- Setting axis limits with `plt.xlim()` and `plt.ylim()`
- Adding grids for better readability

### **2. Scatter Plots**
- Creating scatter plots with `plt.scatter()`
- Customizing markers and colors
- Variable sizing based on data
- Alternative technique using `plt.plot()` with 'o' marker

### **3. Bar Charts**
- Vertical bar charts with `plt.bar()`
- Horizontal bar charts with `plt.barh()`
- Grouped bar charts (side-by-side)
- Stacked bar charts
- Rotating x-axis labels for better readability

### **4. Histograms**
- Basic histograms with custom bins
- Logarithmic scale histograms
- Analyzing data distributions

### **5. Pie Charts**
- Basic pie charts with labels and percentages
- Exploding slices for emphasis
- Adding shadows and styling

### **6. Styling and Customization**
- Using different plot styles (`plt.style.use()`)
- Available style options (dark_background, ggplot, seaborn, etc.)
- Saving plots to files with `plt.savefig()`

---

## 📁 Datasets Used

All datasets are stored in the `dataset/` folder:

- **`sharma-kohli.csv`** - Career comparison data between Rohit Sharma and Virat Kohli
- **`batter.csv`** - Batting statistics for cricket analysis
- **`batsman_season_record.csv`** - Season-wise performance records
- **`vk.csv`** - Virat Kohli's detailed batting data
- **`gayle-175.csv`** - Chris Gayle's historic 175-run match data
- **`big-array.npy`** - Large numerical array for histogram demonstrations

---

## 🚀 Key Features Demonstrated (Basics)

- **Data Loading:** Reading CSV files with Pandas and NumPy arrays
- **Basic Plot Customization:** Colors, markers, line styles, and sizes
- **Multiple Plots:** Comparing datasets on single visualization
- **Fundamental Statistical Visualization:** Distributions, comparisons, and trends
- **Export Functionality:** Saving plots as image files
- **Basic Interactive Elements:** Legends, grids, and annotations

---

## 💻 Getting Started

### Prerequisites
```bash
pip install matplotlib pandas numpy seaborn
```

### Running the Notebook
1. Open `matplotlib_basics.ipynb` in Jupyter Notebook or VS Code
2. Run cells sequentially to see different plot types
3. Experiment with different datasets and customizations

---

## 🎯 Learning Objectives (Basic Level)

After completing this basic tutorial, you'll be able to:
- Create fundamental plot types (line, scatter, bar, histogram, pie)
- Apply basic plot customization and styling
- Handle real-world datasets for basic visualization
- Export plots for reports and presentations
- Choose appropriate basic plot types for different data scenarios
- **Foundation for advanced matplotlib concepts**

---

## 🔗 Related Topics

- **NumPy:** For numerical array operations
- **Pandas:** For data manipulation and analysis
- **Seaborn:** For advanced statistical visualizations (built on Matplotlib)
- **Advanced Matplotlib:** Coming next - subplots, animations, 3D plots, and more complex visualizations

---

## 📈 Sample Visualizations

The notebook includes practical examples such as:
- Cricket player performance comparisons
- Batting average vs strike rate analysis
- Season-wise performance tracking
- Data distribution analysis
- Custom styling and themes

**Follow along with the [YouTube tutorial](https://www.youtube.com/live/XaKn_cKFlSY?si=jUoRmebX1QmMFKd_)** for step-by-step guidance and refer to the [official documentation](https://matplotlib.org/) for detailed function references.