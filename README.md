# Juan Antonio Monleón de la Lluvia — Résumé

**Nuclear Engineer · PhD Student in Neutronics @ ASNR (formerly IRSN), France**

Uncertainty quantification and variance-reduction techniques for reactor-vessel
ageing. Hands-on with MCNP, Serpent, OpenMC, NJOY and ADVANTG; active member
of the JEFF and SINBAD nuclear-data communities. Lead developer of **KIKA**, a
cross-platform desktop application (Tauri + React + FastAPI) for nuclear-data
visualization, sensitivity analysis, and uncertainty quantification, built on
top of the open-source [**kika-nd**](https://github.com/juanmonleon/kika)
Python library (PyPI).

📄 **[Download the résumé (PDF)](Resume.pdf)** &nbsp;·&nbsp;
🌐 **[View the HTML version](https://juanmonleon.github.io/Resume/)** &nbsp;·&nbsp;
💼 **[LinkedIn](https://linkedin.com/in/juanantonio-monleondelalluvia)** &nbsp;·&nbsp;
✉️ **[juanmonleon96@gmail.com](mailto:juanmonleon96@gmail.com)**

## Selected publication

**J. A. Monleon de la Lluvia, M. Brovchenko, D. Rochman, E. Dumonteil**,
"[Towards Efficient Nuclear Data Uncertainty Quantification in Radiation
Shielding Calculations](https://www.tandfonline.com/doi/full/10.1080/00295639.2025.2510048)",
*Nuclear Science and Engineering*, 2025. &nbsp;·&nbsp;
[pre-print PDF](files/Monleon_2025_NSE_preprint.pdf)

---

## Preview

<p align="center">
  <a href="Resume.pdf">
    <img src="assets/resume_page_1.png" alt="Résumé preview — page 1" width="720">
  </a>
</p>

<details>
<summary>See page 2</summary>

<p align="center">
  <img src="assets/resume_page_2.png" alt="Résumé preview — page 2" width="720">
</p>

</details>

---

## Repository contents

| Path | What it is |
| --- | --- |
| [`Resume.pdf`](Resume.pdf) | Latest compiled résumé (printable) |
| [`index.html`](index.html) / [`style.css`](style.css) | Source of the résumé — a small static site |
| [`assets/`](assets) | Rendered page previews used above |
| [`files/`](files) | Supporting documents (degree certificates, papers, poster) |

### Supporting documents

- **Journal paper (2025)** — [Towards Efficient Nuclear Data Uncertainty Quantification in Radiation Shielding Calculations](files/Monleon_2025_NSE_preprint.pdf) · *Nuclear Science and Engineering* · [DOI](https://www.tandfonline.com/doi/full/10.1080/00295639.2025.2510048)
- **Conference paper** — [Sensitivity Analysis and Uncertainty Quantification in PWR Irradiation Ageing-like problems](files/Monleon_2024_RPSD_conference.pdf) · ANS Winter Conference RPSD, Orlando (Nov 2024)
- **Master's thesis** — [Reducing Spectrum-Driven Uncertainties with Variance Reduction Techniques](files/Monleon_2023_MasterThesis_SCK-CEN.pdf) · SCK CEN, Belgium
- **Master thesis research** — [Enhancing the EXFOR nuclear data library with Machine Learning Techniques](files/Monleon_2023_MasterResearch_UPM.pdf)
- **Award-winning poster** — [JdT 2024 Poster (IRSN)](files/Monleon_2024_JdT_poster.pdf)
- **Degree certificates** — [MII](files/Monleon_Master_MII_UPM.pdf) · [MUCTN](files/Monleon_Master_MUCTN_UPM.pdf) · [GITI](files/Monleon_Bachelor_GITI_UPM.pdf)

---

## Working on the résumé locally

The site is a single static HTML file — pick whichever preview workflow you like:

- **VS Code + Live Server** *(recommended — auto-reloads on save)*: install the
  [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
  extension, right-click `index.html` → *Open with Live Server*.
- **Zero-install terminal**: `python3 -m http.server 8000`, then open
  <http://localhost:8000>. Manual refresh on each save.
- **No server at all**: just open `index.html` directly in a browser.

## Regenerating `Resume.pdf` and the previews

1. Open the local preview above and use the browser's **Print → Save as PDF**
   (A4, margins: *Default*, background graphics: *on*) to overwrite
   `Resume.pdf`.
2. Re-render the page thumbnails embedded in this README:

   ```bash
   gs -sDEVICE=png16m -r150 -dTextAlphaBits=4 -dGraphicsAlphaBits=4 \
      -o assets/resume_page_%d.png Resume.pdf
   mogrify -trim -bordercolor white -border 20 assets/resume_page_*.png
   ```
