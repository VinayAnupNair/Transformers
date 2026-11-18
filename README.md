# CS 4372 - NLP Using Transformers

Vinay Nair  
NetID: van220003

## GitHub Repository

https://github.com/VinayAnupNair/Transformers

## Dataset

[Alice's Adventures in Wonderland – Standard Ebooks](https://github.com/standardebooks/lewis-carroll_alices-adventures-in-wonderland_john-tenniel/archive/refs/heads/master.zip)

The dataset contains the book *Alice's Adventures in Wonderland* by Lewis Carroll. I obtained the book from Standard Ebooks because Project Gutenberg was unavailable at the time.

The book contains 12 chapters, which were extracted from XHTML files and converted into plain text. The text was then split into 151 passages of approximately 200 words each.

Five passages from different chapters were selected for evaluating the Transformer models.

## Requirements

- Python 3
- torch
- transformers
- pandas
- numpy
- requests
- beautifulsoup4
- nltk
- scikit-learn
- evaluate
- rouge_score
- sacrebleu
- sentencepiece
- sacremoses
- bottleneck

## Running the Code

1. Open the submitted `.ipynb` file in Google Colab or Jupyter Notebook.
2. Install the required packages if they are not already installed. In a notebook cell, run:

   ```python
   %pip install torch transformers pandas numpy requests beautifulsoup4 nltk scikit-learn evaluate rouge_score sacrebleu sentencepiece sacremoses bottleneck
   ```

3. Run all notebook cells from top to bottom.
4. The book will be downloaded from the Standard Ebooks GitHub repository. An internet connection is required.
5. The notebook extracts the chapter text, divides it into passages, loads the pretrained Transformer models, and performs the four NLP tasks.
6. The notebook evaluates each model using the appropriate evaluation metrics and displays the final results.

## Models

- **Text Summarization:** Google FLAN-T5-Large (Encoder-Decoder Transformer)
- **Machine Translation:** Helsinki-NLP OPUS-MT English-to-French (Encoder-Decoder Transformer)
- **Question Answering:** DistilBERT pretrained on SQuAD (Encoder-Only Transformer)
- **Text Generation:** DistilGPT2 (Decoder-Only Transformer)

## Experiments

- **Task 1:** Generate summaries using FLAN-T5-Large and evaluate them using ROUGE scores.
- **Task 2:** Translate English passages into French using Helsinki-NLP OPUS-MT and evaluate them using BLEU and chrF scores.
- **Task 3:** Develop a question-answering system using TF-IDF retrieval and DistilBERT, evaluated using Exact Match and F1 Score.
- **Task 4:** Generate text from seed passages using DistilGPT2 and evaluate language-model perplexity.

## Notes

- The dataset is downloaded from a public GitHub repository rather than included with the submission.
- All four tasks use pretrained Transformer models without additional training or fine-tuning.
- Five passages were selected for summarization, translation, and text-generation evaluation.
- The question-answering system was evaluated using five questions.
- Reference summaries were manually prepared, while French reference translations were obtained using Google Translate.
- Text generation was tested using different seed lengths and generation parameters.
- Perplexity was calculated on the original book text rather than the generated continuations.
- The pretrained models are downloaded from Hugging Face when first loaded, so an internet connection is required.
- Running the models may require significant memory and computational resources. A GPU is recommended for faster execution.
