**Resume Ranking with BERT-based NLP**

This project leverages advanced Natural Language Processing (NLP) techniques, particularly BERT (Bidirectional Encoder Representations from Transformers), to rank resumes based on their relevance to specific job categories. The objective is to streamline the recruitment process by automatically evaluating resumes against job descriptions and identifying the most suitable candidates.

**Key Components:**

1. **Data Preprocessing:**
   - The dataset comprises resumes categorized into various job roles.
   - Resumes are preprocessed to remove noise, including HTML tags, special characters, digits, and non-ASCII characters, and are converted to lowercase.

2. **BERT-Based Model:**
   - A custom PyTorch dataset is defined for efficient data loading and processing.
   - A DistilBERT model is utilized for generating embeddings (numerical representations) of resume text.
   - Resumes are tokenized using the DistilBERT tokenizer and converted into embeddings.
   - These embeddings capture semantic information about the resumes, enabling meaningful comparisons.

3. **Ranking Resumes:**
   - Resumes are ranked based on their similarity to predefined job categories.
   - For each job category, the average embedding of resumes in that category is computed.
   - Cosine similarity is used to measure the similarity between individual resumes and the category's average embedding.
   - Top 10 resumes with the highest similarity scores are selected for each category.

4. **Model Validation:**
   - The ranking model's performance is evaluated using metrics such as accuracy, precision, recall, and cross-validation scores.
   - SVM (Support Vector Machine) classifier is employed for validation, ensuring the robustness of the ranking approach.

5. **Overall Architecture:**
   - The architecture follows a modular design, allowing for easy integration of additional features or improvements.
   - It comprises data preprocessing, model training, evaluation, and ranking components.
