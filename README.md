# 📚 BibTeX Reference Manager and Enhancer

This Jupyter Notebook project provides tools for parsing, managing, filtering, and enhancing `.bib` files typically used in LaTeX documents.  
It supports cleaning duplicated references, matching citations in `.tex` files, and updating BibTeX entries from online databases.

## 🚀 Features
- 🔎 Parse `.bib` files and extract structured reference data.
- 🛠️ Identify and manage duplicate entries by key or title.
- 📄 Filter references used inside `.tex` files and create a clean database.
- 🌐 Fetch missing BibTeX entries using CrossRef API based on paper titles.
- ✏️ Automatically correct and update BibTeX keys inside entries.
- 💾 Store everything in a local SQLite database.

## 📥 Input Required

- **A `.bib` file**: containing your reference entries (e.g., `Refs.bib`).
- **A `.tex` file**: your LaTeX document where citations (`\cite{}`) are used (e.g., `main.tex`).

Simple examples:
```python
bibtex_file = 'Refs.bib'
tex_file = 'main.tex'
```

## 📤 Output Generated

- **SQLite Database** (`references.db`):
  - Table `bibtex_entries` with parsed references from `.bib` file.
  - Table `filtered_bibtex_entries` with only cited references from `.tex` file.
- **Updated BibTeX Entries**:
  - New BibTeX information fetched via DOI lookup if missing.
  - Corrected BibTeX keys matched to your original keys.

The final result can be easily exported back to LaTeX for clean bibliography management.

## 🛠️ How to Use
1. Install the required Python packages:
   ```bash
   pip install pandas itables selenium habanero beautifulsoup4 requests
   ```

2. Prepare your `.bib` file and `.tex` file inside the `bibtext/` folder.

3. Open and run the notebook:
   - Parse the `.bib` file and create the database.
   - Extract citation keys from the `.tex` file.
   - Filter references and match entries.
   - Fetch missing BibTeX entries (optional).
   - Update BibTeX keys if needed.

4. Review and export your final cleaned database or BibTeX entries.

⚡ Chrome browser will open automatically if you run parts that use Selenium (optional).

## ⚠️ Disclaimer
This tool is developed for **personal academic use only**.  
It interacts with publicly available metadata sources (like CrossRef) and is intended to assist researchers in managing references.  
The developer takes **no responsibility for misuse** or violations of any publisher's terms.  
Please use responsibly according to publisher and database policies.
