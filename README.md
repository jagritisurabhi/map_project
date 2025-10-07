# Interactive Regional Analytics

A comprehensive, interactive web application for visualizing multi-dimensional regional data across different countries. This project provides an intuitive interface to explore economic, demographic, social, and environmental metrics with advanced hierarchical filtering and real-time visualization.

## Features

### Interactive Map Visualization
- **Dynamic Mapping**: Interactive map powered by Leaflet.js
- **Regional Data**: Visual representation of 37 different metrics across 8 categories
- **Real-time Updates**: Instant data updates based on user selections
- **Color-coded Regions**: Distinct colors for easy region identification
- **Data Labels**: In-region data display with current values and units
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices

### Advanced Hierarchical Filtering System
- **Country Selection**: Choose from multiple countries (Netherlands, Germany, France, Belgium)
- **Category-based Filtering**: 8 main categories with specialized metrics
- **Dynamic Metric Selection**: 37 total metrics across all categories
- **Year Range**: Select data from 2020 to 2025
- **Smart Units**: Automatic unit display based on metric type
- **Real-time Updates**: Instant map and label updates on filter changes

### Data Categories & Metrics

#### Economic (6 metrics)
- GRP (EUR bn), House Prices (EUR/m²), Rental Prices (EUR/m²)
- Tourism (Overnight Stays), Startup Density, Poverty Rate

#### Demographic (3 metrics)
- Population, Aging Population (65+), Immigration Rate

#### Crime & Safety (5 metrics)
- Gun Violence, Total Crime Rate, Property Crime
- Violent Crime, Drug-related Crime

#### Transportation (5 metrics)
- Road Accidents, Fatal Road Accidents, Public Transport Usage
- Bicycle Accidents, Traffic Density

#### Health (4 metrics)
- Life Expectancy, Infant Mortality, Hospital Beds
- Mental Health Services

#### Education & Employment (5 metrics)
- Unemployment Rate, Higher Education, Student Population
- R&D Expenditure, Innovation Index

#### Environment (5 metrics)
- Air Quality (PM2.5), Green Energy, Waste Generation
- Water Quality, Protected Areas

#### Social & Cultural (4 metrics)
- Cultural Events, Museum Visits, Library Usage
- Sports Participation

### Professional Interface
- **Modern Design**: Clean, gradient-based header with professional styling
- **Hierarchical Navigation**: Intuitive category and metric selection
- **Smooth Animations**: Hover effects and transitions for enhanced user experience
- **Accessibility**: Proper focus states and keyboard navigation support
- **Mobile Responsive**: Optimized layout for all screen sizes

### Data Sources & Methodology
- **Comprehensive Sources**: Detailed information about data origins and methodology
- **Category-specific Resources**: Tailored data source information for each category
- **Technical Documentation**: Complete implementation details and data processing methods
- **Transparency**: Clear licensing and update information
- **Dynamic Content**: Sources modal updates based on current selections

## Technology Stack

### Frontend
- **HTML5**: Semantic markup and structure
- **CSS3**: Modern styling with gradients, flexbox, and responsive design
- **JavaScript (ES6+)**: Interactive functionality and data manipulation
- **Leaflet.js**: Interactive mapping library
- **TopoJSON**: Efficient geographic data format

### Data Processing
- **GeoJSON**: Standard geographic data format
- **CSV Processing**: Automated data transformation and mapping
- **JSON**: Structured data storage with hierarchical categories
- **Data Generation**: Automated script for comprehensive data creation

### Development Tools
- **Git**: Version control
- **Node.js**: Development server and data processing
- **HTTP Server**: Local development environment

## Project Structure

```
map_project/
├── index.html              # Main application file
├── data/
│   ├── nl_prov_raw.geojson # Raw Netherlands provinces data
│   ├── nl_provinces_iso.csv # Province ISO code mapping
│   ├── values.json         # Comprehensive data (8 categories, 37 metrics)
│   └── nl_provinces.topo.json # Processed TopoJSON data
├── .gitignore              # Git ignore rules
└── README.md               # Project documentation
```

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local HTTP server (for development)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/jagritisurabhi/map_project.git
   cd map_project
   ```

2. **Start a local server**
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js
   npx http-server -p 8000
   
   # Using PHP
   php -S localhost:8000
   ```

3. **Open in browser**
   Navigate to `http://localhost:8000`

### Development Setup

1. **Data Processing** (if needed)
   ```bash
   # Install dependencies
   npm install csv-parser topojson-server topojson-client
   
   # Process data
   node process_data.js
   ```

