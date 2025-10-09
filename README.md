# EPA Hydraulic Gradient Calculator

A Blazor WebAssembly application that recreates the EPA's online hydraulic gradient calculation tool for environmental site assessment.

## ?? Live Demo

Access the application at: **https://kurtw555.github.io/HydraulicGradient/**

## ?? Features

- **Hydraulic gradient calculation** using least-squares plane fitting
- Support for up to **30 data points** (ID, coordinates, head values)
- **Two calculation modes**: Head and Head Squared
- **Unit selection** for coordinates and head (feet or meters)
- **Example datasets** for testing and learning
- **Real-time calculations** with comprehensive results
- **Responsive design** that works on desktop and mobile

## ?? What It Calculates

- **Gradient magnitude** (hydraulic gradient intensity)
- **Flow direction** as degrees from north
- **R² coefficient** for statistical confidence
- **Maximum head difference** analysis
- **Number of points** used in calculation

## ?? Quick Start

### Using the Online Version
1. Visit the live demo link above
2. Click "Example Data Set 1" or "Example Data Set 2" to see sample data
3. Click "Calculate" to see results
4. Enter your own well data to analyze your site

### Running Locally
```bash
git clone https://github.com/kurtw555/HydraulicGradient.git
cd HydraulicGradient
dotnet run --project HydraulicGradient
```

## ?? How to Use

1. **Enter Site Information**
   - Site name and date
   - Select calculation basis (Head or Head Squared)
   - Choose units for coordinates and head values

2. **Input Well Data**
   - Enter well ID, X-coordinate, Y-coordinate, and head value
   - Use up to 30 data points
   - Leave unused rows empty

3. **Calculate Results**
   - Click "Calculate" button
   - Review gradient magnitude and flow direction
   - Check R² value for data quality assessment

## ??? Technical Details

- **Framework**: Blazor WebAssembly (.NET 9)
- **Hosting**: GitHub Pages (static files)
- **Calculation Method**: Least-squares plane fitting
- **Browser Compatibility**: All modern browsers
- **Offline Support**: Works offline after initial load

## ?? Mathematical Background

The application fits a plane to the head data using the equation:
```
a·x + b·y + c = h
```

Where:
- (x,y) are well coordinates
- h is the head value
- a, b, c are coefficients calculated by least-squares fitting

The hydraulic gradient is calculated as:
- **Magnitude**: ?(a² + b²)
- **Direction**: arctan(a/b) adjusted for quadrant

## ?? Deployment

This application is automatically deployed to GitHub Pages using GitHub Actions. Every push to the `main` branch triggers a new deployment.

### Local Development
```bash
# Clone the repository
git clone https://github.com/kurtw555/HydraulicGradient.git
cd HydraulicGradient

# Run locally
dotnet run --project HydraulicGradient
```

### Manual Deployment
```bash
# Build for production
dotnet publish HydraulicGradient -c Release -o publish

# The publish folder contains all files needed for hosting
```

## ?? Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## ?? License

This project is in the public domain and free to use for educational and professional purposes.

## ?? Original EPA Tool

Based on the EPA's online hydraulic gradient calculator:
https://www3.epa.gov/ceampubl/learn2model/part-two/onsite/gradient4plus-ns.html

## ?? Issues & Support

If you encounter any issues or have suggestions:
1. Check existing [Issues](https://github.com/kurtw555/HydraulicGradient/issues)
2. Create a new issue with detailed description
3. Include sample data if applicable.