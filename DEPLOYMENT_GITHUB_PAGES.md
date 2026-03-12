## Deploying this site to GitHub Pages

This project is set up to be served as a static site (for example a Jekyll site) from a GitHub repository. Follow these steps to get it live at `https://<your-username>.github.io` on GitHub Pages.

> You only need to do this once per repository. After that, any new commits you push to the configured branch will automatically trigger a redeploy.

### 1. Prepare a local Git repository

In a terminal, from the project root (this folder):

```bash
cd /Users/angela/Documents/Mickey/workspace/website
git init
git add .
git commit -m "Initial site"
```

If `git init` tells you the repo already exists, you can skip that line.

### 2. Create a GitHub repository

1. Sign in to GitHub in your browser.
2. Click **New repository**.
3. Choose a name:
   - If you want a **user site** at `https://<your-username>.github.io`, name the repo exactly `<your-username>.github.io`.
   - Otherwise, choose any name (e.g. `personal-website`) and GitHub Pages will serve it under `https://<your-username>.github.io/<repo-name>/`.
4. Set **Visibility** to **Public** (GitHub Pages works best with public repos on the free tier).
5. Click **Create repository**.

GitHub will now show you the repo URL, which looks like:

```text
git@github.com:<your-username>/<repo-name>.git
```

or

```text
https://github.com/<your-username>/<repo-name>.git
```

Copy that URL.

### 3. Connect your local repo to GitHub and push

Back in your terminal, still in the project root:

```bash
git remote add origin <copied-repo-url>
git branch -M main
git push -u origin main
```

If `origin` already exists, replace the first command with:

```bash
git remote set-url origin <copied-repo-url>
```

and then run the `git push` command again.

Once this completes, your code is on GitHub.

### 4. Enable GitHub Pages in repo settings

1. In your browser, open your GitHub repository page.
2. Click the **Settings** tab.
3. In the left sidebar, click **Pages** (sometimes under “Code and automation” → “Pages”).
4. Under **Source** (or **Build and deployment**):
   - Set **Source** to **Deploy from a branch**.
   - Set **Branch** to `main` and **/ (root)** as the folder.
5. Click **Save**.

GitHub will start building and deploying the site. This usually takes from a few seconds up to a couple of minutes.

### 5. Verify the live site

On the same **Pages** settings screen:

1. Wait until you see a green banner showing that the site is deployed, along with a URL such as:
   - `https://<your-username>.github.io` (for a user site repo), or
   - `https://<your-username>.github.io/<repo-name>/` (for a project repo).
2. Click the URL. It should open your site in a new tab.

If the page does not load immediately:

- Wait 1–2 minutes and refresh – initial GitHub Pages deployments can take a short time to propagate.
- Confirm that:
  - The repo is public.
  - The **Branch** in Pages settings is set to `main`.
  - Your site’s entry file (`index.html` or `index.md`) is in the repository root or configured correctly for your static site generator.

### 6. Ongoing workflow

Once GitHub Pages is enabled:

- Make changes locally.
- Commit them:

  ```bash
  git add .
  git commit -m "Describe your change"
  git push
  ```

- GitHub will automatically rebuild and redeploy your site. Within a minute or two, refreshing your GitHub Pages URL should show the updated content.

