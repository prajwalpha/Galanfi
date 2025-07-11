# Galanfi Dashboard

A comprehensive energy management dashboard built with React Native and Expo Router, featuring real-time monitoring, analytics, and reporting capabilities for electrical systems.

## Features

### 🏠 Dashboard
- Real-time energy consumption monitoring
- Live device status indicators
- Key performance metrics (Total Energy, Cost, Peak Load, Efficiency)
- 24-hour energy consumption charts
- Current time and time range displays

### 📊 Analytics & Reporting
- **Energy Trends**: Historical analysis with forecasting capabilities
- **Asset Analytics**: Comprehensive asset performance monitoring
- **Consumption Reports**: Detailed energy consumption analysis with cost breakdown
- **History**: Complete parameter history with filtering and search

### 🔌 IoT Device Management
- Device status monitoring (Online/Offline/Maintenance)
- Battery level and signal strength indicators
- Add new devices functionality
- Real-time device health monitoring

### ⚙️ Parameter Selection
- Comprehensive electrical parameter selection
- Hierarchical organization (Groups > Sub-groups > Meters > Parameters)
- 200+ electrical parameters including:
  - Voltage measurements (L1-N, L2-N, L3-N, L1-L2, L2-L3, L3-L1)
  - Current measurements (L1, L2, L3, Neutral)
  - Power measurements (Active, Reactive, Apparent, Power Factor)
  - Power quality parameters (THD, Harmonics, Voltage Unbalance)
  - Protection relay status and monitoring

## Architecture

### 📁 Project Structure
```
├── app/                     # App Router pages
│   ├── (tabs)/             # Tab navigation
│   │   ├── index.tsx       # Dashboard
│   │   ├── iot-devices.tsx # IoT Devices
│   │   └── settings.tsx    # Settings
│   ├── history.tsx         # History page
│   ├── energy-reports.tsx  # Energy Reports
│   ├── energy-trends.tsx   # Energy Trends
│   ├── asset-analytics.tsx # Asset Analytics
│   └── consumption-reports.tsx # Consumption Reports
├── components/             # Reusable UI components
│   └── ui/
│       ├── MetricCard.tsx
│       ├── EnergyChart.tsx
│       ├── DataTable.tsx
│       ├── LiveIndicator.tsx
│       ├── ParameterSelectionPanel.tsx
│       └── DropdownSelect.tsx
├── services/               # API services
│   ├── api.ts             # Main API functions
│   └── electricalParameterService.ts
├── types/                  # TypeScript definitions
└── constants/             # App constants
```

### 🎨 Design System
- **Dark Theme**: Professional dark color scheme
- **Responsive Design**: Optimized for mobile and tablet
- **Material Icons**: Consistent iconography
- **Color Palette**:
  - Primary: `#4a90e2` (Blue)
  - Success: `#27ae60` (Green)
  - Warning: `#f39c12` (Orange)
  - Error: `#e74c3c` (Red)
  - Background: `#0f0f23` (Dark Blue)
  - Card Background: `#1a1a2e` (Lighter Dark Blue)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd galanfi-dashboard
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npx expo start
   ```

4. **Run on device/simulator**
   - iOS: Press `i` in the terminal or scan QR code with Expo Go
   - Android: Press `a` in the terminal or scan QR code with Expo Go
   - Web: Press `w` in the terminal

## Configuration

### Environment Variables
Create a `.env` file in the root directory:
```
EXPO_PUBLIC_API_URL=your_api_url_here
```

### API Configuration
The app uses mock data by default. To connect to a real API:

1. Update the API base URL in `services/api.ts`
2. Replace mock functions with actual API calls
3. Ensure proper error handling and loading states

## Key Components

### Parameter Selection System
The app features a sophisticated parameter selection system:

- **Hierarchical Structure**: Groups → Sub-groups → Meters → Parameters
- **200+ Parameters**: Comprehensive electrical parameter coverage
- **Real-time Search**: Filter parameters by name or description
- **Category Organization**: Parameters grouped by type (voltage, current, power, etc.)
- **Bulk Selection**: Select/deselect all parameters at once

### Real-time Monitoring
- Live data updates every 30 seconds
- WebSocket support for real-time parameter values
- Status indicators for system health
- Automatic reconnection on connection loss

### Advanced Analytics
- Historical trend analysis
- Predictive forecasting
- Power quality analysis
- Cost optimization recommendations

## Development

### Adding New Features
1. Define types in `types/index.ts`
2. Create API functions in `services/api.ts`
3. Build UI components in `components/ui/`
4. Implement pages in `app/`

### Testing
```bash
# Run tests
npm test

# Run with coverage
npm run test:coverage
```

### Building for Production
```bash
# Build for production
npx expo build

# Create standalone app
npx expo build:android
npx expo build:ios
```

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit changes: `git commit -am 'Add new feature'`
4. Push to branch: `git push origin feature/new-feature`
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions, please create an issue in the GitHub repository.