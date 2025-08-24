# Simple Finance Dashboard 💰

A user-friendly Streamlit web application for analyzing personal bank transactions with automatic categorization and interactive visualizations.

## Features

- 📁 **CSV File Upload**: Upload your bank statement CSV files directly
- 📊 **Sample Data**: Try the app instantly with a sample bank statement
- 🏷️ **Smart Categorization**: Automatic transaction categorization with keyword matching
- 📈 **Interactive Charts**: Beautiful pie charts and bar charts for expense visualization
- ✏️ **Manual Editing**: Edit categories directly in an interactive data table
- 💾 **Persistent Storage**: Categories and keywords are saved automatically
- 💰 **Expense Tracking**: Separate views for expenses (debits) and payments (credits)

## Installation

1. **Clone or download the repository**
2. **Install required packages**:
   ```bash
   pip install streamlit pandas plotly
   ```

## Usage

1. **Run the application**:
   ```bash
   streamlit run app.py
   ```

2. **Choose your data source**:
   - Upload your own CSV bank statement, OR
   - Click "Press to use Sample Bank Statement" to try with demo data

3. **Categorize your transactions**:
   - Create new categories using the text input
   - Edit transaction categories in the interactive table
   - Apply changes to save category assignments

4. **View your financial insights**:
   - Expense summary table
   - Interactive pie chart showing spending distribution
   - Bar chart for category comparison

### Sample CSV Format:
```csv
Date,Details,Amount,Currency,Debit/Credit,Status,
28 Feb 2025,Card Payment Received,"18,551.62",AED,Credit,SETTLED, 
15 Feb 2025,EMIRATES INSURANCE,137.95,AED,Debit,SETTLED
04 Feb 2025,NOON.COM,110.69,AED,Debit,SETTLED
23 Feb 2025,Card Payment Received,"12,351.42",AED,Credit,SETTLED
05 Oct 2024,LULU HYPERMARKET,455.00,AED,Debit,SETTLED
```

## How Categorization Works

1. **Automatic Matching**: The app matches transaction details with saved keywords
2. **Manual Assignment**: Edit categories directly in the data table
3. **Keyword Learning**: When you assign a category, the transaction detail becomes a keyword for future automatic categorization
4. **Persistent Storage**: All categories and keywords are saved in `categories.json`

## File Structure

```
finance-dashboard/
├── app.py                    # Main Streamlit application
├── categories.json           # Stored categories and keywords
├── sample_bank_statement.csv # Sample data file
└── README.md                 # This file
```

## Requirements

- Python 3.7+
- Streamlit
- Pandas
- Plotly Express

## How to Download Bank Statements

Most banks provide CSV export functionality:

1. Log in to your bank's online portal
2. Navigate to 'Statements' or 'Transaction History'
3. Select your account and desired date range
4. Choose 'CSV' as the download format
5. Save the file and upload it to the app

## Features in Detail

### 🏷️ Category Management
- Create custom categories for your spending
- Automatic keyword-based categorization
- Manual category editing with instant updates

### 📊 Visualizations
- **Pie Chart**: Shows percentage breakdown of spending by category
- **Bar Chart**: Compares absolute amounts across categories
- **Summary Table**: Detailed category totals

### 💾 Data Persistence
- Categories and keywords are automatically saved
- Session state management for smooth user experience
- No data loss during app interactions

## Troubleshooting

**File Upload Issues**:
- Ensure your CSV has the required columns
- Check date format matches `DD MMM YYYY` (e.g., `15 Jan 2024`)
- Remove any special characters from amount column

**Categorization Not Working**:
- Keywords are case-insensitive and match exact transaction details
- Try editing categories manually first to build the keyword database

**App Not Starting**:
- Verify all dependencies are installed
- Ensure you're running Python 3.7 or higher

## Contributing

Feel free to submit issues and feature requests! This is a simple finance dashboard designed to be easily customizable for different banking formats and currencies.

## License

This project is open source and available under the MIT License.
