# ⚡ N8N Workflow Collection & Documentation

A professionally organized collection of **2,053 n8n workflows** with a lightning-fast documentation system that provides instant search, analysis, and browsing capabilities.

## 🚀 **NEW: High-Performance Documentation System**

**Experience 100x performance improvement over traditional documentation!**

### Quick Start - Fast Documentation System

```bash
# Install dependencies
pip install -r requirements.txt

# Start the fast API server
python run.py

# Open in browser
http://localhost:8000
```

**Features:**

* ⚡ **Sub-100ms response times** with SQLite FTS5 search
* 🔍 **Instant full-text search** with advanced filtering
* 📱 **Responsive design** - works perfectly on mobile
* 🌙 **Dark/light themes** with system preference detection
* 📊 **Live statistics** - 365 unique integrations, 29,445 total nodes
* 🎯 **Smart categorization** by trigger type and complexity
* 🎯 **Use case categorization** by service name mapped to categories
* 📄 **On-demand JSON viewing** and download
* 🔗 **Mermaid diagram generation** for workflow visualization
* 🔄 **Real-time workflow naming** with intelligent formatting

---

## 📂 Repository Organization

### Workflow Collection

* **2,053 workflows** with meaningful, searchable names
* **365 unique integrations** across popular platforms
* **29,445 total nodes** with professional categorization
* **Quality assurance** - All workflows analyzed and categorized

### Advanced Naming System ✨

Our intelligent naming system converts technical filenames into readable titles:

* **Before**: `2051_Telegram_Webhook_Automation_Webhook.json`
* **After**: `Telegram Webhook Automation`
* **100% meaningful names** with smart capitalization
* **Automatic integration detection** from node analysis

### Use Case Category ✨

The search interface includes a dropdown filter that lets you browse 2,000+ workflows by category.

The system includes an automated categorization feature that organizes workflows by service categories to make them easier to discover and filter.

### How Categorization Works

1. **Run the categorization script**

   ```
   python create_categories.py
   ```

2. **Service Name Recognition**
   The script analyzes each workflow JSON filename to identify recognized service names (e.g., "Twilio", "Slack", "Gmail", etc.)

3. **Category Mapping**
   Each recognized service name is matched to its corresponding category using the definitions in `context/def_categories.json`. For example:

   * Twilio → Communication & Messaging
   * Gmail → Communication & Messaging
   * Airtable → Data Processing & Analysis
   * Salesforce → CRM & Sales

4. **Search Categories Generation**
   The script produces a `search_categories.json` file that contains the categorized workflow data

5. **Filter Interface**
   Users can then filter workflows by category in the search interface, making it easier to find workflows for specific use cases

### Available Categories

The categorization system includes the following main categories:

* AI Agent Development
* Business Process Automation
* Cloud Storage & File Management
* Communication & Messaging
* Creative Content & Video Automation
* Creative Design Automation
* CRM & Sales
* Data Processing & Analysis
* E-commerce & Retail
* Financial & Accounting
* Marketing & Advertising Automation
* Project Management
* Social Media Management
* Technical Infrastructure & DevOps
* Web Scraping & Data Extraction

---

## 🛠 Usage Instructions

### Option 1: Modern Fast System (Recommended)

```bash
# Clone repository
git clone <repo-url>
cd n8n-workflows

# Install Python dependencies
pip install -r requirements.txt

# Start the documentation server
python run.py

# Browse workflows at http://localhost:8000
```

### Option 2: Development Mode

```bash
# Start with auto-reload for development
python run.py --dev

# Or specify custom host/port
python run.py --host 0.0.0.0 --port 3000

# Force database reindexing
python run.py --reindex
```

### Import Workflows into n8n

```bash
# Use the Python importer (recommended)
python import_workflows.py

# Or manually import individual workflows via the n8n UI
```

---

## 📊 Workflow Statistics

### Current Collection Stats

* **Total Workflows**: 2,053
* **Active Workflows**: 215
* **Total Nodes**: 29,445
* **Unique Integrations**: 365
* **Database**: SQLite with FTS5 full-text search

### Trigger Distribution

* **Complex**: 831 workflows
* **Webhook**: 519 workflows
* **Manual**: 477 workflows
* **Scheduled**: 226 workflows

### Complexity Analysis

* **Low (≤5 nodes)**: \~35%
* **Medium (6-15 nodes)**: \~45%
* **High (16+ nodes)**: \~20%

### Popular Integrations

* **Communication**: Telegram, Discord, Slack, WhatsApp
* **Cloud Storage**: Google Drive, Google Sheets, Dropbox
* **Databases**: PostgreSQL, MySQL, MongoDB, Airtable
* **AI/ML**: OpenAI, Anthropic, Hugging Face
* **Development**: HTTP Request, Webhook, GraphQL

---

## 🔍 Advanced Search Features

### Smart Search Categories

Available Categories:

* **messaging**
* **ai\_ml**
* **database**
* **email**
* **cloud\_storage**
* **project\_management**
* **social\_media**
* **ecommerce**
* **analytics**
* **calendar\_tasks**
* **forms**
* **development**

### API Usage Examples

```bash
curl "http://localhost:8000/api/workflows?q=telegram+automation"
curl "http://localhost:8000/api/workflows?trigger=Webhook&complexity=high"
curl "http://localhost:8000/api/workflows/category/messaging"
curl "http://localhost:8000/api/stats"
curl "http://localhost:8000/api/categories"
```

---

## 🏗 Technical Architecture

* **SQLite Database**
* **FastAPI Backend**
* **Responsive Frontend**
* **Automatic Categorization and Naming**
* **Change Detection**
* **Compressed Responses**
* **Mobile Optimization**

---

## 🔧 Setup & Requirements

* Python 3.7+
* Modern Browser
* 50MB Storage
* n8n Instance

---

## 📋 Naming Convention

Filenames are automatically transformed:

```
2051_Telegram_Webhook_Automation_Webhook.json → Telegram Webhook Automation
```

---

## 🚀 API Documentation

### Endpoints

* `/` - Browser interface
* `/api/stats`
* `/api/workflows`
* `/api/workflows/{filename}`
* `/api/workflows/{filename}/download`
* `/api/workflows/{filename}/diagram`
* `/api/workflows/category/{category}`
* `/api/categories`
* `/api/integrations`
* `/api/reindex`

---

## 🤝 Contributing

1. Export and clean workflow JSON
2. Place in `workflows/`
3. Run reindexing

---

## ⚠️ Notes

* Replace credentials
* Test in dev
* May require community nodes

---

## 📚 Resources

* [n8n Docs](https://docs.n8n.io/)
* [n8n Community](https://community.n8n.io/)
* [Templates](https://n8n.io/workflows/)

---

**🎯 Perfect for**: Developers, automation engineers, business analysts, and anyone looking to streamline their workflows with proven n8n automations.
