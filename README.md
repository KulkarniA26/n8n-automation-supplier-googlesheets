# n8n-automation-supplier-googlesheets
n8n automation for find suppliers for a given product using a local llm
This automated workflow leverages n8n, Google Sheets, and AI (Ollama LLM) to streamline supplier discovery for any product or service. Simply input your search query, and the system automatically generates a comprehensive, structured spreadsheet containing verified supplier information including company names, websites, contact details, and phone numbers.​​

Built for: Procurement professionals, supply chain managers, business owners, and anyone who needs to source suppliers efficiently without expensive enterprise software.​

✨ Features
Chat-Based Input: Natural language interface powered by n8n's chat trigger for intuitive interaction​​

AI-Driven Search: Uses Ollama Chat Model to intelligently parse queries and generate relevant supplier data​

Structured Output: Automatically organizes results into clean Google Sheets with standardized columns​​

Multi-Step Processing: Smart data splitting and field editing ensure accurate, well-formatted results​​

Real-Time Execution: See results populate in your spreadsheet within minutes, not days​​

No Manual Research: Eliminates hours of tedious web searching and data entry​​

🏗️ Architecture
The workflow consists of several key components:​

Chat Trigger: Initiates workflow when user submits a supplier query

Google Sheets Integration: Creates and updates spreadsheets with supplier data

Ollama LLM Chain: Processes natural language input and generates structured supplier information

Data Processing Nodes: Edits fields, splits output, and formats data for consistency

Output Management: Appends results to main sheet and removes temporary rows

🚀 Getting Started
Prerequisites
n8n instance (self-hosted or cloud)​

Ollama running locally (connected via Docker or localhost)​

Google account with Sheets API access​​

Basic understanding of n8n workflows​​

Installation
Clone or download this workflow JSON file

Import into n8n: Navigate to Workflows → Import from File​

Configure credentials:

Set up Google Sheets OAuth2 authentication​​

Connect Ollama Chat Model to your local instance​

Activate workflow: Toggle the workflow to "Active" status​

Usage
Open the workflow's chat interface​​

Type your supplier query (e.g., "paper cups", "sustainable packaging manufacturers")​

Wait for the AI to process and populate the Google Sheet​​

Access your results in the automatically created/updated spreadsheet​​

Example Input: paper cups
| Website Name      | Website URL                      | Email ID            | Contact Person | Phone Number |
| ----------------- | -------------------------------- | ------------------- | -------------- | ------------ |
| Paper Cups Inc    | https://www.paper-cups.com/      | info@paper-cups.com | Mark Davis     | 1234567890   |
| Green Earth Paper | https://www.greenearthpaper.com/ | ...                 | ...            | ...          |

🛠️ Configuration
Customizing Data Fields
Edit the Edit Fields nodes to modify output column structure:​​

Add additional fields (e.g., Country, Product Category)

Rename existing columns

Adjust data formatting rules

Adjusting AI Behavior
Modify the Basic LLM Chain node prompt to:​

Focus on specific industries or regions

Change output format or level of detail

Add filtering criteria

📊 Workflow Breakdown
Trigger: Chat message received

Sheet Creation: Generates Google Sheet with predefined headers

LLM Processing: Ollama model searches and structures supplier data

Data Transformation: JavaScript code and field editors clean and format output

Split & Insert: Divides results into individual records and appends to sheet

Cleanup: Removes temporary header rows for final polished output

🤝 Contributing
Contributions are welcome! Feel free to:​

Report bugs or issues

Suggest new features or improvements

Submit pull requests with enhancements

Share your customized versions

📝 License
This project is open source and available under the MIT License.​

💡 Use Cases
Manufacturing: Source raw materials and component suppliers​

Retail: Find product vendors and distributors​

Services: Discover B2B service providers​

Research: Compile market intelligence on supplier landscapes​

🙏 Acknowledgments
Built with:​

n8n - Workflow automation platform

Ollama - Local LLM infrastructure

Google Sheets API - Data storage and collaboration
