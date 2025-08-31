# Computational Narrative: Visual Analysis of Fitness Data

A comprehensive data visualization project that analyzes fitness data using computational narrative techniques, following Rule et al's Ten Rules for effective data visualization and storytelling.

## 🏃‍♂️ Project Overview

This project provides an in-depth analysis of Strava fitness data through various visualization techniques, transforming raw GPS and performance metrics into meaningful insights about athletic performance patterns. The analysis combines basic and advanced visualization methods to tell a compelling story about fitness trends over time.

## 📊 Visualizations Included

### Basic Analysis Techniques
- **Interactive Bar Charts**: Daily total distance with cube root transformation
- **Multi-line Plots**: Enhanced speed variations (mean, max, min) over time
- **Normalized Heatmaps**: Special metrics comparison with highlighted key insights

### Advanced Analysis Techniques
- **Combined Line + Bar Charts**: Multi-metric performance analysis with dual y-axes
- **Geographical Maps**: Spatial visualization of performance data with Mercator projection

## 🎯 Key Features

- **Data-Driven Storytelling**: Follows Rule et al's Ten Rules for effective visualization
- **Modular Code Architecture**: Well-documented, reusable functions
- **Interactive Visualizations**: Enhanced user engagement with Plotly
- **Outlier Detection**: Statistical methods for data quality improvement
- **Spatial Analysis**: GPS coordinate mapping with performance overlays
- **Comprehensive Documentation**: Detailed process documentation and insights

## 📁 Project Structure

```
Computational Narrative/
│
├── src/
│   ├── computational_narrative.ipynb    # Main analysis notebook
│   └── assets/
│       ├── strava.csv                  # Fitness data (not included)
│       └── map.png                     # Background map image (not included)
│
├── requirements.txt                     # Python dependencies
├── cn_readme.md                         # Project documentation
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/fitness-data-analysis.git
   cd fitness-data-analysis
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Add your data**
   - Place your Strava CSV export in `assets/strava.csv`
   - Add a background map image as `assets/map.png` (optional)

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook notebooks/fitness_analysis.ipynb
   ```

## 📊 Data Requirements

The analysis expects a Strava data export with the following key columns:
- `timestamp`: Activity timestamps
- `enhanced_speed`: Enhanced speed measurements
- `enhanced_altitude`: Enhanced altitude data
- `heart_rate`: Heart rate measurements
- `position_lat`, `position_long`: GPS coordinates
- Special metrics: `Air Power`, `Cadence`, `Form Power`, `Ground Time`, etc.

### Exporting Your Strava Data

1. Go to [Strava Settings](https://www.strava.com/settings/privacy) → Privacy Controls
2. Request data export
3. Download and extract the activities CSV file
4. Place the file in the `assets/` directory

## 🔧 Key Functions

| Function | Description |
|----------|-------------|
| `prepare_data()` | Cleans and preprocesses raw fitness data |
| `plot_total_distance()` | Creates interactive bar chart of daily distances |
| `plot_enhanced_speed()` | Generates multi-line speed analysis plots |
| `plot_heatmap()` | Produces normalized metrics heatmap |
| `generate_combined_chart()` | Creates dual-axis performance visualization |
| `generate_geographical_map()` | Maps performance data spatially |

## 📈 Sample Insights

The analysis reveals:
- **Performance Trends**: Identification of peak performance periods
- **Activity Patterns**: Changes in training intensity over time
- **Spatial Performance**: Geographic areas of varying performance
- **Metric Correlations**: Relationships between different fitness metrics

## 🛠️ Dependencies

- `pandas` - Data manipulation and analysis
- `numpy` - Numerical computing
- `matplotlib` - Static plotting
- `seaborn` - Statistical visualization
- `plotly` - Interactive visualizations
- `scipy` - Scientific computing

## 🎨 Visualization Philosophy

This project adheres to Rule et al's Ten Rules for computational data visualization:

1. **Tell a Story for an Audience**: Each visualization serves a narrative purpose
2. **Document the Process**: Comprehensive documentation of methodology
3. **Show Uncertainty**: Statistical methods for outlier detection
4. **Modularize Code**: Reusable, well-documented functions

## 📝 Usage Examples

```python
# Load and prepare data
df = pd.read_csv('assets/strava.csv')
df_clean = prepare_data(df)

# Generate basic visualizations
plot_total_distance(df_clean)
plot_enhanced_speed(df_clean)
plot_heatmap(df_clean)

# Create advanced visualizations
generate_combined_chart(df_clean, 'date', 'enhanced_speed', 
                       'enhanced_altitude', 'heart_rate')
generate_geographical_map(df_clean, 'position_lat', 'position_long', 
                         'enhanced_speed', 'timestamp', '2019-08-17', 
                         'assets/map.png')
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Rule et al for the Ten Rules of computational data visualization
- Strava for providing comprehensive fitness data export
- The open-source Python data science community

**Note**: This project is for educational and personal use. Please respect Strava's terms of service when using their data export feature.
