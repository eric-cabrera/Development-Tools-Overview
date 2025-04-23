# Steps to Publish a Site to GitHub Pages

1. **Prepare Your Repository**:
   - Ensure all your changes are committed and pushed to the `main` branch.

2. **Create a `gh-pages` Branch**:
   - Open your terminal and run the following commands:
     ```powershell
     git checkout --orphan gh-pages
     git reset --hard
     git add .
     git commit -m "Deploy to GitHub Pages"
     git push -u origin gh-pages --force
     ```

3. **Enable GitHub Pages**:
   - Go to your repository on GitHub.
   - Navigate to **Settings > Pages**.
   - Under the "Source" section, select the `gh-pages` branch.
   - Click **Save**.

4. **Verify Your Site**:
   - After a few minutes, your site should be live at `https://<your-username>.github.io/<repository-name>/`.

5. **Update Content**:
   - To update your site, make changes in your local repository, commit them, and push to the `gh-pages` branch:
     ```powershell
     git checkout gh-pages
     git add .
     git commit -m "Update site content"
     git push
     ```

6. **Optional: Return to Main Branch**:
   - If you need to work on the main branch again, switch back:
     ```powershell
     git checkout main
     ```
