# Research Paper Analysis Tool

Welcome to the Research Paper Analysis Tool. This Python-based tool is designed to assist users in extracting valuable insights from research abstracts. It provides functionalities for summarizing texts, extracting key phrases, and performing sentiment analysis, streamlining the process of understanding and evaluating academic papers.

## Features

The tool offers three primary capabilities:

1. **Extractive Summarization**: Generates a concise summary of an abstract by selecting the most relevant sentences based on cosine similarity. This enables quick comprehension of the key points in the abstract of a research paper.

2. **Keyword Extraction**: Identifies and extracts the top 5 key phrases from the abstract. The tool utilizes lemmatization to ensure that variations of similar terms are consolidated into their base forms, providing a clear set of essential keywords without having similar, repetitive words.

3. **Sentiment Analysis**: Analyzes the sentiment of the abstract using a sentiment analysis model from Hugging Face. This feature assesses whether the overall tone of the abstract is positive or negative.

## Methods Used
- **Cosine Similarity**:  For extractive summarization.
- **KeyBERT**: For keyword extraction.
- **Hugging Face Transformers**: For sentiment analysis.

## Technologies
- **Python**: Programming language used.
- **Sentence Transformers**: For generating sentence embeddings.
- **KeyBERT**: For keyword extraction.
- **Transformers**: For sentiment analysis.

## Installation

To use the Research Paper Analysis Tool, you need to install the required Python packages. Execute the following commands in your terminal:

```bash
pip install -U sentence-transformers keybert transformers
```

## Usage

After installation, you can interact with the tool via the command line. The tool provides an interactive prompt where you can select the desired analysis:

1. **Summarization**: Creates a summary of the abstract by selecting the most significant sentences.
2. **Keywords**: Extracts and normalizes the 5 most important key phrases from the abstract.
3. **Sentiment Analysis**: Determines the sentiment of the abstract while providing the sentiment score to indicate the degree of positivity or negativity expressed in the text.
4. **Combined Analysis**: Performs all three analyses sequentially.

The tool is built using Python and relies on libraries like sentence-transformers, keybert, and transformers. The core functionalities are implemented in Python scripts, and users can interact with the tool via the command line.

## Example Usage

The following example demonstrates how to use the tool:

```bash
# Example of usage
question = input("Choose between the following: \n1. Summarizer \n2. Keywords \n3. Sentiment Analysis \n4. All \n")
abstract = input("Enter abstract here: ")
```

## Sample Output
```bash
Choose between the following: 
1. Summarizer 
2. Keywords 
3. Sentiment Analysis 
4. All 
4
Enter abstract here: The increasing complexity of climate systems presents a significant challenge in accurately predicting future environmental conditions. This study explores the application of deep neural networks (DNNs) to enhance climate prediction models under conditions of high uncertainty. Leveraging historical climate data and advanced machine learning algorithms, we constructed a multi-layered neural network capable of learning non-linear dependencies between atmospheric variables. The model was trained on both regional and global climate datasets, incorporating variables such as temperature, humidity, and greenhouse gas concentrations. Results indicate that the proposed DNN model outperforms traditional statistical methods, particularly in scenarios with incomplete or noisy data. The model's predictive accuracy was validated using cross-validation techniques, with performance metrics showing an improvement of 15% over standard regression-based approaches. However, the black-box nature of neural networks poses interpretability challenges, which are addressed through post-hoc explainability methods, such as SHAP (Shapley Additive Explanations). Future work will focus on integrating real-time satellite data and improving computational efficiency to support more dynamic climate forecasts. This study contributes to the growing body of research seeking to harness artificial intelligence for environmental sustainability and resilience.
Number of sentences you want in the summary: 3

Summary:
This study explores the application of deep neural networks (DNNs) to enhance climate prediction models under conditions of high uncertainty.
Leveraging historical climate data and advanced machine learning algorithms, we constructed a multi-layered neural network capable of learning non-linear dependencies between atmospheric variables.
The increasing complexity of climate systems presents a significant challenge in accurately predicting future environmental conditions.

Unique Keywords:
['climate', 'predict', 'model', 'neural', 'dnn']

Sentiment Analysis Result:
[{'label': 'POSITIVE', 'score': 0.99456787109375}]
```

## Getting Started

To run the Research Paper Analysis Tool:

1. **Clone the Repository**

```bash
git clone https://github.com/yourusername/research-paper-analysis-tool.git
cd research-paper-analysis-tool
```

2. **Install Dependencies**

```bash
pip install -U sentence-transformers keybert transformers
```

3. **Run the Tool**

    Execute the main script and follow the prompts:

```bash
python main.py
```

## Contact
For any issues or further inquiries, please contact Suhani Khandelwal at suhanikhnadelwal05@gmail.com. If you encounter any bugs or have suggestions, feel free to open an issue on the GitHub repository.
