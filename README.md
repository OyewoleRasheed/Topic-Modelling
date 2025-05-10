# 📝 Topic Modeling with LDA + Interactive Visualization

This project performs **Topic Modeling** on text data using **Latent Dirichlet Allocation (LDA)** and visualizes the topics interactively using **pyLDAvis**.

It also maps numeric topics into **human-readable labels** based on the top keywords for each topic.

---

## 🚀 Features

* Vectorizes text data using **CountVectorizer**
* Fits an **LDA model** to discover hidden topics
* Displays **top keywords** per topic
* Maps each document to a **meaningful topic label**
* Visualizes topics with interactive, browser-based visualization using **pyLDAvis**

---

## 📦 Requirements

Install the required packages:

```bash
pip install pandas scikit-learn pyLDAvis matplotlib
```

> ✅ Compatible with `pyLDAvis` version 3.4.0 and later.

---

## 📊 How It Works

1. **Load Data**

   * Reads text articles or documents from your dataset.

2. **Text Vectorization**

   * Uses `CountVectorizer` (not TF-IDF) to create a document-term matrix for LDA.

3. **LDA Topic Modeling**

   * Uses `sklearn`'s `LatentDirichletAllocation` to discover latent topics.
   * Fits the model and extracts **top 10 keywords** for each topic.

4. **Assign Topic Names**

   * Maps numeric topic IDs (e.g., 0, 1, 2) to **readable names** like "Machine Learning", "Clustering", etc.

5. **Interactive Visualization**

   * Visualizes topics using **pyLDAvis** with circles representing topics and bar charts showing top terms.
   * Allows interactive exploration in a browser or notebook.

---

## 🔥 Example Topics

```
Topic 0 (Machine Learning):
  learning, machine, algorithms, deep, books, best, algorithm, use, applications, introduce

Topic 1 (Python / Data):
  python, data, learning, using, learn, machine, want, news, language, stock

Topic 2 (Insurance / Sentiment):
  insurance, people, want, learn, using, python, analysis, task, sentiment, analyze

Topic 3 (Clustering):
  clustering, machine, learning, algorithm, using, classification, python, algorithms, implementation, clusters

Topic 4 (Naive Bayes / Classification):
  algorithm, bayes, learning, naive, based, clustering, machine, classification, introduction, similar
```

---

## 📂 Example Output (Document Labels)

| Article                                      | Topic Name                   |
| -------------------------------------------- | ---------------------------- |
| "Data analysis is the process of inspecting" | Machine Learning             |
| "Multinomial Naive Bayes algorithm..."       | Naive Bayes / Classification |
| "News categorized into politics and sports"  | Python / Data                |

---

## 🌐 Visualization

* **Circles**: Each topic is a circle sized by prevalence.
* **Distance**: Circles further apart mean more distinct topics.
* **Hover**: See top keywords per topic interactively.



> ✅ Works both in **Jupyter Notebooks** and in **browsers**.


## ✅ Best Practices Used

* ✔️ Uses `CountVectorizer` (not TF-IDF) — ideal for count-based LDA
* ✔️ Uses robust `pyLDAvis.prepare()` (avoids version/module errors)
* ✔️ Maps numeric topic IDs to human-readable names
* ✔️ Assigns topics back to each document (`topic_name` column)

---

## 🙋 Author

Created by \[Oyewole Rasheed]
Feel free to connect for improvements or collaborations!

---

## 📚 References

* Original tutorial inspiration:
  [Topic Modelling using Python — The Clever Programmer (2023)](https://thecleverprogrammer.com/2023/02/13/topic-modelling-using-python/)
