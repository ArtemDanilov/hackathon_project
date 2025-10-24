# FlowmapBlue Example Datasets

This directory contains example datasets for demonstrating FlowmapBlue visualization capabilities.

## Available Datasets

### 1. US Cities (`us-cities.json`)
- **Description**: Major US cities with flow connections
- **Nodes**: 10 cities (New York, Los Angeles, Chicago, Houston, Phoenix, etc.)
- **Flows**: 10 connections between cities
- **Use Case**: Demonstrates domestic migration or trade flows

### 2. European Cities (`european-cities.json`)
- **Description**: Major European cities with circular flow pattern
- **Nodes**: 10 cities (London, Paris, Berlin, Madrid, Rome, etc.)
- **Flows**: 10 connections forming a circular pattern
- **Use Case**: Shows European travel or trade routes

### 3. US Airports (`us-airports.json`)
- **Description**: Major US airports with flight connections
- **Nodes**: 10 airports (JFK, LAX, O'Hare, DFW, Denver, etc.)
- **Flows**: 10 flight routes with varying passenger counts
- **Use Case**: Airline route visualization and passenger flow analysis

### 4. World Countries (`world-countries.json`)
- **Description**: Major world countries with global trade flows
- **Nodes**: 10 countries (USA, China, India, Brazil, Russia, etc.)
- **Flows**: 10 international trade connections
- **Use Case**: Global trade visualization and economic relationships

### 5. Tech Hubs (`tech-hubs.json`)
- **Description**: US tech hubs with talent migration flows
- **Nodes**: 10 tech cities (Silicon Valley, Seattle, Austin, Boston, etc.)
- **Flows**: 10 talent migration routes
- **Use Case**: Tech industry talent flow and innovation centers

## Data Format

Each dataset follows this structure:

```json
{
  "nodes": [
    {
      "id": "unique_identifier",
      "lat": latitude_coordinate,
      "lon": longitude_coordinate,
      "name": "Human Readable Name"
    }
  ],
  "flows": [
    {
      "origin": "origin_node_id",
      "dest": "destination_node_id",
      "count": flow_magnitude
    }
  ]
}
```

## Usage

1. Start the Laravel server: `php artisan serve`
2. Open `http://localhost:8000`
3. Use the buttons at the top to switch between different datasets
4. The map will automatically adjust center and zoom for each dataset

## Customization

To add your own dataset:

1. Create a new JSON file in this directory following the format above
2. Add a button in the welcome.blade.php file
3. Update the `loadDataset()` function to handle your new dataset
4. Adjust map center and zoom settings as needed

## Notes

- All coordinates are in decimal degrees (WGS84)
- Flow magnitudes are arbitrary units for demonstration
- Map automatically flies to appropriate center/zoom for each dataset
- Error handling included for failed data loads
