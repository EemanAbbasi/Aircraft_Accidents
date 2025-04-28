# Aircraft Accident Analysis
Overview
This repository contains a Jupyter notebook (aircraft_accident_analysis.ipynb) for analyzing aircraft accidents and fatalities from 1908 to 2025, using the dataset aircraft_accidents.csv. The analysis explores accident frequency, fatality counts, and patterns by aircraft manufacturer, with a focus on potential climate change impacts (e.g., weather-related accidents due to storms or turbulence). Visualizations include pie charts, heatmaps, and bar plots, styled for publication quality (e.g., Nature standards).

Key analyses include:

#Pie Charts: Distribution of accidents and fatalities by manufacturer (e.g., Boeing, Douglas/McDonnell Douglas), with leader lines for readability.
Heatmaps: Accidents and fatalities by aircraft type and decade, highlighting temporal trends.
Bar Plots: Accidents and fatalities by manufacturer, aircraft type, operator type, and country.
Climate Change Context: Investigating whether high-fatality manufacturers or recent accidents correlate with severe weather events (e.g., storms causing 7.5% of delays, 55% turbulence increase in North Atlantic, 41% in USA, 1979–2020).

# Dataset
The dataset (aircraft_accidents.csv) contains records of aircraft accidents from 1908 to 2025, with the following columns:

##Date: Date of the accident (e.g., "17-Sep-08").
##Location / Operator: Location and operator (e.g., "Fort Myer, Virginia\nMilitary - U.S. Army").
##Aircraft Type / Registration: Aircraft type and registration (e.g., "Wright Flyer III\n?").
##Fatalities: Fatalities, aboard, and ground deaths in the format "X/Y(Z)" (e.g., "1/2(0)").

The dataset is preprocessed to:

Parse dates and correct years (e.g., 2046 → 1946).
Split Location / Operator into Location and Airline/Op.
Split Aircraft Type / Registration into AC Type and Reg.
Parse Fatalities into Fatalities, Aboard, and Ground.
Derive Manufacturer by consolidating aircraft types (e.g., Boeing 737 → "Boeing").
Add Country, Operator_Type (Military, Commercial, Private, Other), and Decade.

# Requirements
To run the notebook, install the required Python packages:
pip install pandas matplotlib seaborn numpy

The notebook uses:

Pandas: Data manipulation and analysis.
Matplotlib/Seaborn: Creating visualizations (pie charts, heatmaps, bar plots).
NumPy: Numerical operations.

# Setup

Clone the repository:
git clone https://github.com/your-username/aircraft-accident-analysis.git
cd aircraft-accident-analysis


Ensure the dataset (aircraft_accidents.csv) is in the same directory as the notebook.

Install dependencies (see Requirements).

Open the notebook:
jupyter notebook aircraft_accident_analysis.ipynb


Run the cells to reproduce the analysis and visualizations.


# Visualizations
The notebook includes the following visualizations, saved as images in the plots/ directory:

Pie Chart (Fatalities by Manufacturer): Proportion of fatalities by manufacturer, with leader lines to reduce label clutter.
Pie Chart (Accidents by Manufacturer): Distribution of accidents by manufacturer.
Heatmaps: Accidents and fatalities by aircraft type and decade, showing temporal patterns.
Bar Plots: Accidents and fatalities by manufacturer, aircraft type, operator type, and country.

To view plots on GitHub, the notebook uses Markdown cells with embedded image references (see below).
Displaying Plots on GitHub
GitHub renders Jupyter notebooks, but plots generated in code cells may not display unless saved as images and referenced in Markdown cells. Follow these steps to ensure plots are visible:

Save Plots as Images:Each plot is saved using plt.savefig() with a high DPI (300 for Nature quality). For example:
plt.savefig('plots/fatalities_by_manufacturer_pie.png', dpi=300, bbox_inches='tight', format='png')

Images are stored in the plots/ directory.

Add Markdown Cells:After each plot’s code cell, insert a Markdown cell to display the image:
![Fatalities by Manufacturer](plots/fatalities_by_manufacturer_pie.png)

Ensure the filename matches exactly, including case sensitivity.

Commit Images to GitHub:Include all plot images in the repository:
```bash
git add plots/*.png
git commit -m "Add plot images"
git push origin main
```


Example Notebook Structure:
## Fatalities by Manufacturer
The following pie chart shows the distribution of fatalities by aircraft manufacturer, with leader lines for readability.
```python
# Code to generate pie chart
plt.savefig('plots/fatalities_by_manufacturer_pie.png', dpi=300, bbox_inches='tight', format='png')
plt.show()
```

Dataset sourced from aviation accident records (1908–2025).
Visualizations styled for Nature publishing quality, inspired by scientific publication standards.
Analysis considers climate change impacts, referencing studies on storm delays (7.5%) and turbulence increases (55% in North Atlantic, 41% in USA, 1979–2020).
