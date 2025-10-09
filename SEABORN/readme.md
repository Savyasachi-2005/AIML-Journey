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

### Datasets Used
- `tips` - Seaborn built-in dataset
- `gapminder` - From plotly.express
- `titanic` - Seaborn built-in dataset

---

**Note:** More content will be added as the tutorial progresses.