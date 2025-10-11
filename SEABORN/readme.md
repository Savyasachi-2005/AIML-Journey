# SEABORN

## Overview
Seaborn is easy to use and is a better version of matplotlib with more graphs included. It's a famous Python visualization library.

## Types of Functions
- **Figure level**
- **Axes level**

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
- Axes level: `sns.scatterplot()`
- Figure level: `sns.relplot()` with `kind='scatter'`
- Parameters: `data`, `x`, `y`, `hue`, `style`, `size`

#### Line Plot
- Axes level: `sns.lineplot()`
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
- Axes level: `sns.histplot()`
- Parameters: `bins`, `hue`, `element`
- Can be applied on both numerical and categorical data

#### KDE Plot (Kernel Density Estimate)
- Provides a smooth, continuous curve representing the probability density function
- Uses a kernel function centered on each data point
- The bandwidth parameter controls the smoothness of the curve
- Figure level: `sns.displot()` with `kind='kde'`
- Axes level: `sns.kdeplot()`
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
- Axes level function: `sns.heatmap()`
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

### Categorical Plots

**Purpose:** Used to visualize relationships between categorical variables and numerical variables, or distributions across categories.

#### Categorical Scatter Plots

**Strip Plot**
- Axes level: `sns.stripplot()`
- Figure level: `sns.catplot()` with `kind='strip'`
- Creates a categorical scatter plot
- Parameters: `jitter` (adds random noise to prevent overlap), `hue`
- Useful for showing individual data points

**Swarm Plot**
- Axes level: `sns.swarmplot()`
- Figure level: `sns.catplot()` with `kind='swarm'`
- Similar to strip plot but automatically adjusts points to avoid overlap
- Better for smaller datasets
- Parameters: `hue`

#### Categorical Distribution Plots

**Box Plot**
- Axes level: `sns.boxplot()`
- Figure level: `sns.catplot()` with `kind='box'`
- Displays distribution based on five-number summary:
  - Minimum
  - First Quartile (Q1)
  - Median
  - Third Quartile (Q3)
  - Maximum
- Shows outliers, symmetry, data grouping, and skewness
- Can create single boxplot for numerical data only
- Parameters: `hue`, `x`, `y`

**Violin Plot**
- Axes level: `sns.violinplot()`
- Figure level: `sns.catplot()` with `kind='violin'`
- Combination of boxplot and KDE plot
- Shows the probability density of data at different values
- Parameters: `hue`, `split` (splits violin for hue categories)

#### Categorical Estimate Plots

**Bar Plot**
- Axes level: `sns.barplot()`
- Figure level: `sns.catplot()` with `kind='bar'`
- Shows estimates of central tendency (mean by default)
- Parameters:
  - `estimator`: Statistical function (e.g., `np.std`, `np.min`, `np.max`)
  - `ci` or `errorbar`: Confidence interval display
  - `hue`: Multiple categories

**Point Plot**
- Axes level: `sns.pointplot()`
- Figure level: `sns.catplot()` with `kind='point'`
- Shows point estimates and confidence intervals
- Useful for showing trends across categories
- Parameters: `hue`, `errorbar`

**Count Plot**
- Axes level: `sns.countplot()`
- Figure level: `sns.catplot()` with `kind='count'`
- Shows the count of observations in each category
- Similar to histogram but for categorical variables
- Parameters: `hue`

#### Faceting with catplot
- Can create faceted plots using `col` and `row` parameters
- Allows visualization across multiple categorical dimensions

### Regression Plots

**Purpose:** Draw a scatterplot of two variables (x & y), fit a regression model y~x, and plot the resulting regression line with a 95% confidence interval.

#### Reg Plot
- Axes level: `sns.regplot()`
- Simple regression plot
- Does NOT support `hue` parameter
- Best for single regression line

#### LM Plot (Linear Model Plot)
- Figure level: `sns.lmplot()`
- Supports `hue` parameter for multiple regression lines
- Allows faceting with `col` and `row`
- More flexible than regplot

#### Resid Plot (Residual Plot)
- `sns.residplot()`
- Plots residuals of regression
- Useful for checking regression assumptions
- Shows the difference between observed and predicted values

### Multi-Plots

#### FacetGrid
- Second way to create faceted plots
- More flexible than using `col` and `row` in other functions
- Usage:
  ```python
  g = sns.FacetGrid(data=tips, col='day', row='time')
  g.map(sns.scatterplot, 'tip', 'total_bill')
  g.add_legend()
  ```

#### Pairwise Relationships

**Pair Plot**
- Figure level: `sns.pairplot()`
- Creates a grid of plots showing pairwise relationships
- Diagonal shows distribution of each variable
- Off-diagonal shows scatter plots between variables
- Parameters: `hue` (color by category)
- Great for exploring relationships in datasets

**PairGrid**
- More flexible version of pairplot
- Allows custom plot types for different sections:
  - `g.map()`: Apply to all plots
  - `g.map_diag()`: Apply to diagonal plots
  - `g.map_offdiag()`: Apply to off-diagonal plots
  - `g.map_upper()`: Apply to upper triangle
  - `g.map_lower()`: Apply to lower triangle
- Example combinations:
  - Diagonal: histogram, violinplot, KDE
  - Off-diagonal: scatterplot, boxplot, histogram

#### Joint Plots

**Joint Plot**
- Figure level: `sns.jointplot()`
- Combines bivariate plot with univariate plots on margins
- Available kinds: `'scatter'`, `'hist'`, `'hex'`, `'kde'`, `'reg'`, `'resid'`
- Shows relationship between two variables with their distributions

**JointGrid**
- More flexible version of jointplot
- Allows custom plot combinations
- Usage:
  ```python
  g = sns.JointGrid(data=tips, x='total_bill', y='tip')
  g.plot(sns.scatterplot, sns.violinplot)
  ```

### Useful Seaborn Functions

- `sns.get_dataset_names()` - Get list of all available built-in datasets
- `sns.load_dataset('dataset_name')` - Load a built-in dataset

### Datasets Used
- `tips` - Seaborn built-in dataset
- `gapminder` - From plotly.express
- `titanic` - Seaborn built-in dataset
- `iris` - From plotly.express

---

## Learning Resources

### Video Tutorials
**Video 1 (Completed):** [Seaborn Tutorial - Part 1](https://www.youtube.com/watch?v=DWVLRhnuGqI&list=PLEh1XlOqUn8LJIRnN7hRJtUOmThVbkiyr&index=6)
- Covers: Relational Plots, Distribution Plots, and Matrix Plots

**Video 2 (Completed):** [Seaborn Tutorial - Part 2](https://www.youtube.com/live/kLWeKeqc9Ms?si=pUB9qjOoZV57B4g1)
- Covers: Categorical Plots, Regression Plots, and Multiplots

---

## Progress Tracker

### ✅ Completed
- [x] Relational Plots (Scatter, Line, Facet)
- [x] Distribution Plots (Histogram, KDE, Rugplot, Bivariate)
- [x] Matrix Plots (HeatMap, ClusterMap)
- [x] Categorical Plots (Strip, Swarm, Box, Violin, Bar, Point, Count)
- [x] Regression Plots (Regplot, LMplot, Residplot)
- [x] Multiplots (FacetGrid, Pairplot, PairGrid, Jointplot, JointGrid)

---

**Note:** This documentation will be updated accordingly as I finish the tutorials and add new content to the notebook.