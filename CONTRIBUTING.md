# Contributing to Radio Device Directory

Thank you for your interest in contributing to the Radio Device Directory! This guide will help you understand how to submit device information and contribute to our community-driven database.

## How to Contribute Device Information

### Step 1: Fork the Repository
1. Click the "Fork" button at the top right of this repository
2. Clone your fork to your local machine:
   ```bash
   git clone https://github.com/YOUR_USERNAME/radio-device-directory-db.git
   cd radio-device-directory-db
   ```

### Step 2: Add Your Device
1. Open the `devices.json` file
2. Add your device information to the JSON array
3. Follow the exact format shown in the examples

### Step 3: Validate Your Changes
1. Ensure your JSON is valid using a tool like [JSONLint](https://jsonlint.com/)
2. Verify all required fields are completed
3. Double-check that your device isn't already in the database

### Step 4: Submit Your Changes
1. Commit your changes:
   ```bash
   git add devices.json
   git commit -m "Add [Device Name] by [Manufacturer]"
   git push origin main
   ```
2. Create a pull request from your fork to this repository
3. Fill out the pull request template with device details

## Device Data Requirements

### Required Fields
- `name`: Full product name
- `description`: Detailed description of capabilities
- `manufacturer`: Company or brand name
- `type`: Device category (HAM, IoT, LoRa, etc.)
- `frequency_range`: Operating frequency specification
- `power_output`: Power output in watts (numeric)
- `price`: Current price in USD (numeric)
- `connectivity`: Array of connectivity options

### Optional Fields
- `software`: Software/firmware information
- `purchase_date`: Date in YYYY-MM-DD format
- `purchase_url`: Direct purchase link

## Review Process

All submissions are reviewed for:
- Technical accuracy
- Complete information
- Proper formatting
- No duplicate entries

## Community Guidelines

- Provide accurate, up-to-date information
- Include helpful descriptions for end users
- Keep manufacturer and product names consistent
- Use official product names and specifications
- Include working purchase links when possible

## Questions or Issues?

If you need help or have questions about the contribution process, please:
1. Check existing issues first
2. Open a new issue with your question
3. Tag it with the "question" label

Thank you for helping build a comprehensive resource for the radio community!