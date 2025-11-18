## Publish the book on GitHub Pages

1. [Install Quarto](https://quarto.org/docs/get-started/) and confirm `quarto check install` succeeds.
2. Render the HTML + PDF outputs into `docs/` (GitHub Pages expects this folder):  
   ```bash
   quarto render
   ```
3. Commit the rendered `docs/` folder (it includes both the HTML site and the generated PDF download):
   ```bash
   git add docs
   git commit -m "Render Quarto book"
   ```
4. Create a new GitHub repository named `RFCBook`, push the project, and enable *Settings → Pages → Build from main branch / docs folder*.
5. Update the `book.repo-url` value inside `_quarto.yml` so the "View source" and "Report issue" buttons point at the correct GitHub repo URL.

After the above, every time you run `quarto render` and push, the hosted book at `https://<your-user>.github.io/RFCBook/` will update automatically.
