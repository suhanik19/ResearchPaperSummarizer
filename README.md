# Research Paper Analysis Tool

Welcome to the Research Paper Analysis Tool. This Python-based tool is designed to help users extract valuable insights from research abstracts. It helps with summarizing texts, extracting key phrases, and performing sentiment analysis. I have created this tool to help college students such as myself understand and evaluate academic papers more efficiently to save time and enhance comprehension.

## Features

The tool offers three primary functionalities:

1. **Extractive Summarization**: Generates a concise summary of an abstract by selecting the most relevant sentences based on cosine similarity. This enables quick comprehension of the key points in the abstract of a research paper.

2. **Keyword Extraction**: Identifies and extracts the top 5 key phrases from the abstract. The tool utilizes lemmatization to ensure that variations of similar terms are consolidated into their base forms, providing a clear set of essential keywords without having similar, repetitive words.

3. **Sentiment Analysis**: Analyzes the sentiment of the abstract using a sentiment analysis model from Hugging Face. This feature assesses whether the overall tone of the abstract is positive or negative.

## Methods Used
- **Cosine Similarity**:  For extractive summarization.
- **KeyBERT**: For keyword extraction.
- **Hugging Face Transformers**: For sentiment analysis.

## Technologies
- **Python**
- **Sentence Transformers**: For generating sentence embeddings.
- **KeyBERT**: For keyword extraction.
- **Transformers**: For sentiment analysis.

## Installation

To use the Research Paper Analysis Tool, click [here] (https://colab.research.google.com/drive/10MP7xPtLKRPN1ebOhNYCVVCG8gbNFc56) to open the project notebook in Google Colab.

1. Run the Code: Once the notebook is open, you can run the code cells sequentially by clicking the "Run" button at the top of each cell or by selecting Runtime > Run All from the menu.
   
2. Environment Setup: The Colab notebook is pre-configured with the necessary libraries and dependencies. When prompted, Colab will install any additional libraries automatically.

3. User Interaction: After running the code, the program will prompt you to select certain options and insert the abstract, following the directions accordingly.

## Usage

The tool provides an interactive prompt where you can select the desired analysis:

1. **Summarization**: Summarizes the abstract by picking out the most important sentences based on the number of sentences the user chooses.
2. **Keywords**: Extract the 5 most important distinct key phrases from the abstract.
3. **Sentiment Analysis**: Determines the sentiment of the abstract while providing the sentiment score to indicate the degree of positivity or negativity expressed in the text.
4. **Combined Analysis**: Performs all three of the above analyses sequentially.

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

## Future Work
While this program gets the job done, there are several areas for improvement to make this more robust and user-friendly:
* Advanced Summarization Techniques:
    * Allow users to customize their summaries (detailed vs. concise) and choose the simplicity (5th grade reading level vs. 12th grade reading level)
* Similar Research Paper Generator:
    * Gives users other research papers according to the title and abstract given by the user
    * Integrate with academic databases such as Google Scholar or PubMed

## Contact
For any issues or further inquiries, please contact Suhani Khandelwal at suhanikhnadelwal05@gmail.com. If you encounter any bugs or have suggestions, feel free to open an issue on the GitHub repository.
