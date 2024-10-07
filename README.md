# Constitution of Nepal Dataset

Welcome to the **Constitution of Nepal** dataset repository! This project provides a structured and well-organized dataset of the Constitution of Nepal, making it accessible for contributions, analysis, and applications like **NLP tasks**. We aim to foster a better understanding of Nepal's Constitution, making it easier to research and analyze legal and constitutional data.

The original document can be found in the repository as [Constitution_of_Nepal_2072_ENG.pdf](Constitution_of_Nepal_2072_ENG.pdf).

This repository is maintained by the **KEC Computer Club**. To learn more about the club, visit [computerclubkec.github.io](https://computerclubkec.github.io).

---

## 📁 Repository Structure

The Constitution is divided into smaller, manageable articles for easy contributions. The dataset follows a hierarchical JSON format, designed for clarity and easy navigation.

Here’s the updated file structure:

```
├── index.json                          (Main index of the constitution)
├── articles/                           (Directory containing individual parts)
    ├── part1/                          (Directory for Part 1)
        ├── article1.json               (Contains Part 1, Article 1)
        ├── article2.json               (Contains Part 1, Article 2)
    ├── part2/                          (Directory for Part 2)
        ├── article10.json              (Contains Part 2, Article 10)
        ├── article11.json              (Contains Part 2, Article 11)
    ├── ...                             (Additional parts and articles)
    ├── preamble.json                   (Contains the Preamble)
├── Constitution_of_Nepal_2072_ENG.pdf  (Original PDF document of the Constitution)
```

### **Main Files**

- **`index.json`**: This file serves as an overview of the entire Constitution. It references all parts and articles, with paths to their respective JSON files.
- **`articles/`**: This directory contains subdirectories for each part of the Constitution, with JSON files for each article inside their respective part directories.
- **`Constitution_of_Nepal_2072_ENG.pdf`**: The original PDF document of the Constitution of Nepal for reference.

### **Example of `index.json`:**
```json
{
  "title": "Constitution of Nepal",
  "preamble": {
    "content": "We, the Sovereign People of Nepal...",
    "file": "articles/preamble.json"
  },
  "parts": [
    {
      "part_number": 1,
      "title": "Preliminary",
      "articles": [
        {
          "article_number": 1,
          "title": "Constitution as the fundamental law",
          "file": "articles/part1/article1.json"
        },
        {
          "article_number": 2,
          "title": "Sovereignty and state authority",
          "file": "articles/part1/article2.json"
        }
      ]
    },
    {
      "part_number": 2,
      "title": "Citizenship",
      "articles": [
        {
          "article_number": 10,
          "title": "Not to deprive of citizenship",
          "file": "articles/part2/article10.json"
        },
        {
          "article_number": 11,
          "title": "To be citizens of Nepal",
          "file": "articles/part2/article11.json"
        }
      ]
    }
  ]
}
```

### **Example of Individual Article File (`articles/part1/article1.json`):**
For a simple article with multiple clauses:
```json
{
  "article_number": 1,
  "title": "Constitution as the fundamental law",
  "content": [
    {
      "type": "clause",
      "clause_number": 1,
      "text": "This Constitution is the fundamental law of Nepal. Any law inconsistent with this Constitution shall, to the extent of such inconsistency, be void."
    },
    {
      "type": "clause",
      "clause_number": 2,
      "text": "It shall be the duty of every person to observe this Constitution."
    }
  ],
  "part_number": 1
}
```

### Nested Bullet Points Example:
For articles or clauses with nested bullet points:
```json
{
  "article_number": 2,
  "title": "Sovereignty and state authority",
  "content": [
    {
      "type": "clause",
      "clause_number": 1,
      "text": "The sovereignty and state authority of Nepal shall be vested in the Nepalese people.",
      "subclauses": [
        {
          "type": "subclause",
          "text": "It shall be exercised in accordance with the provisions set forth in this Constitution.",
          "subpoints": [
            {
              "type": "bullet",
              "text": "Further clarification bullet point."
            }
          ]
        }
      ]
    },
    {
      "type": "clause",
      "clause_number": 2,
      "text": "The territory of Nepal shall comprise:",
      "subclauses": [
        {
          "type": "subclause",
          "text": "the territory existing at the time of commencement of this Constitution."
        },
        {
          "type": "subclause",
          "text": "such other territory as may be acquired after the commencement of this Constitution."
        }
      ]
    }
  ],
  "part_number": 1
}
```

### Simple Paragraph Example:
For an article that consists of a single paragraph without multiple clauses or bullets:
```json
{
  "article_number": 3,
  "title": "Nation",
  "content": [
    {
      "type": "paragraph",
      "text": "All the Nepalese people, with multiethnic, multilingual, multi-religious, multicultural characteristics and in geographical diversities, and having common aspirations and being united by a bond of allegiance to national independence, territorial integrity, national interest and prosperity of Nepal, collectively constitute the nation."
    }
  ],
  "part_number": 1
}
```

---

## 🛠️ How to Contribute

We welcome contributions from everyone! To make the process as smooth as possible, follow these steps:

1. **Fork the Repository**: Click the "Fork" button to create a copy of the repository on your GitHub account.

2. **Clone the Repository**: Clone your forked repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/constitution-of-nepal-dataset.git
   ```

3. **Create a New Branch**: Before making changes, create a new branch for your updates:
   ```bash
   git checkout -b your-feature-branch
   ```

4. **Add or Edit Article Files**: Navigate to the `articles/` directory. You can create new article files in the respective part directory or edit existing ones. Follow the structure outlined above.

5. **Update the Index**: If you add a new article, ensure that you update `index.json` to include a reference to your new article.

6. **Commit Your Changes**: After making your changes, commit them:
   ```bash
   git add .
   git commit -m "Add new article or update existing article"
   ```

7. **Push Changes**: Push your changes to your forked repository:
   ```bash
   git push origin your-feature-branch
   ```

8. **Open a Pull Request**: Go to the original repository and open a "New Pull Request". Select your branch and describe your changes.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🤝 Acknowledgments

Thank you to everyone contributing to make the Constitution of Nepal more accessible and understandable through this dataset!

For any questions or discussions, feel free to open an issue or contact the repository maintainers.
