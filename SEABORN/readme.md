# SEABORN

## Overview
Seaborn is easy to use and is a better version of matplotlib with more graphs included. It's a famous Python visualization library.

## Types of Functions
- **Figure level**
- **Axis level**

## Main Classification

### 1. Relational Plot
- Scatterplot
- Lineplot

### 2. Distribution Plot
- Histogram
- KDE plot
- Rugplot

### 3. Categorical Plot
- Barplot
- Countplot
- Boxplot
- Violinplot
- Swarmplot

### 4. Regression Plot
- Regplot

### 5. Matrix Plot
- HeatMap
- ClusterMap

### 6. Multiplot
- Jointplot
- Pairplot

---

## Content Covered

### Relational Plots

#### Scatter Plot
- Used mainly for numerical values
- Axis level: `sns.scatterplot()`
- Figure level: `sns.relplot()` with `kind='scatter'`
- Parameters: `data`, `x`, `y`, `hue`, `style`, `size`

#### Line Plot
- Axis level: `sns.lineplot()`
- Figure level: `sns.relplot()` with `kind='line'`
- Used for showing trends over time or continuous variables
- Parameters: `hue`, `style`, `size`

#### Facet Plot
- Plotting multiple graphs on categorical data
- Only works with `relplot`, not with scatterplot or lineplot
- Parameters: `col`, `row`, `col_wrap`

### Distribution Plots

**Purpose:**
- Used for univariate analysis
- Used to find out the distribution
- Range of the observation
- Central tendency
- Is the data bimodal?
- Are there outliers?

#### Histogram
- Figure level: `sns.displot()` with `kind='hist'`
- Axis level: `sns.histplot()`
- Parameters: `bins`, `hue`, `element`
- Can be applied on both numerical and categorical data

#### KDE Plot (Kernel Density Estimate)
- Provides a smooth, continuous curve representing the probability density function
- Uses a kernel function centered on each data point
- The bandwidth parameter controls the smoothness of the curve
- Figure level: `sns.displot()` with `kind='kde'`
- Axis level: `sns.kdeplot()`
- Parameters: `hue`, `fill`

#### Rugplot
- Plots marginal distribution by drawing ticks along the x and y axes
- Shows the location of individual observations in an unobstructive way
- Intended to complement other plots
- Usage: `sns.rugplot()`

#### Bivariate Plots
- **Bivariate Histogram**: Bins the data within rectangles that tile the plot and shows the count of observations with fill color
- **Bivariate KDE**: Shows density estimation for two variables

### Matrix Plots

#### HeatMap
- Plots rectangular data as a color-encoded matrix
- Axis level function: `sns.heatmap()`
- Used for visualizing matrix-like data (pivot tables, correlation matrices, etc.)
- Parameters:
  - `annot`: Display values in cells
  - `linewidth`: Width of lines dividing cells
  - `cmap`: Color palette (e.g., 'summer', 'coolwarm', 'viridis')
- Common use case: Displaying life expectancy across countries and years

#### ClusterMap
- Creates a hierarchically-clustered heatmap
- Figure level function: `sns.clustermap()`
- Automatically performs clustering on rows and columns
- Useful for identifying patterns and groupings in data
- Works well with numerical features

### Datasets Used
- `tips` - Seaborn built-in dataset
- `gapminder` - From plotly.express
- `titanic` - Seaborn built-in dataset
- `iris` - From plotly.express

---

## Learning Resources

### Video Tutorials
**Video 1 (Completed):** [Seaborn Tutorial](https://www.youtube.com/watch?v=DWVLRhnuGqI&list=PLEh1XlOqUn8LJIRnN7hRJtUOmThVbkiyr&index=6)
- Covers: Relational Plots, Distribution Plots, and Matrix Plots

**Video 2 (Upcoming):** To be covered
- Will include: Categorical Plots, Regression Plots, and Multiplots

---

## Progress Tracker

### ✅ Completed
- [x] Relational Plots (Scatter, Line, Facet)
- [x] Distribution Plots (Histogram, KDE, Rugplot, Bivariate)
- [x] Matrix Plots (HeatMap, ClusterMap)

### 📝 To Be Covered
- [ ] Categorical Plots (Barplot, Countplot, Boxplot, Violinplot, Swarmplot)
- [ ] Regression Plots (Regplot)
- [ ] Multiplots (Jointplot, Pairplot)
- [ ] Additional documentation and examples

---

**Note:** This documentation will be updated accordingly as I finish the tutorials and add new content to the notebook.