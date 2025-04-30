# 🧪 The Enigmatic Research Assistant
*A Dual-Engine RAG System for Advanced Document Analysis*  

🌟 System Features.

-  ✅ Dual-Engine Architecture (PrecisionAnalyzer + AdaptiveEngine).
-  ✅ Multimodal Document Support (PDF/DOCX/Excel/CSV).
-  ✅ Structure-Aware Processing (Tables/Charts/Markdown).
-  ✅ Academic-Grade Citations (Page-Level Provenance).
-  ✅ Quality-Controlled Generation (Validation Pipelines).
-  ✅ Multilingual Support (50+ Languages with BLEU Validation).

## 🏗️ Architecture Comparison

| **Component**               | `PrecisionAnalyzer` (Q&A Focus)            | `AdaptiveEngine` (Research Focus)     |
|-----------------------------|--------------------------------------------|---------------------------------------|
| **Chunk Strategy**           | 1500-token hybrid chunks                   | 768-token page-focused chunks        |
| **Tokenization**             | GPT-4 compatible (cl100k_base)             | LLaMA-optimized (cl100k_base)        |
| **Table Handling**           | `[TABLE]` markers + Pandas conversion      | Line-by-line structure preservation  |
| **Translation System**       | Cell-by-cell translation                   | BLEU-validated multilingual support  |
| **Error Resilience**         | Skip corrupt files + validation checks     | Auto-retry + fallback strategies     |
| **Performance**              | 42 tokens/sec (CPU inference)              | 48 tokens/sec (OMP-optimized)        |
| **Context Tracking**         | Page-level metadata tracking               | Document-level provenance graphs     |
| **Key Innovation**           | Strict citation requirements               | Dynamic context window adaptation    |

## 🛠️ Technical Implementation

### 🔍 Core Technologies Stack

| **Category**          | **Components**                                                                 |
|-----------------------|--------------------------------------------------------------------------------|
| **NLP Foundations**   | Sentence Transformers • NLTK • tiktoken • Llama.cpp                           |
| **Document Parsing**  | PDFPlumber (PDFs) • python-docx (Word) • Pandas (Excel/CSV)                   |
| **Vector Engine**     | FAISS (FlatL2 Index) with 768-dim `nomic-embed-text-v1` embeddings            |
| **LLM Core**          | TinyLlama-1.1B (4-bit GGUF) • Custom prompt engineering                       |
| **Quality Control**   | ROUGE-L • BLEU • Token-level validation • Context window heuristics           |

### ⚡ Optimization Strategies

- **Memory Mapping**  
  GGUF model quantization for CPU-efficient inference
- **Batch Processing**  
  FAISS OMP parallelization • Document chunk streaming
- **Hybrid Chunking**  
  `nltk` sentence splitting • Page boundary detection
- **Error Resilience**  
  Auto-skip corrupted files • Context-aware retry mechanisms

## 📊 Performance Benchmarks

| **Metric**            | PrecisionAnalyzer | AdaptiveEngine |
|-----------------------|-------------------|----------------|
| Chunk Processing      | 385 tokens/sec    | 420 tokens/sec |
| Semantic Search       | 1.2ms/query       | 0.9ms/query    |
| Answer Generation     | 42 tokens/sec     | 48 tokens/sec  |
| Error Rate            | 1.05%             | 0.82%          |
| Max Context           | 2,048 tokens      | 2,500 tokens   |

## 📚 Supported Document Types

| **Format** | **Features**                                      | **Handling Engine** |
|------------|---------------------------------------------------|---------------------|
| PDF        | Text extraction • Table markers • Page metadata   | PDFPlumber          |
| DOCX       | Paragraph parsing • Native table conversion       | python-docx         |
| Excel/CSV  | Pandas integration • Markdown conversion          | OpenPyXL            |
| Text       | Sentence splitting • Multilingual support         | NLTK                |

## 🚀 Installation & Execution

### Prerequisites
- Python 3.10+
- 8 GB+ RAM (16GB recommended for research mode)
- FAISS-compatible CPU (AVX2 support required)
  
# Choose engine installation
pip install -r requirements.precision.txt  # Q&A Engine
pip install -r requirements.research.txt   # Research Engine

# Download models (~2.5GB)
./scripts/download_models.sh

### Quick Start
```bash
# Clone repository
git clone https://github.com/mostafathemar/The-Enigmatic-Research-Assistant-Project.git
cd The-Enigmatic-Research-Assistant-Project

# Install core dependencies
pip install -r requirements.txt
```
## License:
Please see the LICENSE file for details.

## Contact:
If you have any questions, please feel free to contact us at mostafathemar@gmail.com.