2. **Customization**
   - Modify `data/values.json` for different datasets
   - Update `data/nl_provinces.topo.json` for different regions
   - Customize styling in the `<style>` section of `index.html`

## Usage

### Basic Navigation
1. **Select Country**: Choose from the country dropdown
2. **Choose Category**: Select from 8 main categories (Economic, Demographic, etc.)
3. **Pick Metric**: Select specific metric within the category
4. **Select Year**: Choose desired year (2020-2025)
5. **View Data**: Observe color-coded regions and data labels
6. **Access Sources**: Click "Sources" for detailed data information

### Interactive Features
- **Hover Effects**: Hover over regions to see highlighted boundaries
- **Click Interactions**: Click regions for detailed information
- **Dynamic Legend**: Legend updates automatically with data changes
- **Category Switching**: Seamless switching between different data categories
- **Metric Updates**: Real-time updates when changing metrics
- **Responsive Design**: Interface adapts to different screen sizes

### Advanced Features
- **Hierarchical Filtering**: Navigate through categories and sub-metrics
- **Smart Unit Display**: Automatic unit formatting based on metric type
- **Data Precision**: Intelligent rounding based on data type
- **Province Labels**: In-region data display with current values
- **Sources Modal**: Comprehensive data source information

## Data Sources

### Netherlands (Available)
- **Geographic Data**: Statistics Netherlands (CBS)
- **Economic Data**: Statistics Netherlands (CBS)
- **Format**: GeoJSON converted to TopoJSON
- **License**: Open Data (CC BY 4.0)
- **Last Updated**: 2024
- **Coverage**: 12 provinces, 8 categories, 37 metrics

### Other Countries (In Development)
- **Germany**: Federal Statistical Office (Destatis)
- **France**: National Institute of Statistics (INSEE)
- **Belgium**: Statistics Belgium

## Technical Implementation

### Map Technology
- **Mapping Library**: Leaflet.js v1.9.4
- **Data Format**: TopoJSON (compressed GeoJSON)
- **Tile Source**: OpenStreetMap
- **Projection**: WGS84 (EPSG:4326)
- **Data Structure**: Hierarchical categories with dynamic metric loading

### Data Processing
- **Base Year**: 2020 for all metrics
- **Calculation Method**: Compound Annual Growth Rate (CAGR)
- **Data Range**: 2020-2025 projections
- **Region Mapping**: ISO 3166-2 codes mapped to region names
- **Color Coding**: Distinct colors assigned to each region
- **Precision Handling**: Automatic rounding based on metric type

### Performance Optimizations
- **TopoJSON Compression**: Reduced file sizes for faster loading
- **Efficient Rendering**: Optimized map rendering and data updates
- **Responsive Images**: Adaptive tile loading based on zoom level
- **Caching**: Browser caching for improved performance
- **Dynamic Loading**: Category-based metric loading for efficiency

## Browser Support

- **Chrome**: 60+
- **Firefox**: 55+
- **Safari**: 12+
- **Edge**: 79+

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Leaflet.js**: For the excellent mapping library
- **OpenStreetMap**: For providing free map tiles
- **Statistics Netherlands (CBS)**: For providing open data
- **TopoJSON**: For the efficient geographic data format

## Roadmap

### Phase 1 (Current)
- Netherlands provinces visualization
- 8 categories with 37 metrics
- Hierarchical filtering system
- Advanced data visualization

### Phase 2 (Planned)
- Additional countries (Germany, France, Belgium)
- More specialized metrics
- Advanced filtering options
- Data export functionality
- Time series animation

### Phase 3 (Future)
- Comparative analysis tools
- Custom data upload
- API integration
- Machine learning insights
- Real-time data updates

## Support

For support, questions, or feature requests, please open an issue on GitHub or contact the development team.

## Changelog

### Version 2.0.0 (Latest)
- **Hierarchical Filter System**: 8 categories with 37 total metrics
- **Advanced Data Visualization**: Comprehensive regional analytics
- **Enhanced UI/UX**: Professional design with responsive layout
- **Dynamic Sources Modal**: Category-specific data source information
- **Improved Performance**: Optimized data loading and rendering
- **Mobile Responsive**: Enhanced mobile experience

### Version 1.0.0
- Initial release with Netherlands provinces
- GDP and Population data visualization
- Basic filtering system
- Professional UI design
- Responsive layout
- Data sources documentation