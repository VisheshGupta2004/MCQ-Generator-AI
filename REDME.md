# MCQ Generator Application with LangChain

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)](https://streamlit.io/)
[![LangChain](https://img.shields.io/badge/LangChain-0.1+-green.svg)](https://python.langchain.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5--Turbo-purple.svg)](https://openai.com/)

An intelligent Multiple Choice Question (MCQ) generator application that automatically creates educational quizzes from uploaded text documents using OpenAI's GPT models and LangChain framework.

## 🚀 Features

- **📄 Multi-format Support**: Upload PDF and TXT files containing educational content
- **🤖 AI-Powered Generation**: Automatically generates MCQs using OpenAI's GPT-3.5-Turbo
- **🎯 Customizable Quizzes**: Configure number of questions (3-50), subject, and complexity level
- **✅ Quality Assurance**: Built-in evaluation system to ensure question appropriateness
- **📊 Interactive Display**: Clean table format for questions, options, and correct answers
- **💰 Cost Tracking**: Monitor OpenAI API token usage and costs
- **📝 Comprehensive Logging**: Detailed logging system for debugging and monitoring

## 🏗️ Architecture

The application follows a modular architecture with clear separation of concerns:

```
Project1/
├── StreamlitAPP.py          # Main web interface
├── src/
│   └── mcqgenerator/
│       ├── __init__.py
│       ├── MCQGenerator.py  # Core AI logic and LangChain chains
│       ├── utils.py         # File processing utilities
│       └── logger.py        # Logging configuration
├── response.json            # MCQ template structure
├── requirements.txt         # Python dependencies
└── setup.py                # Package configuration
```

## 🛠️ Technology Stack

- **Frontend**: Streamlit - Modern web interface
- **AI Framework**: LangChain - LLM orchestration
- **Language Model**: OpenAI GPT-3.5-Turbo
- **File Processing**: PyPDF2 for PDF extraction
- **Data Handling**: Pandas for table formatting
- **Environment**: Python-dotenv for configuration

## 📋 Prerequisites

- Python 3.8 or higher
- OpenAI API key
- Internet connection for API calls

## 🔧 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/mcq-generator.git
cd mcq-generator
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Environment Setup
Create a `.env` file in the root directory:
```env
OPENAI_API_KEY=your_openai_api_key_here
```

### 4. Install Package (Optional)
```bash
pip install -e .
```

## 🚀 Usage

### Running the Application
```bash
streamlit run StreamlitAPP.py
```

### Web Interface
1. **Upload Document**: Choose a PDF or TXT file containing educational content
2. **Configure Quiz**: Set the number of questions (3-50), subject, and complexity level
3. **Generate**: Click "Create MCQs" to start the AI-powered generation
4. **Review**: View the generated quiz in a formatted table
5. **Download**: Export results as needed

### Example Input
Upload a document about "Machine Learning" with:
- Number of MCQs: 5
- Subject: Computer Science
- Complexity: Simple

### Expected Output
The system generates 5 multiple-choice questions with:
- Question text
- Four options (a, b, c, d)
- Correct answer
- Quality review and complexity analysis

## 📊 Response Format

The application generates MCQs in the following JSON structure:

```json
{
    "1": {
        "mcq": "What year was machine learning coined?",
        "options": {
            "a": "1959",
            "b": "1960",
            "c": "1958",
            "d": "1961"
        },
        "correct": "a"
    }
}
```

## 🔍 How It Works

### 1. Document Processing
- **PDF Files**: Extracted using PyPDF2
- **TXT Files**: Direct text processing
- **Content Analysis**: Text is analyzed for key concepts and topics

### 2. AI Generation
- **Prompt Engineering**: Structured prompts guide GPT-3.5-Turbo
- **Question Creation**: AI generates diverse, relevant MCQs
- **Option Generation**: Four plausible answer choices per question

### 3. Quality Evaluation
- **Complexity Assessment**: AI evaluates question difficulty
- **Content Validation**: Ensures questions align with source material
- **Tone Adjustment**: Adapts complexity to specified level

### 4. Output Formatting
- **Table Generation**: Clean, readable quiz display
- **Data Validation**: Ensures proper JSON structure
- **User Experience**: Intuitive interface for educators

## 📁 Project Structure

```
├── StreamlitAPP.py          # Main Streamlit application
├── src/                     # Source code directory
│   └── mcqgenerator/       # Core package
│       ├── __init__.py     # Package initialization
│       ├── MCQGenerator.py # LangChain chains and AI logic
│       ├── utils.py        # File processing and data utilities
│       └── logger.py       # Logging configuration
├── experiment/              # Development and testing notebooks
│   └── mcq.ipynb          # Jupyter notebook for experimentation
├── logs/                    # Application logs
├── response.json            # MCQ template structure
├── data.txt                # Sample text for testing
├── requirements.txt         # Python dependencies
├── setup.py                # Package setup configuration
└── test.py                 # Basic testing script
```

## 🧪 Testing

### Basic Test
```bash
python test.py
```

### Jupyter Notebook
Open `experiment/mcq.ipynb` for interactive development and testing.

## 📝 Logging

The application maintains detailed logs in the `logs/` directory:
- Timestamp-based log files
- Detailed execution tracking
- Error logging and debugging information
- API call monitoring

## 🔑 Configuration

### Environment Variables
- `OPENAI_API_KEY`: Your OpenAI API key (required)

### Model Configuration
- **Model**: GPT-3.5-Turbo
- **Temperature**: 0.7 (balanced creativity and consistency)
- **Max Tokens**: Auto-managed by OpenAI

## 🚨 Limitations & Considerations

- **API Costs**: OpenAI API usage incurs costs based on token consumption
- **File Size**: Large documents may increase processing time and costs
- **Content Quality**: Input document quality directly affects MCQ quality
- **Language**: Currently optimized for English content

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues and enhancement requests.

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 🙏 Acknowledgments

- OpenAI for providing the GPT models
- LangChain team for the excellent framework
- Streamlit for the web interface framework
- PyPDF2 for PDF processing capabilities


