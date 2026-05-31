# 📄 Cao Anh Huân — Resume

![LaTeX](https://img.shields.io/badge/LaTeX-47A141?style=for-the-badge&logo=LaTeX&logoColor=white)
![XeLaTeX](https://img.shields.io/badge/XeLaTeX-008080?style=for-the-badge)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

Professional LaTeX-based resume for **Cao Anh Huân — Backend Engineer**, with automated PDF generation via GitHub Actions.

[📥 Download Latest PDF](https://github.com/ah2909/CV_Huan/releases/latest)

---

## 📁 Repository Structure

```
CV_Huan/
├── main.tex          # Main LaTeX source (imports the parts below)
├── preamble.tex      # Packages, settings, custom commands & environments
├── header.tex        # Name and contact information
├── content.tex       # Resume sections (Summary, Education, Experience, ...)
└── .github/workflows/
    └── latex.yml      # CI: build PDF + auto-release on push
```

## 🚀 Build Locally

Requires a TeX distribution with XeLaTeX (TeX Live / MiKTeX).

```bash
# Recommended
latexmk -xelatex -shell-escape main.tex

# Or directly
xelatex -shell-escape main.tex
```

Output: `main.pdf`.

## 🔄 GitHub Actions

On every push to `main`, the workflow compiles `main.tex`, renames the output to
`Cao_Anh_Huan_Resume.pdf`, and publishes a GitHub Release tagged `build-{run_number}`
with a changelog generated from commit history.

## 🎨 Customization

- **Personal info / contact** → `header.tex`
- **Resume content** → `content.tex`
- **Colors, spacing, fonts** → `preamble.tex` (e.g. `\definecolor{primaryColor}{RGB}{0, 79, 144}`)

---

Made with ❤️ using LaTeX.
