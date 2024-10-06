# Constitution of Nepal Dataset

Welcome to the **Constitution of Nepal** dataset repository! This repository aims to provide a structured and well-organized dataset of the Constitution of Nepal, making it easy for contributions, analysis, and future applications such as **NLP tasks**.

We hope this project will help foster better understanding, accessibility, and research for legal and constitutional data. The original document can be found in the repository as [Constitution_of_Nepal_2072_ENG.pdf](Constitution_of_Nepal_2072_ENG.pdf).

This repository is maintained under the **KEC Computer Club** organization. To learn more about the club, visit [computerclubkec.github.io](https://computerclubkec.github.io).

---

## 📁 Repository Structure

The constitution is divided into smaller, manageable sections for easy contributions. The dataset is stored in a hierarchical JSON format, allowing for clear organization and easy navigation.

Here’s the updated file structure:

```
├── index.json                          (Main index of the constitution)
├── sections/                           (Directory containing individual parts)
    ├── part1/                          (Directory for Part 1)
        ├── section1.json               (Contains Part 1, Section 1)
        ├── section2.json               (Contains Part 1, Section 2)
    ├── part2/                          (Directory for Part 2)
        ├── section10.json              (Contains Part 2, Section 10)
        ├── section11.json              (Contains Part 2, Section 11)
    ├── ...                             (Additional parts and sections)
    ├── preamble.json                   (Contains the Preamble)
├── Constitution_of_Nepal_2072_ENG.pdf  (Original PDF document of the Constitution)
```

### **Main Files**

- **`index.json`**: This file serves as an overview of the entire constitution. It includes references to all parts and sections, with paths to their respective JSON files.
- **`sections/`**: This directory contains individual directories for each part of the constitution, with JSON files for each section inside the respective part directory.
- **`Constitution_of_Nepal_2072_ENG.pdf`**: The original PDF document of the Constitution of Nepal for reference.

### **Example of `index.json`:**
```json
{
  "title": "Constitution of Nepal",
  "preamble": {
    "content": "We, the Sovereign People of Nepal...",
    "file": "sections/preamble.json"
  },
  "parts": [
    {
      "part_number": 1,
      "title": "Preliminary",
      "sections": [
        {
          "section_number": 1,
          "title": "Constitution as the fundamental law",
          "file": "sections/part1/section1.json"
        },
        {
          "section_number": 2,
          "title": "Sovereignty and state authority",
          "file": "sections/part1/section2.json"
        }
      ]
    },
    {
      "part_number": 2,
      "title": "Citizenship",
      "sections": [
        {
          "section_number": 10,
          "title": "Not to deprive of citizenship",
          "file": "sections/part2/section10.json"
        },
        {
          "section_number": 11,
          "title": "To be citizens of Nepal",
          "file": "sections/part2/section11.json"
        }
      ]
    }
  ]
}
```

### **Example of Individual Section File (`sections/part1/section1.json`):**
```json
{
  "section_number": 1,
  "title": "Constitution as the fundamental law",
  "content": "This Constitution is the fundamental law of Nepal. Any law inconsistent with this Constitution shall, to the extent of such inconsistency, be void.",
  "part_number": 1
}
```

---

## 🛠️ How to Contribute

We welcome contributions from everyone! To make the process as smooth as possible, please follow these steps:

1. **Fork the Repository**: Click the "Fork" button at the top right of the page to create a copy of the repository on your GitHub account.

2. **Clone the Repository**: Clone your forked repository to your local machine using:
   ```bash
   git clone https://github.com/yourusername/constitution-of-nepal-dataset.git
   ```

3. **Create a New Branch**: Before making changes, create a new branch for your updates:
   ```bash
   git checkout -b your-feature-branch
   ```

4. **Add or Edit Section Files**: Navigate to the `sections/` directory. You can create a new section file in the respective part directory or edit an existing one. Follow the structure outlined above.

5. **Update the Index**: If you add a new section, make sure to update `index.json` to include a reference to your new section.

6. **Commit Your Changes**: After making your changes, commit them:
   ```bash
   git add .
   git commit -m "Add new section or update existing section"
   ```

7. **Push Changes**: Push your changes to your forked repository:
   ```bash
   git push origin your-feature-branch
   ```

8. **Open a Pull Request**: Go to the original repository and click on "New Pull Request". Select your branch and describe your changes.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🤝 Acknowledgments

Thanks to everyone who contributes to making the Constitution of Nepal more accessible and understandable through this dataset!

For any questions or discussions, feel free to open an issue or contact the repository maintainer.