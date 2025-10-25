# Job Description Analysis

A comprehensive machine learning and AI pipeline for analyzing job descriptions using traditional NLP techniques and modern Generative AI approaches. This project extracts structured information from job advertisements and provides intelligent matching capabilities.

## 🎯 Project Overview

This repository contains a hybrid pipeline that combines traditional NLP methods with Generative AI to extract and analyze structured information from job descriptions. The system can:

- Extract skills, responsibilities, and requirements from job descriptions
- Perform intelligent matching between job descriptions and candidate profiles
- Provide measurement and evaluation using BERTScore and ROUGE metrics
- Support RAG (Retrieval-Augmented Generation) workflows for document analysis

## 📁 Repository Structure

```
job-description-analysis/
├── 01-data-import.ipynb              # Data import and basic exploration
├── 02-data-preprocessing.ipynb       # Data cleaning and preprocessing
├── 03-langgraph-job-description.ipynb # LangGraph pipeline with LangFuse integration
├── 04-measurement.ipynb              # Evaluation using BERTScore and ROUGE
├── 05-langgrph-agentic-rag-client-help.ipynb # RAG agent for document analysis
├── job-description-data/              # Dataset files
│   ├── ads-50k.csv                   # Main dataset
│   ├── ads-50k.json                  # JSON format dataset
│   └── sample_df.csv                 # Sample data for testing
├── chroma_db/                        # ChromaDB vector database
├── client-help-logs/                 # Client interaction logs
├── job-description-logs/             # Processing logs
├── instructions/                     # Project documentation
├── reference/                        # Reference implementations
└── requirements.txt                  # Python dependencies
```

## 🚀 Features

### 1. Data Processing Pipeline
- **Data Import**: Load and explore job description datasets
- **Preprocessing**: Clean HTML content, extract text, and prepare data for analysis
- **Feature Engineering**: Extract structured information from unstructured text

### 2. AI-Powered Analysis
- **LangGraph Integration**: Advanced workflow orchestration with LangGraph
- **LangFuse Integration**: Comprehensive tracing and monitoring
- **RAG Capabilities**: Retrieval-augmented generation for document analysis
- **Vector Database**: ChromaDB for efficient similarity search

### 3. Evaluation and Measurement
- **BERTScore**: Semantic similarity evaluation
- **ROUGE Metrics**: Text overlap and quality assessment
- **Cosine Similarity**: Content similarity analysis
- **Performance Logging**: Detailed tracking of model performance

### 4. Intelligent Matching
- **Job-Candidate Matching**: AI-powered compatibility assessment
- **Skills Extraction**: Automated identification of required skills
- **Requirements Analysis**: Structured extraction of job requirements
- **Classification**: Job categorization and metadata extraction

## 🛠️ Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd job-description-analysis
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**:
   Create a `.env` file with your API keys:
   ```
   OPENAI_API_KEY=your_openai_api_key
   LANGFUSE_PUBLIC_KEY=your_langfuse_public_key
   LANGFUSE_SECRET_KEY=your_langfuse_secret_key
   LANGFUSE_HOST=your_langfuse_host
   ```

## 📊 Usage

### 1. Data Import and Preprocessing
```python
# Run the data import notebook
jupyter notebook 01-data-import.ipynb

# Process and clean the data
jupyter notebook 02-data-preprocessing.ipynb
```

### 2. LangGraph Pipeline
```python
# Execute the main analysis pipeline
jupyter notebook 03-langgraph-job-description.ipynb
```

### 3. Evaluation
```python
# Run performance measurements
jupyter notebook 04-measurement.ipynb
```

### 4. RAG Agent
```python
# Use the intelligent document analysis agent
jupyter notebook 05-langgrph-agentic-rag-client-help.ipynb
```

## 🔧 Key Technologies

- **LangChain**: Framework for LLM applications
- **LangGraph**: Workflow orchestration
- **LangFuse**: LLM observability and tracing
- **ChromaDB**: Vector database for embeddings
- **OpenAI**: GPT models for text analysis
- **BERTScore**: Semantic similarity evaluation
- **ROUGE**: Text quality metrics
- **Pandas**: Data manipulation
- **Scikit-learn**: Machine learning utilities

## 📈 Performance Metrics

The system provides comprehensive evaluation using:
- **BERTScore**: Measures semantic similarity between generated and reference text
- **ROUGE-1, ROUGE-2, ROUGE-L**: Measures n-gram overlap and longest common subsequence
- **Cosine Similarity**: Content similarity analysis
- **Custom Metrics**: Domain-specific evaluation criteria

## 📝 Data Format

The system processes job descriptions in JSON format with the following structure:
```json
{
  "id": "unique_identifier",
  "title": "Job Title",
  "abstract": "Job Summary",
  "content": "Full Job Description",
  "metadata": {
    "classification": "Job Category",
    "location": "Job Location",
    "workType": "Employment Type"
  }
}
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Support

For questions or support, please open an issue in the repository or contact the development team.

## 🔮 Future Enhancements

- [ ] Multi-language support
- [ ] Advanced skill matching algorithms
- [ ] Real-time job recommendation system
- [ ] Integration with job boards and ATS systems
- [ ] Enhanced visualization and reporting capabilities