# AI-Powered Document Processing Backend

A Flask-based backend service providing AI-powered document processing and analysis capabilities.

## System Architecture
- **Framework**: Flask with CORS support
- **Database**: SQLite (invoices.db)
- **Storage**: Azure Blob Storage integration
- **Task Processing**: Asynchronous task processing system

## Detailed Backend Architecture

### High-Level Architecture
```mermaid
graph TB
    Client[Client Applications] --> API[Flask API Layer]
    API --> Auth[Authentication]
    API --> DocProc[Document Processing]
    API --> AI[AI Services]
    API --> Storage[Storage Services]
    
    DocProc --> AzureBlob[Azure Blob Storage]
    DocProc --> LocalFS[Local File System]
    DocProc --> SQLite[(SQLite DB)]
    
    AI --> NLP[NLP Processing]
    AI --> OCR[OCR Service]
    AI --> VectorDB[Vector Database]
    
    Storage --> AzureBlob
    Storage --> LocalFS
    Storage --> SQLite
```

### Document Processing Flow
```mermaid
sequenceDiagram
    participant Client
    participant API
    participant DocProc
    participant AzureBlob
    participant VectorDB
    participant AI

    Client->>API: Upload Document
    API->>DocProc: Process Document
    DocProc->>AzureBlob: Store Original
    DocProc->>DocProc: Extract Text
    DocProc->>VectorDB: Store Embeddings
    DocProc->>AI: Process Content
    AI-->>API: Return Results
    API-->>Client: Response
```

### Component Interaction
```mermaid
graph LR
    subgraph Frontend
        Client[Client Apps]
    end

    subgraph Backend
        API[Flask API]
        Auth[Auth Service]
        DocProc[Document Processor]
        AI[AI Services]
    end

    subgraph Storage
        AzureBlob[Azure Blob]
        LocalFS[Local Storage]
        SQLite[(SQLite DB)]
        VectorDB[Vector Store]
    end

    Client --> API
    API --> Auth
    API --> DocProc
    API --> AI
    
    DocProc --> AzureBlob
    DocProc --> LocalFS
    DocProc --> SQLite
    DocProc --> VectorDB
    
    AI --> VectorDB
    AI --> AzureBlob
```

### Data Flow Architecture
```mermaid
flowchart TD
    A[Client Request] --> B{Request Type}
    B -->|Document Upload| C[File Processing]
    B -->|Query| D[AI Processing]
    B -->|Email| E[Email Processing]
    
    C --> F[Azure Blob Storage]
    C --> G[Local Storage]
    C --> H[Vector Database]
    
    D --> I[NLP Processing]
    D --> J[Document Retrieval]
    D --> K[Response Generation]
    
    E --> L[Email Extraction]
    E --> M[Content Processing]
    
    F --> N[Response]
    G --> N
    H --> N
    I --> N
    J --> N
    K --> N
    L --> N
    M --> N
```

## Core Components

### 1. Document Processing
- **File Upload & Processing**
  - Supports PDF, text, and image files
  - Azure Blob Storage integration for file management
  - Document chunking and vectorization

### 2. API Endpoints

#### Document Management
- `POST /processfiles` - Process uploaded documents
- `POST /process_bulk_files` - Handle bulk file processing
- `GET /task_status/<task_id>` - Check async processing status

#### Document Analysis
- `POST /ask` - Query documents with natural language
- `POST /summarize` - Generate document summaries
- `POST /extractTables` - Extract tables from documents

#### Email Processing
- `POST /extractOutlookEmails` - Extract and process Outlook emails

#### OCR & Notes Processing
- `POST /processHWNotesWithOCR` - Process handwritten notes using OCR
- `POST /processHWNotes` - Process handwritten notes and extract study materials

#### Utility Endpoints
- `GET /alive` - Health check endpoint
- `GET /getfilenames` - List available files

## Key Features

### 1. Document Processing Pipeline
- Document loading and chunking
- Text extraction from various formats
- Vector storage for semantic search

### 2. AI Capabilities
- Natural language querying
- Document summarization
- Table extraction
- OCR processing
- Meeting analysis

### 3. Data Management
- Azure Blob Storage integration
- Local file system management
- Database storage for metadata

## Setup and Installation

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Configure environment variables:
- Azure Blob Storage credentials
- Database configuration
- Other service-specific settings

3. Run the server:
```bash
python server.py
```

## Docker Deployment

Build and run using Docker Compose:
```bash
docker-compose up --build
```

## Project Structure
```
flask-server/
├── server.py                 # Main application file
├── DataIngest.py            # Data ingestion utilities
├── TextFromImage.py         # OCR processing
├── RetrievalData.py         # Document retrieval
├── outlookEmails.py         # Email processing
├── tasks.py                 # Async task processing
├── azBlobUtil.py           # Azure Blob Storage utilities
└── requirements.txt         # Project dependencies
```

## Security Features
- Input validation
- Secure file handling
- Error handling and logging
- User email validation

## Error Handling
- Comprehensive error handling system
- Logging for debugging
- User-friendly error messages
