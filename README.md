# Juan Antonio Monleón de la Lluvia — Résumé

**Nuclear Engineer · PhD Student in Neutronics @ ASNR (formerly IRSN), France**

Uncertainty quantification and variance-reduction techniques for reactor-vessel
ageing. Hands-on with MCNP, Serpent, OpenMC, NJOY and ADVANTG, and Python for
nuclear data / machine-learning workflows.

📄 **[Download the résumé (PDF)](Resume.pdf)** &nbsp;·&nbsp;
🌐 **[View the HTML version](https://juanmonleon.github.io/Resume/)** &nbsp;·&nbsp;
💼 **[LinkedIn](https://linkedin.com/in/juanantonio-monleondelalluvia)** &nbsp;·&nbsp;
✉️ **[juanmonleon96@gmail.com](mailto:juanmonleon96@gmail.com)**

---

## Preview

<p align="center">
  <a href="Resume.pdf">
    <img src="assets/resume_page_1.png" alt="Résumé preview — page 1" width="720">
  </a>
</p>

<details>
<summary>See pages 2 and 3</summary>

<p align="center">
  <img src="assets/resume_page_2.png" alt="Résumé preview — page 2" width="720">
  <img src="assets/resume_page_3.png" alt="Résumé preview — page 3" width="720">
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

- **Conference paper** — [Sensitivity Analysis and Uncertainty Quantification in PWR Irradiation Ageing-like problems](files/2024-11_RPSD_Conference.pdf) · ANS Winter Conference RPSD, Orlando (Nov 2024)
- **Master's thesis** — [Reducing Spectrum-Driven Uncertainties with Variance Reduction Techniques](<files/Reducing Spectrum-Driven Uncertainties with Variance Reduction Techniques.pdf>) · SCK CEN, Belgium
- **Master thesis research** — [Enhancing the EXFOR nuclear data library with Machine Learning Techniques](<files/Enhancing the EXFOR nuclear data library with Machine Learning Techniques.pdf>)
- **Award-winning poster** — [JdT 2024 Poster (IRSN)](files/MONLEON_Poster_JdT24.pdf)
- **Degree certificates** — [MII](files/Titulo_MII.pdf) · [MUCTN](files/Titulo_MUCTN.pdf) · [GITI](files/Titulo_GITI.pdf)

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
