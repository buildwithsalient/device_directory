# Radio Device Directory - Device Database

This repository contains the device database for the Radio Device Directory application. The database is stored as a JSON file that manufacturers can update through pull requests.

## For Manufacturers - How to Submit a Device

1. **Fork this repository** to your GitHub account
2. **Edit the `devices.json` file** to add your device information
3. **Submit a pull request** with your changes
4. **Wait for review** - we'll review your submission and merge it if approved

## Device Data Format

Each device entry should follow this JSON structure:

```json
{
  "name": "Your Device Name",
  "description": "Detailed description of the device and its capabilities",
  "manufacturer": "Your Company Name",
  "type": "HAM",
  "frequency_range": "2.4 GHz",
  "power_output": 0.5,
  "price": 39.99,
  "software": "Optional software information",
  "connectivity": ["Bluetooth", "WiFi", "USB"],
  "purchase_date": "2025-05-22",
  "purchase_url": "https://your-store.com/product-link"
}
```

### Field Descriptions

- **name** (required): The full product name
- **description** (required): Detailed description of the device
- **manufacturer** (required): Your company or brand name
- **type** (required): Device category (e.g., "HAM", "IoT", "LoRa")
- **frequency_range** (required): Operating frequency (e.g., "2.4 GHz", "868/915 MHz")
- **power_output** (required): Power output in watts (numeric value)
- **price** (required): Current price in USD (numeric value)
- **software** (optional): Software/firmware information
- **connectivity** (required): Array of connectivity options
- **purchase_date** (optional): Date format: "YYYY-MM-DD"
- **purchase_url** (optional): Direct link to purchase the device

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