# ⛏️ Zeba Manuscript Sanity Check
**Zeba Manuscript Sanity Check** is a specialized automation tool designed for authors, editors, and small publishers to bridge the gap between a raw manuscript and a production-ready document.

This repository contains two core modules:
1. **Manuscript Cleaner**: A tool to audit headings and fix typographic inconsistencies in `.docx` files.
2. **Metadata Multiplier**: A converter that transforms simple text into industry-standard **ONIX 3.0**, **Dublin Core**, and **JSON-LD** formats.

## 🚀 Features
### 1. Manuscript Audit & Cleanup
* **Heading Audit**: Automatically loops through document paragraphs to verify that 'Heading 1' styles are sequential (e.g., catching if you skipped from Chapter 2 to Chapter 4).
* **Whitespace Cleanup**: Uses regex logic to find and replace multiple spaces with a single space.
* **Smart Quote Conversion**: Applies a heuristic to replace "straight" quotes with curly (typographic) quotes based on surrounding characters.
* **Sanity Reporting**: Generates a live log of every change made, which can be exported as a text file.

### 2. Metadata Multiplier
* **ONIX 3.0 Generation**: Creates distributor-ready XML files for Amazon, Ingram, and others.
* **Dublin Core**: Generates library-standard XML for archival and institutional discovery.
* **JSON-LD**: Produces Schema.org 'Book' objects to boost SEO and search engine visibility.
* **Live Preview**: Allows you to see a bolded, human-readable preview of your parsed data before downloading.

---

## 🛠️ Technical Steps
For developers or interns looking to contribute or understand the backend:
1. **Environment Setup**:
```bash
pip install streamlit lxml python-docx onixcheck
```

2. **Input Parsing**: The tool reads `.txt` files or text areas line-by-line, mapping `Key: Value` pairs into a Python dictionary.
3. **XML Construction**: Uses the `lxml` library to build strict XML trees adhering to the **Editeur ONIX 3.0** namespace.
4. **Regex Cleaning**: Employs Python's `re` module with Unicode character support (e.g., `\u201c`, `\u201d`) to handle typography without encoding errors.
5. **Validation**: Integrates `onixcheck` to ensure the output XML meets official industry standards.

---

## 📂 Project Structure

```text
Zeba_Manuscript_Sanity_Check/
├── app.py              # Main Streamlit application
├── requirements.txt    # Dependency list (lxml, python-docx, streamlit)
├── assets/             # Images and iconography
└── README.md           # Project documentation
```

---

## 💻 Installation & Usage
### Local Development

1. Clone the repository:
```bash
git clone https://github.com/sufyanism/Zeba_Manuscript_Sanity_Check.git

```

2. Navigate to the directory:
```bash
cd Zeba_Manuscript_Sanity_Check

```

3. Install dependencies:
```bash
pip install -r requirements.txt

```

4. Run the app:
```bash
streamlit run app.py

```

## ☁️ Deployment on Railway

This project is configured for one-click deployment on [Railway](https://railway.app/).

1. **Fork this repository** to your GitHub account.
2. **Create a new Project** on Railway and select "Deploy from GitHub repo".
3. **Automatic Detection**: Railway will use the `railway.json` and `requirements.txt` to:
* Install Python and dependencies (`lxml`, `streamlit`, `python-docx`).
* Start the Streamlit server on the correct port.


## Screenshot
<img width="1177" height="772" alt="Zeba_Manuscript_Sanity_Check" src="https://github.com/user-attachments/assets/690e73c5-dcaf-4659-85ff-467569dd116d" />

## Screencast
https://github.com/user-attachments/assets/09702b4c-67fb-4ea8-8ac9-ddd4f1584864

## About Me 
✨ I’m **Sufyan bin Uzayr**, an open-source developer passionate about building and sharing meaningful projects.
You can learn more about me and my work at [sufyanism.com](https://sufyanism.com/) or connect with me on [Linkedin](https://www.linkedin.com/in/sufyanism)

## Your all-in-one learning hub! 
🚀 Explore courses and resources in coding, tech, and development at **zeba.academy** and **code.zeba.academy**. Empower yourself with practical skills through curated tutorials, real-world projects, and hands-on experience. Level up your tech game today! 💻✨

**Zeba Academy**  is a learning platform dedicated to **coding**, **technology**, and **development**.  
➡ Visit our main site: [zeba.academy](https://zeba.academy)   </br>
➡ Explore hands-on courses and resources at: [code.zeba.academy](https://code.zeba.academy)   </br>
➡ Check out our YouTube for more tutorials: [zeba.academy](https://www.youtube.com/@zeba.academy)  </br>
➡ Follow us on Instagram: [zeba.academy](https://www.instagram.com/zeba.academy/)  </br>

**Thank you for visiting!**
