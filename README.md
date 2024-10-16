# Check-in System

A simple employee check-in system that logs entries to Google Sheets. This system records when employees enter the workspace, their names, and their reason for visiting. This readme also walks through creating the google API required

## Features
- Simple command-line interface
- Automatic timestamp recording
- Google Sheets integration for easy record keeping
- Tracks employee name and reason for visit

## Prerequisites
- Python 3.7 or higher
- Google Cloud Project with Sheets API enabled
- Google account with access to Google Sheets

## Setup

### 1. Clone the Repository
```bash
git clone https://github.com/QuothingRaven/check-in_system
cd check-in_system
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Google Sheets Setup
1. Create a new Google Sheet
2. Add the following headers to Row 1:
   - A1: "Timestamp"
   - B1: "Employee Name"
   - C1: "Reason for Visit"
3. Copy the spreadsheet ID from the URL
   - URL format: `https://docs.google.com/spreadsheets/d/`**`YOUR_SPREADSHEET_ID`**`/edit`

### 4. Google Cloud Setup
1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project
3. Enable the Google Sheets API
4. Create OAuth 2.0 credentials
5. Download the credentials file as `credentials.json`
6. Place `credentials.json` in the project directory

### 5. Environment Setup
1. Copy `.env.example` to `.env`
2. Update `.env` with your spreadsheet ID

## Usage
```bash
python checkin.py
```

Follow the prompts to enter:
- Employee name
- Reason for visit

Type 'quit' at any time to exit the program.

## File Structure
```
warehouse-checkin/
├── checkin.py
├── credentials.json
├── requirements.txt
├── .env
└── README.md
```

## Security Notes
- Never commit `credentials.json` or `.env` to version control
- Keep your Google Cloud credentials secure
- Regularly review access logs and permissions

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Customization
If you need this customized to your buisness needs or would like to contribute feel free to reach by email: ravenmarketing@protonmail.com

## License
This project is licensed under the MIT License - see the LICENSE file for details
