# Interactive Regional Analytics

A modern, interactive web application for visualizing economic and demographic data across different regions. This project provides an intuitive interface to explore GDP and population data with dynamic filtering and real-time visualization.

## Features

### Interactive Map Visualization
- **Dynamic Mapping**: Interactive map powered by Leaflet.js
- **Regional Data**: Visual representation of economic and demographic metrics
- **Real-time Updates**: Instant data updates based on user selections
- **Color-coded Regions**: Distinct colors for easy region identification
- **Data Labels**: In-region data display with current values

### Advanced Filtering System
- **Country Selection**: Choose from multiple countries (Netherlands, Germany, France, Belgium)
- **Metric Selection**: Toggle between GDP (Gross Regional Product) and Population data
- **Year Range**: Select data from 2020 to 2025
- **Dynamic Units**: Automatic unit display (EUR billions for GDP, People for Population)

### Professional Interface
- **Modern Design**: Clean, gradient-based header with professional styling
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Smooth Animations**: Hover effects and transitions for enhanced user experience
- **Accessibility**: Proper focus states and keyboard navigation support

### Data Sources & Methodology
- **Comprehensive Sources**: Detailed information about data origins and methodology
- **Country-specific Resources**: Tailored data source information for each country
- **Technical Documentation**: Complete implementation details and data processing methods
- **Transparency**: Clear licensing and update information

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
- **JSON**: Structured data storage and retrieval

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
│   ├── values.json         # Economic and demographic data
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
2. **Choose Metric**: Select GDP or Population data
3. **Pick Year**: Select desired year (2020-2025)
4. **View Data**: Observe color-coded regions and data labels
5. **Access Sources**: Click "Sources" for detailed data information

### Interactive Features
- **Hover Effects**: Hover over regions to see highlighted boundaries
- **Click Interactions**: Click regions for detailed information
- **Dynamic Legend**: Legend updates automatically with data changes
- **Responsive Design**: Interface adapts to different screen sizes

## Data Sources

### Netherlands (Available)
- **Geographic Data**: Statistics Netherlands (CBS)
- **Economic Data**: Statistics Netherlands (CBS)
- **Format**: GeoJSON converted to TopoJSON
- **License**: Open Data (CC BY 4.0)
- **Last Updated**: 2024

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

### Data Processing
- **GDP Calculation**: Compound Annual Growth Rate (CAGR) from 2020 base year
- **Population Growth**: Annual growth rate applied from 2020 base year
- **Region Mapping**: ISO 3166-2 codes mapped to region names
- **Color Coding**: Distinct colors assigned to each region

### Performance Optimizations
- **TopoJSON Compression**: Reduced file sizes for faster loading
- **Efficient Rendering**: Optimized map rendering and data updates
- **Responsive Images**: Adaptive tile loading based on zoom level
- **Caching**: Browser caching for improved performance

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
- GDP and Population data
- Basic filtering and interaction

### Phase 2 (Planned)
- Additional countries (Germany, France, Belgium)
- More economic indicators
- Advanced filtering options
- Data export functionality

### Phase 3 (Future)
- Time series animation
- Comparative analysis tools
- Custom data upload
- API integration

## Support

For support, questions, or feature requests, please open an issue on GitHub or contact the development team.

## Changelog

### Version 1.0.0
- Initial release with Netherlands provinces
- GDP and Population data visualization
- Interactive filtering system
- Professional UI design
- Responsive layout
- Data sources documentation
