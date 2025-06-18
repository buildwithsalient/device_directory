# Radio Device Directory - Device Database

This repository contains the device database for the Radio Device Directory application. The database is stored as a JSON file that manufacturers can update through pull requests.

## For Manufacturers - How to Submit a Device or Request Edits

1. **Fork this repository** to your GitHub account
2. **Edit the `devices.json` file** to add your device information, or to request changes to an existing entry (for example, if your brand wishes to update technical details, images, or other information)
3. **Submit a pull request** with your changes or requested edits
4. **Wait for review** - we'll review your submission and merge it if approved

## Device Data Format

Each device entry should follow this JSON structure:

```json
{
  "name": "Your Device Name",
  "description": "Detailed description of the device and its capabilities",
  "manufacturer": "Your Company Name",
  "brand": "Brand Name (if different from manufacturer)",
  "type": "LoRa",
  "frequency_range": "868/915 MHz",
  "power_output": 0.5,
  "price": 39.99,
  "software": ["Firmware name", "Other software"],
  "connectivity": ["Bluetooth", "WiFi", "USB"],
  "mcu": "MCU type/model",
  "lora_chip": "LoRa chip/model",
  "gps": {
    "supported": true,
    "type": "active",
    "chip": "GPS chip/model"
  },
  "battery": {
    "present": true,
    "type": "Rechargeable lithium",
    "capacity_mAh": 700,
    "charging": ["USB magnetic cable", "solar"]
  },
  "sensors": ["3-axis accelerometer", "temperature", "light"],
  "ip_rating": "IP65",
  "dimensions_mm": { "length": 85, "width": 55, "height": 6.5 },
  "weight_g": 32,
  "release_date": "2025-04-15",
  "purchase_date": "2025-06-15",
  "purchase_url": "https://your-store.com/product-link",
  "screen": { "present": true, "type": "OLED", "size": 1.3 },
  "charger_type": "USB Type-C, solar, Li-ion",
  "radios": [
    {
      "type": "LoRa",
      "antenna": { "type": "pcb trace" },
      "chip": "SX1262",
      "techniques": ["LoRa"]
    },
    {
      "type": "Bluetooth",
      "antenna": { "type": "chip" },
      "chip": "nRF52840",
      "techniques": []
    }
  ],
  "assets": [
    "https://your-store.com/images/device1.jpg",
    "https://your-store.com/images/device2.jpg"
  ]
}
```

### Field Descriptions (updated)

- **name** (required): The full product name
- **description** (required): Detailed description of the device
- **manufacturer** (required): Your company or brand name
- **brand** (optional): Brand name if different from manufacturer
- **type** (required): Device category (e.g., "HAM", "IoT", "LoRa", "Cellular")
- **frequency_range** (required): Operating frequency (e.g., "2.4 GHz", "868/915 MHz")
- **power_output** (required): Power output in watts (numeric value)
- **price** (required): Current price in USD (numeric value)
- **software** (optional): Array of software/firmware names
- **connectivity** (required): Array of connectivity options
- **mcu** (optional): MCU type/model
- **lora_chip** (optional): LoRa chip/model
- **gps** (optional): Object with `supported` (boolean), `type` (active/passive/other), and `chip` (model)
- **battery** (optional): Object with `present` (boolean), `type`, `capacity_mAh`, and `charging` (array)
- **sensors** (optional): Array of sensor types
- **ip_rating** (optional): IP rating (e.g., "IP65")
- **dimensions_mm** (optional): Object with `length`, `width`, `height` (all numbers, mm)
- **weight_g** (optional): Device weight in grams
- **release_date** (optional): Product release date (YYYY-MM-DD)
- **purchase_date** (optional): Date format: "YYYY-MM-DD"
- **purchase_url** (optional): Direct link to purchase the device
- **screen** (optional): Object with `present` (boolean), `type` (string), `size` (number, inches)
- **charger_type** (optional): String describing charger type(s)
- **radios** (optional): Array of radio interfaces, each with:
  - **type**: Radio type (e.g., "LoRa", "Wi-Fi", "Bluetooth", "Zigbee", "Cellular")
  - **antenna**: Object with `type` (antenna type, e.g., "pcb trace", "chip", "external SMA")
  - **chip**: Chip/model used for this radio (e.g., "SX1262", "nRF52840"), or null if unknown
  - **techniques**: Array of supported radio techniques (e.g., ["NB-IoT", "LTE-M"])
- **assets** (optional): Array of product image URLs

## Submission Guidelines

- Ensure all required fields are filled out
- Use accurate and up-to-date information
- Include a direct purchase link if available
- Follow the exact JSON format shown above
- Test your JSON syntax before submitting

## Review Process

All submissions will be reviewed for:
- Accuracy of technical specifications
- Proper JSON formatting
- Completeness of required information
- Appropriate categorization

## Questions?

If you have questions about the submission process, please open an issue in this repository.