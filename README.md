---
title: Reference Management System
emoji: 📚
colorFrom: blue
colorTo: purple
sdk: docker
sdk_version: "latest"
app_file: app.py
pinned: false
---

<div align="center">

<h1>📚 Reference Management System</h1>
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=2563eb&center=true&vCenter=true&width=700&lines=Clean+Up+Your+BibTeX+References;Crossref+Enrichment+·+LTWA+Abbreviations;Protect+Acronyms+for+LaTeX" alt="Typing SVG"/>

<br/>

[![Python](https://img.shields.io/badge/Python-3.10+-3b82f6?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.x-4f46e5?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Crossref](https://img.shields.io/badge/Crossref-API-f59e0b?style=for-the-badge)](https://www.crossref.org/)
[![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-3b82f6?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Status](https://img.shields.io/badge/Status-Active-22c55e?style=for-the-badge)](#)

<br/>

[![Live Demo](https://img.shields.io/badge/%E2%96%B6_Live_Demo-Hugging_Face_Space-ffcc00?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/spaces/mnoorchenar/scopus)
[![Source Code](https://img.shields.io/badge/Source_Code-GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mnoorchenar/scopus)

<br/>

**📚 Reference Management System** — A simple web app to process and organize BibTeX references.

<br/>

---

</div>

## Table of Contents

- [What It Does](#-what-it-does)
- [How to Use](#-how-to-use)
- [Quick Start](#-quick-start)
- [Options Explained](#️-options-explained)
- [Database](#️-database)
- [Notes](#-notes)
- [Example Input](#-example-input)
- [Troubleshooting](#️-troubleshooting)
- [Learn More](#-learn-more)
- [Project Structure](#-project-structure)
- [Author](#-author)
- [Contributing](#-contributing)
- [Disclaimer](#️-disclaimer)
- [License](#-license)

---

## 📖 What It Does

**Input**: Paste your BibTeX entries  
**Process**: Enrich metadata, abbreviate journals, protect acronyms  
**Output**: View results and save to database  

No local files needed (main.tex, Refs.bib). Everything happens online.

---

## 📖 How to Use

1. **Paste BibTeX** into the input box
2. **Choose options**:
   - 🌐 **Enrich**: Fetch latest data from Crossref API (~3-5 sec per reference)
   - 📖 **Abbreviate**: Shorten journal names (requires `ltwa.txt`)
   - 🛡️ **Protect**: Wrap acronyms in braces for LaTeX (`{RNN}`, `{LSTM}`)
   - 💾 **Save**: Store in database for later use
3. **Process** and view results in table, BibTeX, or JSON format
4. **Export** as CSV or .bib file

---

## 🚀 Quick Start

### Local Setup
```bash
pip install -r requirements.txt
python app.py
# Open http://localhost:5000
```

### Hugging Face Spaces
Already deployed at: `huggingface.co/spaces/mnoorchenar/scopus`

---

## ⚙️ Options Explained

| Option | What it does | Notes |
|--------|-------------|-------|
| Enrich with Crossref | Updates references from online database | Slower but most accurate |
| Journal Abbreviations | Converts "Nature" → "Nature" using LTWA standard | Needs `ltwa.txt` file |
| Protect Acronyms | Wraps multi-uppercase words in braces | Prevents LaTeX from lowercasing |
| Save to Database | Stores all versions locally | SQLite - portable & persistent |

---

## 🗄️ Database

All processed references saved to `refs_management.db`:
- Original BibTeX
- Enriched metadata from Crossref
- Abbreviated journal names
- Acronym-protected versions
- Import timestamp

---

## 📝 Notes

- **No files to upload**: Paste content directly
- **Crossref API**: Free but rate-limited (~3-5 sec per entry)
- **Journal abbreviations**: Optional, but requires `ltwa.txt` with tab-separated format
- **Database**: SQLite - runs locally, no internet needed after processing
- **Export**: Download as CSV or BibTeX anytime

---

## 💡 Example Input

```bibtex
@article{Smith2024,
  author = {Smith, John},
  title = {Machine Learning for NLP},
  journal = {IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year = {2024}
}
```

---

## 🛠️ Troubleshooting

**App won't start**: Check `python app.py` runs on port 7860 (Hugging Face Spaces)

**"ltwa.txt not found"**: Optional file - app works without it (abbreviation feature just won't activate)

**Crossref slow**: Normal - API has rate limits. 10 references ≈ 30-50 seconds

**Results not saving**: Ensure "Save to Database" checkbox is enabled

---

## 📚 Learn More

- Crossref API: https://crossref.org
- Journal abbreviations: https://www.nlm.nih.gov/bsd/ltwa_mainpage.html

---

## 📁 Project Structure

```
Scopus/
│
├── 📂 Refs/
│   ├── Others/
│   ├── Refs.bib
│   ├── Refs.db
│   ├── ltwa.txt
│   ├── main.tex
│   └── overleaf.py
├── 📂 templates/                 # HTML templates
│   └── index.html
├── 📄 Dockerfile                 # Container definition (port 7860)
├── 📄 app.py                     # Application entry point
├── 📄 ltwa.txt
└── 📄 requirements.txt           # Python dependencies
```

---

## 👨‍💻 Author

<div align="center">

<table>
<tr>
<td align="center" width="100%">

<img src="https://avatars.githubusercontent.com/mnoorchenar" width="120" style="border-radius:50%; border: 3px solid #4f46e5;" alt="Mohammad Noorchenarboo"/>

<h3>Mohammad Noorchenarboo</h3>

<code>Data Scientist</code> &nbsp;|&nbsp; <code>AI Researcher</code> &nbsp;|&nbsp; <code>Biostatistician</code>

📍 &nbsp;Ontario, Canada &nbsp;&nbsp; 📧 &nbsp;[mohammadnoorchenarboo@gmail.com](mailto:mohammadnoorchenarboo@gmail.com)

──────────────────────────────────────

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mnoorchenar)&nbsp;
[![Personal Site](https://img.shields.io/badge/Website-mnoorchenar.github.io-4f46e5?style=for-the-badge&logo=githubpages&logoColor=white)](https://mnoorchenar.github.io/)&nbsp;
[![HuggingFace](https://img.shields.io/badge/HuggingFace-ffcc00?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/mnoorchenar)&nbsp;
[![Google Scholar](https://img.shields.io/badge/Scholar-4285F4?style=for-the-badge&logo=googlescholar&logoColor=white)](https://scholar.google.ca/citations?user=nn_Toq0AAAAJ&hl=en)&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mnoorchenar)

</td>
</tr>
</table>

</div>

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

---

## ⚠️ Disclaimer

> [!WARNING]
> Personal project built for my own use. It is shared as-is, without warranty of any kind, and is not intended as a product or service.

---

## 📜 License

Distributed under the **MIT License**.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:06b6d4&height=120&section=footer&text=Made%20with%20%E2%9D%A4%EF%B8%8F%20by%20Mohammad%20Noorchenarboo&fontColor=ffffff&fontSize=18&fontAlignY=80" width="100%"/>

[![GitHub Stars](https://img.shields.io/github/stars/mnoorchenar/scopus?style=social)](https://github.com/mnoorchenar/scopus/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/mnoorchenar/scopus?style=social)](https://github.com/mnoorchenar/scopus/fork)

<sub>The name "Reference Management System" is used purely for academic and research purposes. Any similarity to existing product names or trademarks is entirely coincidental. This project has no affiliation with any commercial entity.</sub>

</div>
